# <a id="DotNetBrowser_Cast_IMediaReceivers"></a> Interface IMediaReceivers

Namespace: [DotNetBrowser.Cast](DotNetBrowser.Cast.md)  
Assembly: DotNetBrowser.dll  

The service that allows observing media <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receivers in the environment.

```csharp
public interface IMediaReceivers
```

## Properties

### <a id="DotNetBrowser_Cast_IMediaReceivers_AllAvailable"></a> AllAvailable

Gets the list of connected (not <xref href="DotNetBrowser.Cast.MediaReceiverState.Unavailable" data-throw-if-not-resolved="false"></xref> unavailable)
media receivers.

<p>
    The initial list of media receivers can be empty or not full. This is because receivers
    are <xref href="DotNetBrowser.Cast.Events.MediaReceiverDiscoveredEventArgs" data-throw-if-not-resolved="false"></xref> discovered asynchronously in Chromium.
</p>

```csharp
IReadOnlyList<IMediaReceiver> AllAvailable { get; }
```

#### Property Value

 [IReadOnlyList](https://learn.microsoft.com/dotnet/api/system.collections.generic.ireadonlylist\-1)<[IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)\>

## Methods

### <a id="DotNetBrowser_Cast_IMediaReceivers_Refresh"></a> Refresh\(\)

Asynchronously updates the list of available media receivers.

<p>
    This method forces Chromium to discover media receivers available in the local network.
    Use it before calling the <xref href="DotNetBrowser.Cast.IMediaReceivers.RetrieveAsync(System.Predicate%7bDotNetBrowser.Cast.IMediaReceiver%7d%2cSystem.TimeSpan)" data-throw-if-not-resolved="false"></xref>
    method to shorten the time to discover new receivers.
</p>

```csharp
void Refresh()
```

### <a id="DotNetBrowser_Cast_IMediaReceivers_RetrieveAsync_System_Predicate_DotNetBrowser_Cast_IMediaReceiver__System_TimeSpan_"></a> RetrieveAsync\(Predicate<IMediaReceiver\>, TimeSpan\)

Waiting till the first receiver matching the <code>predicate</code> is discovered.

```csharp
Task<IMediaReceiver> RetrieveAsync(Predicate<IMediaReceiver> predicate, TimeSpan timeout)
```

#### Parameters

`predicate` [Predicate](https://learn.microsoft.com/dotnet/api/system.predicate\-1)<[IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)\>

The predicated media receiver.

`timeout` [TimeSpan](https://learn.microsoft.com/dotnet/api/system.timespan)

The predefined timeout.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)\>

The task that can be used to wait for completion and obtain the result with
the first discovered receiver matching the <code>predicate</code>.

#### Remarks

<p>
    If a matching receiver has already been discovered, returns it immediately.
</p>
<p>
    Example of usage:
</p>

<pre><code class="lang-csharp">browser.Cast.StartPresentationHandler =
    new AsyncHandler&lt;StartPresentationParameters, StartPresentationResponse&gt;(async p =&gt;
    {
        IMediaReceiver mediaReceiver
            = await p.MediaReceivers
                     .RetrieveAsync(receiver =&gt; receiver.Name.Contains("Samsung TV"), timeout);
        return StartPresentationResponse.Start(mediaReceiver);
    });</code></pre>

#### Exceptions

 [ReceiverNotDiscoveredException](DotNetBrowser.Cast.ReceiverNotDiscoveredException.md)

When the receiver has not been discovered within <code>timeout</code>.

### <a id="DotNetBrowser_Cast_IMediaReceivers_RetrieveAsync_System_Predicate_DotNetBrowser_Cast_IMediaReceiver__"></a> RetrieveAsync\(Predicate<IMediaReceiver\>\)

Waiting till the first receiver matching the <code>predicate</code> is discovered.

```csharp
Task<IMediaReceiver> RetrieveAsync(Predicate<IMediaReceiver> predicate)
```

#### Parameters

`predicate` [Predicate](https://learn.microsoft.com/dotnet/api/system.predicate\-1)<[IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)\>

The predicated media receiver.

#### Returns

 [Task](https://learn.microsoft.com/dotnet/api/system.threading.tasks.task\-1)<[IMediaReceiver](DotNetBrowser.Cast.IMediaReceiver.md)\>

The task that can be used to wait for completion and obtain the result with
the first discovered receiver matching the <code>predicate</code>.

#### Remarks

<p>
    If a matching receiver has already been discovered, returns it immediately.
</p>
<p>
    Example of usage:
</p>

<pre><code class="lang-csharp">browser.Cast.StartPresentationHandler =
    new AsyncHandler&lt;StartPresentationParameters, StartPresentationResponse&gt;(async p =&gt;
    {
        IMediaReceiver mediaReceiver
            = await p.MediaReceivers
                     .RetrieveAsync(receiver =&gt; receiver.Name.Contains("Samsung TV"));
        return StartPresentationResponse.Start(mediaReceiver);
    });</code></pre>

#### Exceptions

 [ReceiverNotDiscoveredException](DotNetBrowser.Cast.ReceiverNotDiscoveredException.md)

When the receiver has not been discovered within 45 seconds.

### <a id="DotNetBrowser_Cast_IMediaReceivers_Discovered"></a> Discovered

Occurs when a new media <xref href="DotNetBrowser.Cast.IMediaReceiver" data-throw-if-not-resolved="false"></xref> receiver has been discovered in
the environment.

```csharp
event EventHandler<MediaReceiverDiscoveredEventArgs> Discovered
```

#### Event Type

 [EventHandler](https://learn.microsoft.com/dotnet/api/system.eventhandler\-1)<[MediaReceiverDiscoveredEventArgs](DotNetBrowser.Cast.Events.MediaReceiverDiscoveredEventArgs.md)\>

