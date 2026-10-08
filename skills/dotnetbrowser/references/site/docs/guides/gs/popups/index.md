
# Pop-ups

**Lead**
This page describes how to work with pop-ups, display or suppress them.


## Overview

Any web page can display pop-up windows using one of the following ways:

1. The `window.open()` JavaScript function. For example:

   ```js
   window.open("https://www.google.com", "_blank", 
       "resizable=yes, top=500, left=500, width=400, height=400");
   ```

2. A link with the `target` attribute:

   ```html
   <a href="https://www.google.com" target="_blank">Open Google</a>
   ```

**Note**
By default, all pop-ups are suppressed for the `IBrowser` instance. If an `IBrowserView` instance is initialized from the `IBrowser` instance that does not have custom pop-up handling, the default popup handler is registered. The pop-ups are displayed in a separate Window or Form.


## Opening pop-ups

To change the default behavior and take control over creation of pop-ups, use the `CreatePopupHandler` and `OpenPopupHandler` handlers.

The `CreatePopupHandler` handler is invoked when the engine wants to know whether pop-up can be created or not. The following code sample shows how to allow creating a pop-up:


**C#**
```csharp
browser.CreatePopupHandler =
    new Handler<CreatePopupParameters, CreatePopupResponse>(p =>
    {
        return CreatePopupResponse.Create();
    });
```

**VB**
```vb
browser.CreatePopupHandler = 
    New Handler(Of CreatePopupParameters, CreatePopupResponse)(Function(p)
        Return CreatePopupResponse.Create()
    End Function)
```



If the `CreatePopupHandler` handler allows you to create a pop-up, the `OpenPopupHandler` handler is invoked. In this handler, you can access the created pop-up and display it if necessary. See the code sample below:


**C#**
```csharp
browser.OpenPopupHandler = 
    new Handler<OpenPopupParameters>(p =>
    {
        // Access the created popup browser.
        IBrowser popup = p.PopupBrowser;
    });
```

**VB**
```vb
browser.OpenPopupHandler = 
    New Handler(Of OpenPopupParameters)(Sub(p)
        ' Access the created popup browser.
        Dim popup As IBrowser = p.PopupBrowser
    End Sub)
```



**Note**
The `popup` instance in the sample above does not have any web page loaded at the time the handler is invoked. The web page will be loaded later. At the moment, you can register all required event listeners and handlers, but you cannot access DOM or JavaScript, because the `popup` does not have a `IFrame` yet.


## Suppressing pop-ups

To suppress pop-ups, use the following approach:


**C#**
```csharp
browser.CreatePopupHandler =
    new Handler<CreatePopupParameters, CreatePopupResponse>(p =>
    {
        return CreatePopupResponse.Suppress();
    });
```

**VB**
```vb
browser.CreatePopupHandler = 
    New Handler(Of CreatePopupParameters, CreatePopupResponse)(Function(p)
        Return CreatePopupResponse.Suppress()
    End Function)
```



### Loading pop-up URL into the main browser

To suppress creating a separate pop-up and load the pop-up URL into the main browser, use the following approach:


**C#**
```csharp
browser.CreatePopupHandler =
    new Handler<CreatePopupParameters, CreatePopupResponse>(p =>
    {
        browser.Navigation.LoadUrl(p.TargetUrl);
        return CreatePopupResponse.Suppress();
    });
```

**VB**
```vb
browser.CreatePopupHandler = 
    New Handler(Of CreatePopupParameters, CreatePopupResponse)(Function(p)
        browser.Navigation.LoadUrl(p.TargetUrl)
        Return CreatePopupResponse.Suppress()
    End Function)
```



## Displaying pop-ups

When you initialize a WinForms or WPF `BrowserView`, it automatically configures the given `IBrowser` instance with the default implementation of the `CreatePopupHandler` and `OpenPopupHandler` handlers.

The default implementation of the `CreatePopupHandler` allows creating all pop-ups:


**C#**
```csharp
browser.CreatePopupHandler =
    new Handler<CreatePopupParameters, CreatePopupResponse>(p =>
    {
        return CreatePopupResponse.Create();
    });
```

**VB**
```vb
browser.CreatePopupHandler = 
    New Handler(Of CreatePopupParameters, CreatePopupResponse)(Function(p)
        Return CreatePopupResponse.Create()
    End Function)
```



See the details on the default implementation of the `OpenPopupHandler` handler for both WinForms and WPF below.

### WinForms

The default implementation for WinForms `BrowserView` is the following:


**C#**

```csharp
using System;
using System.Windows.Forms;
using DotNetBrowser.Browser;
using DotNetBrowser.Browser.Events;
using DotNetBrowser.Browser.Handlers;
using DotNetBrowser.Geometry;
using DotNetBrowser.Handlers;
using DotNetBrowser.WinForms;

namespace Popups.WinForms
{
    public class OpenPopupHandler : IHandler<OpenPopupParameters>
    {
        private readonly Control parent;

        public OpenPopupHandler(Control parent)
        {
            this.parent = parent;
        }

        public void Handle(OpenPopupParameters parameters)
        {
            Action showPopupAction = () =>
            {
                ShowPopup(parameters.PopupBrowser,
                          parameters.Rectangle);
            };
            parent.BeginInvoke(showPopupAction);
        }

        private void ShowPopup(IBrowser popupBrowser, Rectangle rectangle)
        {
            BrowserView browserView = new BrowserView
            {
                Dock = DockStyle.Fill
            };

            browserView.InitializeFrom(popupBrowser);
            // Set the same popup handler for the popup browser itself.
            popupBrowser.OpenPopupHandler = new OpenPopupHandler(browserView);

            Form form = new Form();

            if(!rectangle.IsEmpty)
            {
                form.StartPosition = FormStartPosition.Manual;

                form.Location = new System.Drawing.Point(rectangle.Origin.X,
                                                         rectangle.Origin.Y);

                form.ClientSize = new System.Drawing.Size((int)rectangle.Size.Width,
                                                          (int)rectangle.Size.Height);

                browserView.Width = (int)rectangle.Size.Width;
                browserView.Height = (int)rectangle.Size.Height;
            }
            else
            {
                form.Width = 800;
                form.Height = 600;
            }

            form.Closed += delegate
            {
                form.Controls.Clear();

                if(!popupBrowser.IsDisposed)
                {
                    popupBrowser.Dispose();
                }
            };

            popupBrowser.TitleChanged += delegate (object sender, TitleChangedEventArgs e)
            {
                form.BeginInvoke((Action)(() => { form.Text = e.Title; }));
            };

            popupBrowser.Disposed += delegate
            {
                Action formCloseAction = () =>
                {
                    form.Controls.Clear();
                    form.Hide();
                    form.Close();
                    form.Dispose();
                };
                form.BeginInvoke(formCloseAction);
            };

            form.Controls.Add(browserView);
            form.Show();
        }
    }
}
```

**VB**

```vb
Imports DotNetBrowser.Browser
Imports DotNetBrowser.Browser.Handlers
Imports DotNetBrowser.Geometry
Imports DotNetBrowser.Handlers
Imports DotNetBrowser.WinForms

Public Class OpenPopupHandler
    Implements IHandler(Of OpenPopupParameters)

    Private ReadOnly parent As Control

    Public Sub New(parent As Control)
        Me.parent = parent
    End Sub

    Public Sub Handle(p As OpenPopupParameters) _
        Implements IHandler(Of OpenPopupParameters).Handle
        Dim showPopupAction As Action = Sub()
            ShowPopup(p.PopupBrowser, p.Rectangle)
        End Sub
        parent.BeginInvoke(showPopupAction)
    End Sub

    Private Sub ShowPopup(popupBrowser As IBrowser, rectangle As Rectangle)
        Dim browserView As New BrowserView With {.Dock = DockStyle.Fill}

        browserView.InitializeFrom(popupBrowser)
        ' Set the same popup handler for the popup browser itself.
        popupBrowser.OpenPopupHandler = New OpenPopupHandler(browserView)

        Dim form As New Form()

        If Not rectangle.IsEmpty Then
            form.StartPosition = FormStartPosition.Manual

            form.Location =
                New Drawing.Point(rectangle.Origin.X, rectangle.Origin.Y)

            form.ClientSize =
                New Drawing.Size(rectangle.Size.Width, rectangle.Size.Height)

            browserView.Width = CInt(rectangle.Size.Width)
            browserView.Height = CInt(rectangle.Size.Height)
        Else
            form.Width = 800
            form.Height = 600
        End If

        AddHandler form.Closed, Sub()
            form.Controls.Clear()

            If Not popupBrowser.IsDisposed Then
                popupBrowser.Dispose()
            End If
        End Sub

        AddHandler popupBrowser.TitleChanged, Sub(sender, e)
            form.BeginInvoke(CType(Sub()
                form.Text = e.Title
            End Sub, Action))
        End Sub

        AddHandler popupBrowser.Disposed, Sub()
            Dim formCloseAction As Action = Sub()
                form.Controls.Clear()
                form.Hide()
                form.Close()
                form.Dispose()
            End Sub
            form.BeginInvoke(formCloseAction)
        End Sub

        form.Controls.Add(browserView)
        form.Show()
    End Sub
End Class

```



### WPF

The default implementation for WPF `BrowserView` is the following:


**C#**

```csharp
using System;
using System.Windows;
using System.Windows.Threading;
using DotNetBrowser.Browser;
using DotNetBrowser.Browser.Handlers;
using DotNetBrowser.Geometry;
using DotNetBrowser.Handlers;
using DotNetBrowser.Wpf;

namespace Popups.Wpf
{
    public class OpenPopupHandler : IHandler<OpenPopupParameters>
    {
        private readonly FrameworkElement parent;

        private Dispatcher Dispatcher => parent?.Dispatcher
                                         ?? Application.Current.Dispatcher;

        public OpenPopupHandler(FrameworkElement parentElement)
        {
            parent = parentElement;
        }

        public void Handle(OpenPopupParameters parameters)
        {
            Action showPopupAction = () =>
            {
                ShowPopup(parameters.PopupBrowser,
                          parameters.Rectangle);
            };
            Dispatcher.BeginInvoke(showPopupAction);
        }

        private void ShowPopup(IBrowser popupBrowser, Rectangle rectangle)
        {
            BrowserView browserView = new BrowserView();
            browserView.InitializeFrom(popupBrowser);
            // Set the same popup handler for the popup browser itself.
            popupBrowser.OpenPopupHandler = new OpenPopupHandler(browserView);

            Window window = new Window {Owner = Window.GetWindow(parent)};

            if (!rectangle.IsEmpty)
            {
                window.Top = rectangle.Origin.Y;
                window.Left = rectangle.Origin.X;
                window.SizeToContent = SizeToContent.WidthAndHeight;

                browserView.Width = rectangle.Size.Width;
                browserView.Height = rectangle.Size.Height;
            }
            else
            {
                window.Width = 800;
                window.Height = 600;
            }

            window.Closed += (sender, args) =>
            {
                window.Content = null;
                if (!popupBrowser.IsDisposed)
                {
                    popupBrowser.Dispose();
                }
            };

            popupBrowser.TitleChanged += (sender, e) =>
            {
                Dispatcher?.BeginInvoke((Action) (() => window.Title = e.Title));
            };

            popupBrowser.Disposed += delegate
            {
                Dispatcher?.Invoke(() =>
                {
                    window.Content = null;
                    window.Hide();
                    window.Close();
                });
            };

            window.Content = browserView;
            window.Show();
        }
    }
}
```

**VB**

```vb
Imports System.Windows.Threading
Imports DotNetBrowser.Browser
Imports DotNetBrowser.Browser.Handlers
Imports DotNetBrowser.Geometry
Imports DotNetBrowser.Handlers
Imports DotNetBrowser.Wpf

Public Class OpenPopupHandler
    Implements IHandler(Of OpenPopupParameters)

    Private ReadOnly parent As FrameworkElement

    Private ReadOnly Property Dispatcher As Dispatcher
        Get
            Return If(parent?.Dispatcher, Application.Current.Dispatcher)
        End Get
    End Property

    Public Sub New(parentElement As FrameworkElement)
        parent = parentElement
    End Sub

    Public Sub Handle(p As OpenPopupParameters) _
        Implements IHandler(Of OpenPopupParameters).Handle
        Dim showPopupAction As Action =
                Sub()
                    ShowPopup(p.PopupBrowser, p.Rectangle)
                End Sub
        Dispatcher.BeginInvoke(showPopupAction)
    End Sub

    Private Sub ShowPopup(popupBrowser As IBrowser, rectangle As Rectangle)
        Dim browserView As New BrowserView()
        browserView.InitializeFrom(popupBrowser)
        ' Set the same popup handler for the popup browser itself.
        popupBrowser.OpenPopupHandler = New OpenPopupHandler(browserView)

        Dim window As New Window With {.Owner = Window.GetWindow(parent)}

        If Not rectangle.IsEmpty Then
            window.Top = rectangle.Origin.Y
            window.Left = rectangle.Origin.X
            window.SizeToContent = SizeToContent.WidthAndHeight

            browserView.Width = rectangle.Size.Width
            browserView.Height = rectangle.Size.Height
        Else
            window.Width = 800
            window.Height = 600
        End If

        AddHandler window.Closed, Sub(sender, args)
            window.Content = Nothing
            If Not popupBrowser.IsDisposed Then
                popupBrowser.Dispose()
            End If
        End Sub

        AddHandler popupBrowser.TitleChanged, Sub(sender, e)
            Dispatcher?.BeginInvoke(CType(Sub() window.Title = e.Title, Action))
        End Sub

        AddHandler popupBrowser.Disposed, Sub()
            Dispatcher?.Invoke(Sub()
                window.Content = Nothing
                window.Hide()
                window.Close()
            End Sub)
        End Sub

        window.Content = browserView
        window.Show()
    End Sub
End Class

```



### Avalonia UI

The default implementation for Avalonia `BrowserView` is the following:


```csharp
using Avalonia;
using Avalonia.Controls;
using Avalonia.Threading;
using DotNetBrowser.AvaloniaUi;
using DotNetBrowser.Browser;
using DotNetBrowser.Browser.Handlers;
using DotNetBrowser.Geometry;
using DotNetBrowser.Handlers;

namespace Popups
{
    public class OpenPopupHandler : IHandler<OpenPopupParameters>
    {
        public void Handle(OpenPopupParameters parameters)
        {
            Dispatcher.UIThread.InvokeAsync(() =>
            {
                ShowPopup(parameters.PopupBrowser,
                          parameters.Rectangle);
            });
        }

        private void ShowPopup(IBrowser popupBrowser, Rectangle rectangle)
        {
            BrowserView browserView = new BrowserView();
            browserView.InitializeFrom(popupBrowser);
            // Set the same popup handler for the popup browser itself.
            popupBrowser.OpenPopupHandler = new OpenPopupHandler();

            Window window = new Window();

            if (!rectangle.IsEmpty)
            {
                window.Position = new PixelPoint(rectangle.Origin.X, rectangle.Origin.Y);
                window.SizeToContent = SizeToContent.WidthAndHeight;
                browserView.Width = rectangle.Size.Width;
                browserView.Height = rectangle.Size.Height;
            }
            else
            {
                window.Width = 800;
                window.Height = 600;
            }

            window.Closed += (sender, args) =>
            {
                window.Content = null;
                if (!popupBrowser.IsDisposed)
                {
                    popupBrowser.Dispose();
                }
            };

            popupBrowser.TitleChanged += (sender, e) =>
            {
                Dispatcher.UIThread.InvokeAsync(() => window.Title = e.Title);
            };

            popupBrowser.Disposed += delegate
            {
                Dispatcher.UIThread.InvokeAsync(() =>
                {
                    window.Content = null;
                    window.Hide();
                    window.Close();
                });
            };

            window.Content = browserView;
            window.Show();
        }
    }
}
```

## Closing pop-ups

The opened pop-up can be closed using the `IBrowser.Dispose()` method or  `window.close()` from JavaScript. In both cases, the `Disposed` event is fired.

We recommend that you always register the `Disposed` event listener to get notifications when a pop-up is closed. This will allow you to hide the pop-up window if you have it displayed.


**C#**
```csharp
popupBrowser.Disposed += delegate
{
    // Hide the pop-up window.
};
```

**VB**
```vb
AddHandler popupBrowser.Disposed, Sub()
    ' Hide the pop-up window.
End Sub
```


