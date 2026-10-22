# DotNetBrowser oder WebView2: Ein Vergleich für Entwickler

Wenn es um eingebettete Browser geht, bietet die Branche die unterschiedlichsten
Lösungen: frei und kommerziell, Open Source und proprietär. Sie unterscheiden
sich darin, was sie können, wie sie genutzt werden und welche zusätzlichen
Services dazugehören. In diesem Artikel helfen wir Ihnen bei der Auswahl der
richtigen Lösung.

Im Artikel [DotNetBrowser oder CefSharp][dotnetbrowser-vs-cefsharp-article]
haben wir das Open-Source-Projekt CefSharp mit DotNetBrowser verglichen und
erläutert, wie man sich entscheiden kann.

Heute nehmen wir das proprietäre WebView2 unter die Lupe und argumentieren, dass
DotNetBrowser für den kommerziellen Einsatz besser geeignet ist. Wir beginnen
mit organisatorischen und rechtlichen Aspekten. Danach gehen wir auf die
funktionalen Unterschiede ein.

Die Migration zu DotNetBrowser ist unkompliziert. Sie finden alle Details
im [Migration Guide][migration-guide], der Sie durch den Prozess führt und die
wichtigsten Punkte erklärt.

## In a nutshell


<div class="table-wrapper comparison-table">

|                              | <img class="product-logo" src="/dotnetbrowser/blog/dotnetbrowser-or-webview2/edge-logo.svg" alt="WebView2 logo" width="22" height="22"/> WebView2 | <img class="product-logo" src="/images/product-logos/dotnetbrowser.svg" alt="DotNetBrowser logo" width="22" height="22"/> DotNetBrowser |
|:-----------------------------|:---------------------------------------------------------------------------------------------------------------------------------------------|:----------------------------------------------------------------------------------------------------------------------------------------|
| Lizenz                       | Proprietär                                                                                                                                   | Kommerziell                                                                                                                             |
| Unterstützte Betriebssysteme | Nur Windows                                                                                                                                  | Windows, macOS, Linux                                                                                                                   |
| Unterstützte UI-Toolkits     | WinForms, WPF, WinUI 3, MAUI                                                                                                                 | WinForms, WPF, WinUI 3, Avalonia                                                                                                        |
| [Datensammlung][privacy]     | Ja                                                                                                                                           | Nein                                                                                                                                    |
| Headless Mode                | Nein                                                                                                                                         | Ja, läuft in der Konsole oder als Service                                                                                               |
| [Support][support]           | Öffentliches GitHub-Repository                                                                                                               | Ja, vertraulich, mit SLA                                                                                                                |

</div>

DotNetBrowser und WebView2 sind ausgereifte Lösungen von kommerziellen
Unternehmen mit umfangreicher Erfahrung in diesem Bereich. Damit erhalten Sie
eine Softwarelösung, die funktioniert und nicht von einer Open-Source-Community
abhängt.

Wählen Sie WebView2, wenn:

* Sie ausschließlich freie Software einsetzen dürfen.
* Sie die Vorteile der Evergreen-Distribution nutzen möchten.
* Es für Sie in Ordnung ist, dass Microsoft Daten der Endanwender sammelt.

Wählen Sie DotNetBrowser, wenn:

* Sie ein individuelles Feature benötigen.
* Sie Unterstützung bei der Nutzung des Produkts wünschen.
* Sie Bugs vertraulich melden und beheben lassen möchten.
* Sie Kontrolle über die Datensammlung bei Endanwendern haben möchten.
* Sie eine Anwendung ohne UI ausführen müssen.
* Sie Linux und macOS unterstützen möchten.
* Sie WPF-Controls über einem DRM-geschützten Video im Browser benötigen.
* Sie auf `window.print()`-Aufrufe der Seite reagieren oder Druckerfähigkeiten
  auslesen müssen.
* Sie Traffic in Hintergrund-Threads statt im UI-Thread abfangen müssen.

## Unterschiedliche Ansätze

WebView2 ist ein Control von Microsoft. Es ist kostenlos, aber – wie man es von
Microsoft erwartet – auch proprietär. Es ersetzt das alte, auf Trident
basierende WebView und setzt stattdessen auf Edge.

WebView2 ist ein Control: ein Eintrag in der Visual-Studio-Toolbox, Klassen aus
`Microsoft.Web.WebView2.Core.dll`. Es ist jedoch kein eigenständiges
Microsoft-Produkt wie Office oder Power BI. Der öffentliche Kanal für Fragen und
Bug-Reports ist ein GitHub-Repository, ohne garantierte Reaktionszeit.

DotNetBrowser ist ein Produkt von TeamDev, einem Unternehmen, das sich auf
Browser-Embedding spezialisiert hat. Angefangen haben wir 2004 mit Internet
Explorer, später mit Safari und WebKit – bis wir uns 2013 auf Chromium
festgelegt haben.

2015 haben wir DotNetBrowser eingeführt. Es ist ein kommerzielles Produkt, das
für den kommerziellen Einsatz entwickelt wurde. Neben der Software und der
Dokumentation umfasst das Angebot einen dedizierten Kundenbetreuer, technischen
[Support][getting-help] 
und [Premium-Services][premium-services].

## Unterschiede für Unternehmen

### Fixes, Features und Support

Wie bekommen Sie Hilfe, wenn Sie einen Bug finden oder ein Feature benötigen?
Werfen wir einen genaueren Blick darauf, was WebView2 und DotNetBrowser bieten.

WebView2 sammelt Feedback von der Öffentlichkeit in einem speziellen
GitHub-Repository. Wenn Sie etwas melden möchten, erstellen Sie dort ein Issue.
Wenn Microsoft-Entwickler Ihren Report für wichtig halten, übertragen sie ihn in
ihr internes System. Das erkennen Sie am Label „tracked“.

DotNetBrowser verfügt über ein privates Helpdesk-System, in dem Meldungen von
Kunden vertraulich bleiben. Die garantierte erste Reaktionszeit (SLA) beträgt
einen Geschäftstag.

Der technische Support umfasst: Hilfe bei der Nutzung des Produkts,
Unterstützung beim Troubleshooting, Bugfixes und die Berücksichtigung von
Feature-Requests. Alle Ihre Support-Anfragen werden direkt von
DotNetBrowser-Entwicklern bearbeitet.

### Privacy der Endanwender

Die WebView2 Runtime, die Endanwender installieren, hat eigene
Lizenzbedingungen. Sie erscheinen, wenn Sie auf Microsofts
[WebView2-Seite][webview2-download] auf einen Download-Button klicken. Zwei
Punkte könnten für Sie relevant sein:

1. Microsoft darf Informationen über Ihre Endanwender sammeln.
2. Mit den Standardeinstellungen sind Sie verpflichtet, die Anwender darüber zu
   informieren.

Abschnitt 3(a) der Lizenz besagt, dass die Software Informationen über Sie und
die Nutzung durch Ihre Endanwender erfassen und an Microsoft senden darf. Mit
der Nutzung der Software stimmen Sie dem zu.

Laut Abschnitt 3(b) ist Microsoft Defender SmartScreen standardmäßig aktiviert.
Solange es aktiviert ist, verpflichtet Abschnitt 9(a) Sie, Ihre Anwender darüber
zu informieren, dass Ihre Software SmartScreen enthält und deren Informationen
an Microsoft sendet. Sie deaktivieren es mit der Einstellung
`IsReputationCheckingRequired`.

Wenn Sie die Runtime mit Ihrer Anwendung ausliefern (Fixed-Version), sind das in
deren Bedingungen die Abschnitte 4(a), 4(b) und 8. Was WebView2 erfasst,
beschreibt Microsoft auf seiner [Datenschutzseite][webview2-privacy].

DotNetBrowser sammelt keine Informationen über Sie oder Ihre Endanwender.
Außerdem verhindert es die Datensammlung durch Google. Mehr dazu, wie
DotNetBrowser mit Daten umgeht und Ihnen Kontrolle über die Privatsphäre gibt,
finden Sie in
den [Privacy Practices][privacy-practices].

## Technische Unterschiede

Aus technischer Sicht unterscheiden sich DotNetBrowser und WebView2 nicht
grundlegend. Beide haben eine ähnliche Architektur, bei der Chromium in einem
separaten Prozess läuft. Beide haben Hunderte Features, von denen sich die
meisten überschneiden.

Die Unterschiede existieren jedoch – und sie können entscheidend sein, wenn Sie
die passende Lösung auswählen müssen. Dieser Vergleich beschreibt WebView2 mit
Stand [SDK 1.0.4258.31][webview2-sdk] (September 2026). Werfen wir einen
genaueren Blick darauf.

### Distribution und Deployment

Sie können WebView2 Runtime zusammen mit Ihrer Anwendung ausliefern oder die
Version nutzen, die beim Endanwender bereits installiert ist. Diese Modi heißen
Fixed-Version und Evergreen.

Im Fixed-Version-Mode kontrollieren Sie die Version von WebView2 in Ihrer
Anwendung – gut für Stabilität. Im Evergreen-Mode überlassen Sie Microsoft die
Logistik und Updates und reduzieren die Größe Ihrer Software.

DotNetBrowser muss mit Ihrer Anwendung ausgeliefert werden. Das ist der einzige
Distribution-Mode, den es out of the box gibt.

### Chrome extensions

Sowohl DotNetBrowser als auch WebView2 unterstützen Extensions. Während WebView2
nur sehr grundlegende Funktionen bereitstellt, gibt DotNetBrowser Entwicklern
mehr Optionen und volle Kontrolle über den Lebenszyklus und die Aktivitäten von
Extensions.

Seit [SDK 1.0.2210.55][webview2-sdk-extensions] (Dezember 2023) kann ein
WebView2-Entwickler [eine Extension][webview2-extensions] aus einem entpackten
Ordner installieren, die installierten Extensions auflisten, aktivieren oder
deaktivieren und entfernen. Eine Installation über den Chrome Web Store gibt es
nicht, ebenso wenig eine API für Icon, Badge oder Popup der Extension.

In DotNetBrowser kann ein Entwickler eine Extension direkt aus der CRX-Datei
installieren, programmatisch auf das Extension-Icon „klicken“, mit einem Popup
interagieren und neue „Tabs“ handhaben, die eine Extension öffnet.

Darüber hinaus können Sie Endanwendern erlauben, direkt mit Extensions zu
arbeiten:

* Nutzung über den Chrome Web Store.
* Anzeige des Extension-Icons mit Badges und Labels.
* Darstellung von Popups und Tabs, die durch die Extension geöffnet werden.

Lesen Sie mehr im [Guide zu Extensions][extensions-guide]
und [probieren Sie es praktisch aus][extensions-article].

### Betrieb ohne UI

Für Use Cases wie Automatisierung oder PDF-Generierung ist keine
Benutzeroberfläche erforderlich. Hier ist ein Headless Mode einfacher und
effizienter.

WebView2 hat keinen Headless Mode. Es benötigt ein Fenster, das auch verborgen
sein kann, und einen UI-Thread mit Message Loop – selbst in einer
Konsolenanwendung. In einem [Windows-Service][webview2-service] unterstützt
Microsoft WebView2 offiziell nicht. Rendern ohne Fenster, [Off-Screen
Rendering][webview2-osr], ist weiterhin ein offener Feature-Request.

DotNetBrowser läuft out of the box headless. Sie können es in einer
Konsolenanwendung, in einem Webserver oder sogar als Windows-Service nutzen. Zum
Beispiel so:

```cs
using (IEngine engine = EngineFactory.Create())
{
    using (IBrowser browser = engine.CreateBrowser())
    {
        browser.Navigation.LoadUrl("https://teamdev.com/dotnetbrowser").Wait();
    }
}
```

### Linux und macOS

Im Jahr 2024 hat Microsoft den Plan offiziell verworfen, WebView2 für
[macOS][webview2-macos] und [Linux][webview2-linux] zu unterstützen.

DotNetBrowser ist eine plattformübergreifende Bibliothek, die auf Windows, macOS
und Linux läuft. Nutzen Sie es mit 
[Avalonia UI][avalonia] 
oder in [Server-Anwendungen][console].

### WPF und überlappende Controls

WebView2 und DotNetBrowser können beide WPF-Elemente über den Browser legen.
WebView2 nutzt dafür ein zweites WPF-Control, DotNetBrowser einen
Rendering-Modus, der in jedem unterstützten UI-Toolkit funktioniert.

Mit dem Standard-Control von WebView2 geht das nicht. Es bettet ein fremdes
Fenster ein, und WPF unterstützt keine Überlappung zwischen Bereichen, die in
unterschiedlichen Fenstern gerendert werden. Elemente über dem Browser bleiben
unsichtbar.

Mit [SDK 1.0.2957.106][webview2-sdk-composition] (Januar 2025) kam in WebView2
[`WebView2CompositionControl`][webview2-composition] hinzu: ein Drop-in-Ersatz
für das Standard-Control, bei dem WPF-Elemente über dem Browser gezeichnet
werden können. Mehr dazu in [WebView2 in WPF-Apps][webview2-wpf].

Das Composition Control von WebView2 bettet kein Fenster ein. Es erfasst die
Ausgabe des Browsers als Bilder über eine Graphics-Capture-Session von Windows
und zeichnet sie selbst. Microsoft nennt zwei Nachteile: Die Framerate kann
niedriger sein als beim Standard-Control, und DRM-geschützte Videos werden nicht
angezeigt.

Außerhalb von WPF hat WebView2 kein solches Control. In WinForms ist es nicht
nötig: Ein Button oder jedes andere undurchsichtige Control wird über WebView2
und DotNetBrowser gleichermaßen gezeichnet. Bei einem transparenten Control
sieht es anders aus: In beiden zeigt es das Formular dahinter, nicht die Seite.

Win32-Apps können den Visual Hosting Mode von WebView2 nutzen und den Browser in
ihre eigene UI einbinden. In WinUI 3 ist WebView2 [External
Content][winui-visual-layer]. XAML-Elemente können darüber liegen, aber dahinter
scheint nichts durch, sodass der Hintergrund des Browsers nicht transparent sein
kann.

DotNetBrowser hat zwei [Rendering-Modi][browser-view-rendering]. Im Off-Screen
Rendering Mode werden die gerenderten Pixel in den Speicher des .NET-Prozesses
kopiert und von einem regulären Control gezeichnet. So können Controls von WPF,
WinForms, WinUI 3 und Avalonia den Browser überlappen. In diesem Modus läuft
DRM-geschütztes Video (Widevine) und bleibt sichtbar, wie der Screenshot unten
zeigt.

Auch in DotNetBrowser senkt Off-Screen Rendering die Framerate. Der
hardwarebeschleunigte Modus bettet ein natives Fenster ein und hat daher
dieselbe Einschränkung bei Überlappungen wie das Standard-Control von WebView2.

![Eine Leiste mit WPF-Controls über einem Widevine-geschützten Video im Off-Screen Rendering Mode von DotNetBrowser](https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-oder-webview2-deutsch/wpf-controls-over-drm-video.webp)
<p class="image-caption">WPF-Controls über einem Widevine-geschützten Video im Off-Screen Rendering Mode. Sintel &copy; Blender Foundation | <a href="https://durian.blender.org/">durian.blender.org</a>, <a href="https://creativecommons.org/licenses/by/3.0/">CC BY 3.0</a>.</p>

### JavaScript aus .NET aufrufen

In beiden Lösungen können Sie JavaScript direkt aus .NET-Code ausführen. Der
Unterschied liegt darin, was passiert, wenn das Ergebnis von Chromium zurück in
die .NET-Welt übertragen wird.

WebView2 konvertiert das Ergebnis zu JSON:

```cs
string result = await coreWebView2.ExecuteScriptAsync(@"'example'");
Debug.Assert(result == "\"example\"");
```

Seit [SDK 1.0.2277.86][webview2-sdk-script] (Februar 2024) kann
`ExecuteScriptWithResultAsync` von WebView2 das Ergebnis als einfachen String
statt als JSON liefern und Script-Exceptions melden. Eine Referenz auf ein
JavaScript-Objekt kann es aber weiterhin nicht zurückgeben.

DotNetBrowser konvertiert automatisch 
[einfache Typen][js-to-net]. Komplexe Typen
werden durch Proxies für die tatsächlichen V8-Objekte ersetzt:

```cs
string title = await browser.MainFrame.ExecuteJavaScript<string>("document.title");
IJsObject window = await browser.MainFrame.ExecuteJavaScript<IJsObject>("window");

// Or just use dynamic types.
dynamic document = browser.MainFrame.ExecuteJavaScript("document").Result;
document.write("Hello world!");
```

### .NET aus JavaScript aufrufen

Beide Lösungen erlauben es, .NET-Objekte in JavaScript verfügbar zu machen –
jeweils mit einem Haken.

In WebView2 gelangt das Objekt über COM nach JavaScript, daher funktionieren nur
Typen, die COM verarbeiten kann. Eine einfache Klasse, ein Array oder ein
WPF-Button wird akzeptiert; beim Hinzufügen einer `List<string>` oder eines
WinForms-Buttons wirft WebView2 dagegen eine Exception. Außerdem können Seite
und App bei WebView2 Web Messages austauschen, eine Nachricht transportiert aber
nur einen String oder JSON: JavaScript erhält eine Kopie der Daten, kein
aufrufbares Objekt.

In DotNetBrowser können Sie [beliebige Objekte injizieren][javascript], auch die
`List<string>` und den WinForms-Button, die WebView2 abgelehnt hat. In
JavaScript haben Sie Zugriff auf die öffentlichen Member und indizierten
Properties des injizierten Objekts. Aufrufe aus JavaScript laufen in
Hintergrund-Threads; auf UI-Controls greifen Sie daher über den UI-Thread zu:
`Dispatcher` in WPF, `Invoke` in WinForms.

### Netzwerk-Intercepting

WebView2 und DotNetBrowser fangen beide Traffic ab. WebView2 tut das im
UI-Thread. DotNetBrowser tut es in Hintergrund-Threads.

WebView2 hat das Event [`WebResourceRequested`][webview2-intercept]. In dessen
Handler können Sie URL, Methode, Header oder Body des Requests ändern oder eine
eigene Response zurückgeben. Für Inhalte, die Sie so zurückgeben, werden keine
Source Maps geladen. Mit dem Event `WebResourceResponseReceived` können Sie die
Response einsehen, aber nicht ändern.

`WebResourceRequested` feuert nur für Requests, die zu einem registrierten
Filter passen: einem URL-Muster plus einem Ressourcentyp. Seit [SDK
1.0.2365.46][webview2-sdk-filter] (Februar 2024) kann ein Filter auch Requests
von Service Workern, Shared Workern und Cross-Origin-iframes erfassen. Die
ältere [Filter-Überladung][webview2-filter] mit zwei Argumenten ist deprecated,
weil sie diese iframes nicht erfasst.

WebView2 löst das Event im [UI-Thread][webview2-local-content] der App aus. Ein
Handler, der drei Sekunden blockiert, lässt das Fenster einfrieren und verzögert
das Laden der Seite um drei Sekunden. Der Handler kann `GetDeferral()` aufrufen
und die Arbeit in asynchronem Code beenden, der Request wartet aber, bis Sie das
Deferral abschließen.

DotNetBrowser hat für jeden Schritt eines Requests einen Handler sowie Events
für die Response. Damit können Sie:

* [HTTP-Requests filtern][navigation-filtering].
* [HTTP-Requests umleiten][before-url-request].
* [HTTP-Request-][before-start-transaction]
  und [Response-Header][receive-headers] überschreiben.
* [Upload-Daten überschreiben][before-upload].
* [Cookies filtern][suppress-cookies].
* Requests authentifizieren.
* Zertifikate prüfen.
* Events für den Beginn der Response, die empfangenen Bytes und den Abschluss
  erhalten.

Um in DotNetBrowser eigene Responses zurückzugeben, registrieren Sie beim
Erstellen der Engine einen [Handler pro Scheme][engine-scheme], auch für
`https`. Jeder Request dieses Schemes erreicht ihn, eine Filterliste müssen Sie
also nicht pflegen.

Weitere Beispiele für Networking mit DotNetBrowser finden Sie in unserem
[GitHub][examples-network].

### Printing API

WebView2 und DotNetBrowser haben beide eine Druck-API. Der Unterschied liegt
darin, wer die Kontrolle hat, wenn die Seite `window.print()` aufruft.

Seit [SDK 1.0.1518.46][webview2-sdk-print] (Januar 2023) druckt WebView2 mit
[`PrintAsync`][webview2-print] und
[`CoreWebView2PrintSettings`][webview2-print-settings] auf einen bestimmten
Drucker. Es druckt außerdem nach PDF – wahlweise in eine Datei oder in einen
Stream. Die Einstellungen umfassen Druckername, Seitenbereiche, Kopien, Duplex,
Sortierung, Farbmodus, Papierformat, Seiten pro Blatt, Ränder, Kopf- und
Fußzeile. `ShowPrintUI` öffnet die Druckvorschau von WebView2 oder den
Druckdialog des Systems.

Was WebView2 fehlt, ist eine API, um die Fähigkeiten eines Druckers wie
Papierformate oder Duplex auszulesen. Diese fragen Sie selbst beim System ab.

Ruft das JavaScript der Seite `window.print()` auf, öffnet WebView2 seine
Druckvorschau, und es gibt kein Event, um das abzufangen. Ein Workaround ist,
`window.print` durch eine eigene Funktion zu ersetzen, die der App eine
Nachricht sendet.

In DotNetBrowser empfängt `RequestPrintHandler` Druck-Requests aus .NET und aus
JavaScript. In diesem Handler entscheiden Sie, ob Sie den Request abbrechen, die
Druckvorschau anzeigen oder ohne Dialog drucken.

Wenn gedruckt wird, läuft danach je nach Inhalt `PrintHtmlContentHandler` oder
`PrintPdfContentHandler`. Darin können Sie:

* Einen Drucker auswählen.
* Die Fähigkeiten des Druckers auslesen: Papierformate, Farbmodelle,
  Duplex-Modi und Kopien.
* Seitenbereiche, Papierformat, Ränder sowie Kopf- und Fußzeilen konfigurieren.

DotNetBrowser hat außerdem einen eingebauten PDF-Drucker. Mehr dazu im
[Printing Guide][printing].

## Kostenlos ausprobieren

Holen Sie sich Ihre kostenlose Lizenz und wählen Sie einen unserer Quickstarts. 



Es dauert 5 Minuten, um mit DotNetBrowser zu starten:

* [DotNetBrowser in WPF][wpf]
* [DotNetBrowser in Avalonia][avalonia]
* [DotNetBrowser in WinForms][winforms]
* [DotNetBrowser in der Konsole][console] – nützlich für Windows-Services 
  und Server-Anwendungen.

[extensions-article]: https://teamdev.com/dotnetbrowser/blog/chrome-extensions-in-dotnetbrowser/
[extensions-guide]: https://teamdev.com/dotnetbrowser/docs/guides/gs/extensions/
[dotnetbrowser-vs-cefsharp-article]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-or-cefsharp/
[privacy]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-oder-webview2-deutsch/#privacy-der-endanwender
[support]: https://teamdev.com/dotnetbrowser/blog/dotnetbrowser-oder-webview2-deutsch/#fixes-features-und-support
[migration-guide]: https://teamdev.com/dotnetbrowser/blog/from-webview2-to-dotnetbrowser-part-1/
[getting-help]: https://teamdev.com/dotnetbrowser/#getting-help
[premium-services]: https://teamdev.com/dotnetbrowser/#getting-help
[privacy-practices]: https://teamdev.com/dotnetbrowser/docs/guides/privacy/
[javascript]: https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/
[navigation-filtering]: https://teamdev.com/dotnetbrowser/docs/guides/gs/navigation/#filtering-resources
[before-url-request]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#before-url-request
[before-start-transaction]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#before-start-transaction
[receive-headers]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#receive-headers
[before-upload]: https://teamdev.com/dotnetbrowser/docs/guides/gs/network/#before-send-upload-data
[suppress-cookies]: https://teamdev.com/dotnetbrowser/docs/guides/gs/cookies/#suppressing-cookies
[examples-network]: https://github.com/TeamDev-IP/DotNetBrowser-Examples#network
[wpf]: https://teamdev.com/dotnetbrowser/docs/quickstart/wpf/
[avalonia]: https://teamdev.com/dotnetbrowser/docs/quickstart/avalonia/
[winforms]: https://teamdev.com/dotnetbrowser/docs/quickstart/winforms/
[console]: https://teamdev.com/dotnetbrowser/docs/quickstart/console/
[js-to-net]: https://teamdev.com/dotnetbrowser/docs/guides/gs/javascript/#javascript-to-net
[browser-view-rendering]: https://teamdev.com/dotnetbrowser/docs/guides/gs/browser-view/#rendering
[webview2-service]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/3458
[webview2-osr]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/547
[webview2-macos]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/1314
[webview2-linux]: https://github.com/MicrosoftEdge/WebView2Feedback/issues/645
[engine-scheme]: https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#intercept-request-per-uri-scheme
[printing]: https://teamdev.com/dotnetbrowser/docs/guides/gs/printing/
[webview2-download]: https://developer.microsoft.com/microsoft-edge/webview2/
[webview2-privacy]: https://learn.microsoft.com/microsoft-edge/webview2/concepts/data-privacy
[webview2-sdk]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-4258-31
[webview2-extensions]: https://learn.microsoft.com/dotnet/api/microsoft.web.webview2.core.corewebview2profile.addbrowserextensionasync
[webview2-sdk-extensions]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-2210-55
[webview2-wpf]: https://learn.microsoft.com/microsoft-edge/webview2/platforms/wpf
[webview2-composition]: https://learn.microsoft.com/dotnet/api/microsoft.web.webview2.wpf.webview2compositioncontrol
[winui-visual-layer]: https://learn.microsoft.com/windows/apps/develop/composition/visual-layer#differences-from-uwp
[webview2-intercept]: https://learn.microsoft.com/microsoft-edge/webview2/how-to/webresourcerequested
[webview2-filter]: https://learn.microsoft.com/dotnet/api/microsoft.web.webview2.core.corewebview2.addwebresourcerequestedfilter
[webview2-local-content]: https://learn.microsoft.com/microsoft-edge/webview2/concepts/working-with-local-content
[webview2-print]: https://learn.microsoft.com/microsoft-edge/webview2/how-to/print
[webview2-sdk-print]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-1518-46
[webview2-sdk-script]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-2277-86
[webview2-sdk-filter]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-2365-46
[webview2-sdk-composition]: https://learn.microsoft.com/microsoft-edge/webview2/release-notes/sdk/1-0-2957-106
[webview2-print-settings]: https://learn.microsoft.com/dotnet/api/microsoft.web.webview2.core.corewebview2printsettings
