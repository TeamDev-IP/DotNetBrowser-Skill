
# Google Maps in DotNetBrowser

**Lead**
Google Maps has no .NET API. The map is a web page, and everything you do to
it goes through the Maps JavaScript API. This tutorial shows how to display
that page in a WinForms application and drive the map from .NET code.


DotNetBrowser connects the two sides in both directions. From .NET, an
`IJsObject` holds a live reference to a JavaScript object, so you can read its
properties and call its methods. From the page, an object injected as
`window.external` lets JavaScript call into your .NET code. The application
built here uses both directions: .NET changes the zoom level and adds markers,
and the page reports back when the map is ready and when it has determined the
current position.

The complete example is available in the DotNetBrowser-Examples repository, for
[C#][example-csharp] and [VB.NET][example-vbnet].

## Prerequisites

You need a Google Maps JavaScript API key. Create one in the Google Cloud
console and enable the Maps JavaScript API for it.

This tutorial loads the map page from the local file system, and a page loaded
that way sends no referrer, so Google rejects a key restricted by HTTP referrer
with `RefererNotAllowedMapError`. Use an unrestricted key while you work
through the tutorial.

Treat that as a local development setting rather than something to ship. In
production, serve the page over HTTP or HTTPS from an origin you control, and
restrict the key to that origin.

## Loading the map

Put the map in an HTML file next to your application. Google loads the Maps
JavaScript API through an inline bootstrap loader, which fetches the library
asynchronously and exposes `google.maps.importLibrary()`:

```html
<div id="map"></div>

<script>
    (g => {
        // The bootstrap loader, copied verbatim from the Google documentation.
    })({
        key: "API_KEY",
        v: "weekly"
    });
</script>
```

Replace `API_KEY` with your own key. The full loader body is in the
[map.html][example-map-html] file of the example.

Next, create the map. `importLibrary()` returns a promise, so the code that
builds the map runs asynchronously:

```javascript
let map;

async function initMap() {
    const {Map} = await google.maps.importLibrary("maps");
    await google.maps.importLibrary("marker");

    map = new Map(document.getElementById("map"),
        {
            center: {lat: 48.209331, lng: 16.381302},
            zoom: 4,
            mapId: "DEMO_MAP_ID"
        });

    window.external.OnMapInitialized(map);
}

initMap();
```

Three details matter here. The `map` variable is global, which is what lets
.NET reach the map later. The `marker` library is imported up front, so that
adding a marker from .NET does not have to wait for a promise. And the call to
`window.external` at the end hands the finished map to .NET — the next section
covers how that object gets there.

**Note**
`DEMO_MAP_ID` is the map ID Google provides so you can try advanced markers
without creating one first. Replace it with a map ID of your own before you
ship: your own map ID is what ties the map to a style you configure in the
Google Cloud console, and changing that style then takes no application
update. See [Get a map ID][maps-map-id].


Load the page through a `file://` URI rather than a bare Windows path:

```csharp
browser.Navigation.LoadUrl(new Uri(Path.GetFullPath("map.html")).AbsoluteUri);
```

## Connecting the page to .NET

The page above calls `window.external.OnMapInitialized(map)`, but `external`
is not a standard browser object. You put it there, by handling
`InjectJsHandler`. DotNetBrowser invokes that handler after it creates the
JavaScript context and before the page scripts run:


**C#**

```csharp
// Inject this form into the page as window.external, so that
// map.html can call back into .NET.
browser.InjectJsHandler = new Handler<InjectJsParameters>(OnInjectJs);
```

**VB**

```vb
' Inject this form into the page as window.external, so that
' map.html can call back into .NET.
browser.InjectJsHandler = New Handler(Of InjectJsParameters)(AddressOf OnInjectJs)
```



The handler assigns the form itself to `window.external`, which makes the
form's public methods callable from JavaScript. `OnMapInitialized` is one of
them. It receives the JavaScript map as an `IJsObject` and stores it:


**C#**

```csharp
/// <summary>
///     Called from map.html once the Maps JavaScript API has loaded and
///     the map has been created.
/// </summary>
public void OnMapInitialized(IJsObject jsMap)
{
    map = new GoogleMap(jsMap);
    BeginInvoke((Action) (() => mapControls.Enabled = true));
}
```

**VB**

```vb
''' <summary>
'''     Called from map.html once the Maps JavaScript API has loaded and
'''     the map has been created.
''' </summary>
Public Sub OnMapInitialized(jsMap As IJsObject)
	map = New GoogleMap(jsMap)
	BeginInvoke(New Action(Sub() mapControls.Enabled = True))
End Sub
```



Waiting for this callback is what makes the rest of the application reliable.
The map does not exist until `importLibrary()` resolves, so any code that
touches it before `OnMapInitialized` runs would fail. The example keeps its
toolbar disabled until then.

For more on calling between .NET and JavaScript, see the
[JavaScript](https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/) guide.

## Changing the zoom

With the map in hand, `IJsObject` gives you its methods. Wrapping it in a small
class keeps the JavaScript details in one place:


**C#**

```csharp
public int Zoom
{
    get { return (int) map.Invoke<double>("getZoom"); }

    set
    {
        int zoom = Math.Min(MaxZoomLevel, Math.Max(MinZoomLevel, value));
        map.Invoke("setZoom", zoom);
    }
}
```

**VB**

```vb
Public Property Zoom() As Integer
	Get
		Return CInt(map.Invoke(Of Double)("getZoom"))
	End Get

	Set
		Dim zoomLevel As Integer = Math.Min(MaxZoomLevel, Math.Max(MinZoomLevel, Value))
		map.Invoke("setZoom", zoomLevel)
	End Set
End Property
```



`Invoke` calls the JavaScript function and returns its result, converted to the
requested .NET type. Google Maps returns the zoom level as a JavaScript number,
which arrives as a `double`.

**Important**
`Invoke` blocks the calling thread until the browser returns a result, so it
must not run on the UI thread. Call it from a background thread, and marshal
back to the UI thread when you need to update a control.


The same rule applies in the other direction. A method that JavaScript calls
through `window.external` runs on the browser thread, so it should not make
another blocking JavaScript call.

## Adding markers

Markers are JavaScript objects too, and you can create them from .NET. Build
the object in the page context, then set its properties:


**C#**

```csharp
// Create the marker in the page context and attach it to the map.
IJsObject marker = Frame
                  .ExecuteJavaScript<IJsObject>(
                       "new google.maps.marker.AdvancedMarkerElement({map: map})")
                  .Result;

// AdvancedMarkerElement exposes the position as a property rather
// than through a setter method.
marker.Properties["position"] = ToLatLngLiteral(latitude, longitude);
```

**VB**

```vb
' Create the marker in the page context and attach it to the map.
Dim marker As IJsObject =
	Frame.ExecuteJavaScript(Of IJsObject)(
		"new google.maps.marker.AdvancedMarkerElement({map: map})").Result

' AdvancedMarkerElement exposes the position as a property rather
' than through a setter method.
marker.Properties("position") = ToLatLngLiteral(latitude, longitude)
```



`ExecuteJavaScript<IJsObject>` evaluates the constructor call and returns a
reference to the new marker. Assigning to `Properties["position"]` then sets
the marker's position, exactly as JavaScript assignment would.

`ExecuteJavaScript` returns a task, and reading `.Result` waits for it. That
blocks the calling thread just as `Invoke` does, so the same rule applies: the
example reaches this method from a background thread.

Two constraints come from Google Maps rather than from DotNetBrowser. Advanced
markers render only on a map created with a map ID, which is why `initMap()`
passes `mapId`. And they replace `google.maps.Marker`, which Google deprecated
in February 2024.

The position is built with the invariant culture on purpose. JSON requires a
dot as the decimal separator, so a locale that uses a comma would produce
coordinates the page cannot parse.

## Enabling geolocation

The example's "My location" button asks the page for the current position.
Chromium treats geolocation as a permission and denies it by default, so the
application has to grant it through a handler on the profile:


**C#**

```csharp
// navigator.geolocation asks for a permission, which is denied
// unless a permission handler grants it.
engine.Profiles.Default.Permissions.RequestPermissionHandler =
    new Handler<RequestPermissionParameters, RequestPermissionResponse>(p =>
        p.Type == PermissionType.Geolocation
            ? RequestPermissionResponse.Grant()
            : RequestPermissionResponse.Deny());
```

**VB**

```vb
' navigator.geolocation asks for a permission, which is denied
' unless a permission handler grants it.
engine.Profiles.Default.Permissions.RequestPermissionHandler =
	New Handler(Of RequestPermissionParameters, RequestPermissionResponse)(
		Function(p)
			If p.Type = PermissionType.Geolocation Then
				Return RequestPermissionResponse.Grant()
			End If
			Return RequestPermissionResponse.Deny()
		End Function)
```



The [Permissions](https://teamdev.com/dotnetbrowser/docs/guides/gs/permissions/) guide covers the handler in
detail.

**Note**
The permission alone is not enough. Chromium determines the position through a
Google service, which needs its own credentials: enable the Google Maps
Geolocation API and pass the keys to the engine, as described in the
[Engine](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#google-apis) guide. These keys are separate
from the Maps JavaScript API key in `map.html`, and one does not substitute for
the other.


## Troubleshooting

**The map appears for a moment, then is replaced by "Oops! Something went
wrong."** Google validates the API key after the first tiles render, so a key
problem surfaces a second or two late. The key is missing, invalid, or
restricted by HTTP referrer. Open the DevTools console for the specific error
code.

**Markers never appear, and the map is otherwise fine.** The map was created
without a map ID. Advanced markers need one.

**Geolocation fails with an empty error message.** Chromium reports an empty
`GeolocationPositionError.message` when it cannot reach the location service.
Configure the engine-level Google API keys.

## Result

The application displays a map, moves it between zoom levels, and drops a
marker at the coordinates you type:

![A WinForms window showing Google Maps with a marker on Vienna](https://teamdev.com/dotnetbrowser/img/tutorials/use-cases/google-maps/marker.webp)
**Image-Caption**
The example application with a marker added from .NET code.


[maps-map-id]: https://developers.google.com/maps/documentation/get-map-id
[example-csharp]: https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/csharp/winforms/GoogleMaps
[example-vbnet]: https://github.com/TeamDev-IP/DotNetBrowser-Examples/tree/v4/vbnet/winforms/GoogleMaps
[example-map-html]: https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/v4/csharp/winforms/GoogleMaps/map.html
