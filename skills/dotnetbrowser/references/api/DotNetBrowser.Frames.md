# <a id="DotNetBrowser_Frames"></a> Namespace DotNetBrowser.Frames

### Namespaces

 [DotNetBrowser.Frames.Handlers](DotNetBrowser.Frames.Handlers.md)

### Classes

 [EditorCommand](DotNetBrowser.Frames.EditorCommand.md)

Provides the supported commands that can be executed in a <xref href="DotNetBrowser.Frames.IFrame" data-throw-if-not-resolved="false"></xref>.

 [WebStorageException](DotNetBrowser.Frames.WebStorageException.md)

Thrown by <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> properties and  methods to indicate that the requested operation failed. This
is a superclass of the exceptions that can be thrown during working with <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref>.

 [WebStorageOverflowException](DotNetBrowser.Frames.WebStorageOverflowException.md)

Thrown by <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> indexer if the new value size exceeds the
available space in the storage.

 [WebStorageSecurityException](DotNetBrowser.Frames.WebStorageSecurityException.md)

Thrown by <xref href="DotNetBrowser.Frames.IWebStorage" data-throw-if-not-resolved="false"></xref> methods if the access to the web storage is forbidden for the
current document.

### Interfaces

 [IFrame](DotNetBrowser.Frames.IFrame.md)

Represents a frame in the browser.
Each web page loaded in the browser has a main(top-level) frame. The frame itself may have child
frames. When a web page is unloaded, its frame and all child frames are closed automatically.

 [IWebStorage](DotNetBrowser.Frames.IWebStorage.md)

<p>An HTML WebStorage.</p>
<p>
    Provides access to the session storage or local storage for a particular document on the loaded
    web page. Allows you to add, modify, or delete the stored items.
</p>

