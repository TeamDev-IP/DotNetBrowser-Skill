
# Context menu

**Lead**
This article describes how to work with the context menu.


By default, the context menu is suppressed for the `IBrowser` instance. If an `IBrowserView` instance is initialized from the IBrowser instance that does not have custom context menu handling, the default context menu handler is registered. The items shown in the default context menu depend on the web page item that was right-clicked, however, in most cases it contains the following items: "Back", "Forward", "Reload", "Print" and "View page source".

**Note**
The default context menu implementation cannot be modified. If you need to add or remove some items, you should create and register your own implementation of the context menu handler.


## Custom context menu

To build a custom context menu, the `IBrowser.ShowContextMenuHandler` handler should be used.

### WinForms


**C#**

```csharp
browser.ShowContextMenuHandler =
    new AsyncHandler<ShowContextMenuParameters, ShowContextMenuResponse
    >(ShowMenu);
```

**VB**

```vb
browser.ShowContextMenuHandler =
    New AsyncHandler(
        Of ShowContextMenuParameters, ShowContextMenuResponse)(
            AddressOf ShowMenu)
```




**C#**

```csharp
private ToolStripItem BuildMenuItem(string item, bool isEnabled,
                                    EventHandler clickHandler)
{
    ToolStripItem result = new ToolStripMenuItem
    {
        Text = item,
        Enabled = isEnabled
    };
    result.Click += clickHandler;

    return result;
}

private Task<ShowContextMenuResponse> ShowMenu(ShowContextMenuParameters parameters)
{
    TaskCompletionSource<ShowContextMenuResponse> tcs =
        new TaskCompletionSource<ShowContextMenuResponse>();

    SpellCheckMenu spellCheckMenu = parameters.SpellCheckMenu;
    if (spellCheckMenu != null)
    {
        BeginInvoke(new Action(() =>
        {
            ContextMenuStrip popupMenu = new ContextMenuStrip();
            if(!string.IsNullOrEmpty(parameters.LinkText))
            {
                ToolStripItem buildMenuItem =
                    BuildMenuItem("Show the URL link", true,
                                  (sender, args) =>
                                  {
                                      string linkURL = parameters.LinkUrl;
                                      Console.WriteLine($"linkURL = {linkURL}");
                                      MessageBox.Show(linkURL, "URL");
                                      tcs.TrySetResult(ShowContextMenuResponse.Close());
                                  });
                popupMenu.Items.Add(buildMenuItem);
            }

            ToolStripItem reloadMenuItem =
                BuildMenuItem("Reload", true, 
                              (sender, args) =>
                              {
                                  Console.WriteLine("Reload current web page");
                                  browser.Navigation.Reload();
                                  tcs.TrySetResult(ShowContextMenuResponse.Close());
                              });
            popupMenu.Items.Add(reloadMenuItem);

            // Close context menu when the browser requests focus back.
            EventHandler<FocusRequestedEventArgs> onFocusRequested = null;
            onFocusRequested = (sender, args) =>
            {
                BeginInvoke((Action) (() => popupMenu.Close()));
                parameters.Browser.FocusRequested -= onFocusRequested;
            };
            parameters.Browser.FocusRequested += onFocusRequested;

            // Handle the menu closed event.
            ToolStripDropDownClosedEventHandler menuOnClosed = null;
            menuOnClosed = (sender, args) =>
            {
                bool itemNotClicked =
                    args.CloseReason != ToolStripDropDownCloseReason.ItemClicked;
                if (itemNotClicked)
                {
                    tcs.TrySetResult(ShowContextMenuResponse.Close());
                }

                parameters.Browser.FocusRequested -= onFocusRequested;
                popupMenu.Closed -= menuOnClosed;
            };
            popupMenu.Closed += menuOnClosed;

            // Show the context menu.
            Point location = new Point(parameters.Location.X, parameters.Location.Y);
            popupMenu.Show(this, location);
            tcs.TrySetResult(ShowContextMenuResponse.Close());
        }));
    }
    else
    {
        tcs.TrySetResult(ShowContextMenuResponse.Close());
    }

    return tcs.Task;
}
```

**VB**

```vb
Private Function BuildMenuItem(item As String, isEnabled As Boolean,
                               clickHandler As EventHandler) As ToolStripItem
    Dim result As ToolStripItem = New ToolStripMenuItem With {
            .Text = item,
            .Enabled = isEnabled
            }
    AddHandler result.Click, clickHandler

    Return result
End Function

Private Function ShowMenu(parameters As ShowContextMenuParameters) _
    As Task(Of ShowContextMenuResponse)
    Dim tcs As New TaskCompletionSource(Of ShowContextMenuResponse)()
    Dim spellCheckMenu As SpellCheckMenu = parameters.SpellCheckMenu

    If spellCheckMenu IsNot Nothing Then
        BeginInvoke(New Action(Sub()
            Dim popupMenu As New ContextMenuStrip()
            If Not String.IsNullOrEmpty(parameters.LinkText) Then
                Dim menuItem As ToolStripItem =
                    BuildMenuItem("Show the URL link", True, Sub(sender, args)
                        Dim linkURL As String = parameters.LinkUrl
                        Console.WriteLine($"linkURL = {linkURL}")
                        MessageBox.Show(linkURL, "URL")
                        tcs.TrySetResult(ShowContextMenuResponse.Close())
                    End Sub)
                popupMenu.Items.Add(menuItem)
            End If

            Dim reloadMenuItem As ToolStripItem =
                BuildMenuItem("Reload", True, Sub(sender, args)
                    Console.WriteLine("Reload current web page")
                    browser.Navigation.Reload()
                    tcs.TrySetResult(ShowContextMenuResponse.Close())
                End Sub)
            popupMenu.Items.Add(reloadMenuItem)

            ' Close context menu when the browser requests focus back.
            Dim onFocusRequested As EventHandler(Of FocusRequestedEventArgs) = Nothing
            onFocusRequested = Sub(sender, args)
                BeginInvoke(CType(Sub() popupMenu.Close(), Action))
                RemoveHandler parameters.Browser.FocusRequested, onFocusRequested
            End Sub
            AddHandler parameters.Browser.FocusRequested, onFocusRequested

            ' Handle the menu closed event.
            Dim menuOnClosed As ToolStripDropDownClosedEventHandler = Nothing
            menuOnClosed = Sub(sender, args)
                Dim itemNotClicked As Boolean = 
                        args.CloseReason <>
                        ToolStripDropDownCloseReason.ItemClicked

                If itemNotClicked Then
                    tcs.TrySetResult(ShowContextMenuResponse.Close())
                End If

                RemoveHandler parameters.Browser.FocusRequested, onFocusRequested
                RemoveHandler popupMenu.Closed, menuOnClosed
            End Sub
            AddHandler popupMenu.Closed, menuOnClosed

            ' Show the context menu.
            Dim location As New Point(parameters.Location.X, parameters.Location.Y)
            popupMenu.Show(Me, location)
            tcs.TrySetResult(ShowContextMenuResponse.Close())
        End Sub))
    Else
        tcs.TrySetResult(ShowContextMenuResponse.Close())
    End If

    Return tcs.Task
End Function
```



The complete example is available in our repository: [C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/csharp/winforms/ContextMenu), [VB.NET](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/vbnet/winforms/ContextMenu)

### WPF


**C#**

```csharp
browser.ShowContextMenuHandler =
    new AsyncHandler<ShowContextMenuParameters, 
                     ShowContextMenuResponse>(ShowContextMenu);
```

**VB**

```vb
browser.ShowContextMenuHandler =
    New AsyncHandler(Of ShowContextMenuParameters, ShowContextMenuResponse )(
        AddressOf ShowContextMenu)
```




**C#**

```csharp
private Task<ShowContextMenuResponse> ShowContextMenu(
    ShowContextMenuParameters parameters)
{
    TaskCompletionSource<ShowContextMenuResponse> tcs =
        new TaskCompletionSource<ShowContextMenuResponse>();

    WebView.Dispatcher?.BeginInvoke(new Action(() =>
    {
        System.Windows.Controls.ContextMenu popupMenu =
            new System.Windows.Controls.ContextMenu();

        if (!string.IsNullOrEmpty(parameters.LinkText))
        {
            MenuItem buildMenuItem =
                BuildMenuItem("Show the URL link", true,
                              Visibility.Visible,
                              (sender, args) =>
                              {
                                  string linkURL = parameters.LinkUrl;
                                  Console.WriteLine($"linkURL = {linkURL}");
                                  MessageBox.Show(linkURL, "URL");
                                  tcs.TrySetResult(ShowContextMenuResponse.Close());
                              });
            popupMenu.Items.Add(buildMenuItem);
        }

        MenuItem reloadMenuItem =
            BuildMenuItem("Reload", true, Visibility.Visible,
                          (sender, args) =>
                          {
                              Console.WriteLine("Reload current web page");
                              browser.Navigation.Reload();
                              tcs.TrySetResult(ShowContextMenuResponse.Close());
                          });
        popupMenu.Items.Add(reloadMenuItem);

        popupMenu.Closed += (sender, args) =>
        {
            tcs.TrySetResult(ShowContextMenuResponse.Close());
        };

        popupMenu.IsOpen = true;
    }));

    return tcs.Task;
}
```

**VB**

```vb
Private Function ShowContextMenu(parameters As ShowContextMenuParameters) _
    As Task(Of ShowContextMenuResponse)
    Dim tcs As New TaskCompletionSource(Of ShowContextMenuResponse)()
    WebView.Dispatcher?.BeginInvoke(New Action(Sub()
        Dim popupMenu As New ContextMenu()

        If Not String.IsNullOrEmpty(parameters.LinkText) Then
            Dim linkMenuItem As MenuItem =
                    BuildMenuItem("Show the URL link", True,
                                  Visibility.Visible,
                                  Sub(sender, args)
                                      Dim linkUrl As String = parameters.LinkUrl
                                      Debug.WriteLine( $"linkURL = {linkUrl}")
                                      MessageBox.Show(linkUrl,"URL")
                                      tcs.TrySetResult(ShowContextMenuResponse.Close())
                                  End Sub)
            popupMenu.Items.Add(linkMenuItem)
        End If

        Dim reloadMenuItem As MenuItem =
                BuildMenuItem("Reload", True, Visibility.Visible,
                              Sub(sender, args)
                                  Debug.WriteLine("Reload current web page")
                                  browser.Navigation.Reload()
                                  tcs.TrySetResult(ShowContextMenuResponse.Close())
                              End Sub)
        popupMenu.Items.Add(reloadMenuItem)
        AddHandler popupMenu.Closed, Sub(sender, args)
            tcs.TrySetResult(ShowContextMenuResponse.Close())
        End Sub
        popupMenu.IsOpen = True
    End Sub))
    Return tcs.Task
End Function
```



The complete example is available in our repository: [C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/csharp/wpf/ContextMenu), [VB.NET](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/vbnet/wpf/ContextMenu)

### Avalonia UI


```csharp
browser.ShowContextMenuHandler =
    new AsyncHandler<ShowContextMenuParameters,
        ShowContextMenuResponse>(ShowContextMenu);
```


```csharp
private Task<ShowContextMenuResponse> ShowContextMenu(
    ShowContextMenuParameters parameters)
{
    TaskCompletionSource<ShowContextMenuResponse> tcs =
        new TaskCompletionSource<ShowContextMenuResponse>();

    Dispatcher.UIThread.InvokeAsync(() =>
    {
        Avalonia.Controls.ContextMenu? cm = new();
        cm.Placement = PlacementMode.AnchorAndGravity;
        cm.PlacementAnchor = PopupAnchor.TopLeft;
        cm.PlacementGravity = PopupGravity.BottomRight;
        cm.HorizontalOffset = parameters.Location.X;
        cm.VerticalOffset = parameters.Location.Y;

        if (!string.IsNullOrEmpty(parameters.LinkText))
        {
            MenuItem buildMenuItem =
                BuildMenuItem("Show the URL link", true, true,
                              async (sender, args) =>
                              {
                                  string linkURL = parameters.LinkUrl;
                                  Console.WriteLine($"linkURL = {linkURL}");
                                  var box =
                                      MessageBoxManager
                                         .GetMessageBoxStandard("URL", linkURL);
                                  var result = await box.ShowAsync();
                                  tcs.TrySetResult(ShowContextMenuResponse.Close());
                              });
            cm.Items.Add(buildMenuItem);
        }

        MenuItem reloadMenuItem =
            BuildMenuItem("Reload", true, true,
                          (sender, args) =>
                          {
                              Console.WriteLine("Reload current web page");
                              browser.Navigation.Reload();
                              tcs.TrySetResult(ShowContextMenuResponse.Close());
                          });
        cm.Items.Add(reloadMenuItem);

        // Close context menu when the browser requests focus back.
        EventHandler<FocusRequestedEventArgs> onFocusRequested = null;
        onFocusRequested = (sender, args) =>
        {
            Dispatcher.UIThread.InvokeAsync(() => cm.Close());
            browser.FocusRequested -= onFocusRequested;
        };
        browser.FocusRequested += onFocusRequested;

        cm.Closed += (sender, args) =>
        {
            browser.FocusRequested -= onFocusRequested;
            browser.Focus();
            tcs.TrySetResult(ShowContextMenuResponse.Close());
        };

        cm.Open(BrowserView);
    });

    return tcs.Task;
}
```


The complete example is available in our repository: [C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/csharp/avalonia/ContextMenu)

## Disable context menu

To supress the context menu completely, the following code should be used:


**C#**
```csharp
browser.ShowContextMenuHandler =
     new Handler<ShowContextMenuParameters, ShowContextMenuResponse>(p =>
    {
        return ShowContextMenuResponse.Close();
    });
```

**VB**
```vb
browser.ShowContextMenuHandler = 
    New Handler(Of ShowContextMenuParameters, ShowContextMenuResponse)(Function(p)
        Return ShowContextMenuResponse.Close()
    End Function)
```


