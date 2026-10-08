# <a id="DotNetBrowser_WinForms_BrowserView"></a> Class BrowserView

Namespace: [DotNetBrowser.WinForms](DotNetBrowser.WinForms.md)  
Assembly: DotNetBrowser.WinForms.dll  

The WinForms-based implementation of browser view.

```csharp
public class BrowserView : Panel, IDropTarget, ISynchronizeInvoke, IWin32Window, IBindableComponent, IComponent, IDisposable, IBrowserView
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[MarshalByRefObject](https://learn.microsoft.com/dotnet/api/system.marshalbyrefobject) ← 
[Component](https://learn.microsoft.com/dotnet/api/system.componentmodel.component) ← 
[Control](https://learn.microsoft.com/dotnet/api/system.windows.forms.control) ← 
[ScrollableControl](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol) ← 
[Panel](https://learn.microsoft.com/dotnet/api/system.windows.forms.panel) ← 
[BrowserView](DotNetBrowser.WinForms.BrowserView.md)

#### Implements

[IDropTarget](https://learn.microsoft.com/dotnet/api/system.windows.forms.idroptarget), 
[ISynchronizeInvoke](https://learn.microsoft.com/dotnet/api/system.componentmodel.isynchronizeinvoke), 
[IWin32Window](https://learn.microsoft.com/dotnet/api/system.windows.forms.iwin32window), 
[IBindableComponent](https://learn.microsoft.com/dotnet/api/system.windows.forms.ibindablecomponent), 
[IComponent](https://learn.microsoft.com/dotnet/api/system.componentmodel.icomponent), 
[IDisposable](https://learn.microsoft.com/dotnet/api/system.idisposable), 
IBrowserView

#### Inherited Members

[Panel.OnResize\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.panel.onresize), 
[Panel.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.panel.tostring), 
[Panel.AutoSize](https://learn.microsoft.com/dotnet/api/system.windows.forms.panel.autosize), 
[Panel.AutoSizeMode](https://learn.microsoft.com/dotnet/api/system.windows.forms.panel.autosizemode), 
[Panel.BorderStyle](https://learn.microsoft.com/dotnet/api/system.windows.forms.panel.borderstyle), 
[Panel.CreateParams](https://learn.microsoft.com/dotnet/api/system.windows.forms.panel.createparams), 
[Panel.DefaultSize](https://learn.microsoft.com/dotnet/api/system.windows.forms.panel.defaultsize), 
[Panel.TabStop](https://learn.microsoft.com/dotnet/api/system.windows.forms.panel.tabstop), 
[Panel.AutoSizeChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.panel.autosizechanged), 
[ScrollableControl.ScrollStateAutoScrolling](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.scrollstateautoscrolling), 
[ScrollableControl.ScrollStateHScrollVisible](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.scrollstatehscrollvisible), 
[ScrollableControl.ScrollStateVScrollVisible](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.scrollstatevscrollvisible), 
[ScrollableControl.ScrollStateUserHasScrolled](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.scrollstateuserhasscrolled), 
[ScrollableControl.ScrollStateFullDrag](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.scrollstatefulldrag), 
[ScrollableControl.AdjustFormScrollbars\(bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.adjustformscrollbars), 
[ScrollableControl.GetScrollState\(int\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.getscrollstate), 
[ScrollableControl.OnLayout\(LayoutEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.onlayout), 
[ScrollableControl.OnMouseWheel\(MouseEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.onmousewheel), 
[ScrollableControl.OnRightToLeftChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.onrighttoleftchanged), 
[ScrollableControl.OnPaintBackground\(PaintEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.onpaintbackground), 
[ScrollableControl.OnPaddingChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.onpaddingchanged), 
[ScrollableControl.OnVisibleChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.onvisiblechanged), 
[ScrollableControl.ScaleControl\(SizeF, BoundsSpecified\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.scalecontrol), 
[ScrollableControl.SetDisplayRectLocation\(int, int\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.setdisplayrectlocation), 
[ScrollableControl.ScrollControlIntoView\(Control\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.scrollcontrolintoview), 
[ScrollableControl.ScrollToControl\(Control\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.scrolltocontrol), 
[ScrollableControl.OnScroll\(ScrollEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.onscroll), 
[ScrollableControl.SetAutoScrollMargin\(int, int\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.setautoscrollmargin), 
[ScrollableControl.SetScrollState\(int, bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.setscrollstate), 
[ScrollableControl.WndProc\(ref Message\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.wndproc), 
[ScrollableControl.AutoScroll](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.autoscroll), 
[ScrollableControl.AutoScrollMargin](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.autoscrollmargin), 
[ScrollableControl.AutoScrollPosition](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.autoscrollposition), 
[ScrollableControl.AutoScrollMinSize](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.autoscrollminsize), 
[ScrollableControl.CreateParams](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.createparams), 
[ScrollableControl.DisplayRectangle](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.displayrectangle), 
[ScrollableControl.HScroll](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.hscroll), 
[ScrollableControl.HorizontalScroll](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.horizontalscroll), 
[ScrollableControl.VScroll](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.vscroll), 
[ScrollableControl.VerticalScroll](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.verticalscroll), 
[ScrollableControl.Scroll](https://learn.microsoft.com/dotnet/api/system.windows.forms.scrollablecontrol.scroll), 
[Control.GetAccessibilityObjectById\(int\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.getaccessibilityobjectbyid), 
[Control.SetAutoSizeMode\(AutoSizeMode\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.setautosizemode), 
[Control.GetAutoSizeMode\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.getautosizemode), 
[Control.GetPreferredSize\(Size\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.getpreferredsize), 
[Control.AccessibilityNotifyClients\(AccessibleEvents, int\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.accessibilitynotifyclients\#system\-windows\-forms\-control\-accessibilitynotifyclients\(system\-windows\-forms\-accessibleevents\-system\-int32\)), 
[Control.AccessibilityNotifyClients\(AccessibleEvents, int, int\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.accessibilitynotifyclients\#system\-windows\-forms\-control\-accessibilitynotifyclients\(system\-windows\-forms\-accessibleevents\-system\-int32\-system\-int32\)), 
[Control.BeginInvoke\(Delegate\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.begininvoke\#system\-windows\-forms\-control\-begininvoke\(system\-delegate\)), 
[Control.BeginInvoke\(Delegate, params object\[\]\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.begininvoke\#system\-windows\-forms\-control\-begininvoke\(system\-delegate\-system\-object\(\)\)), 
[Control.BringToFront\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.bringtofront), 
[Control.Contains\(Control\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.contains), 
[Control.CreateAccessibilityInstance\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.createaccessibilityinstance), 
[Control.CreateControlsInstance\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.createcontrolsinstance), 
[Control.CreateGraphics\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.creategraphics), 
[Control.CreateHandle\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.createhandle), 
[Control.CreateControl\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.createcontrol), 
[Control.DefWndProc\(ref Message\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.defwndproc), 
[Control.DestroyHandle\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.destroyhandle), 
[Control.Dispose\(bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.dispose), 
[Control.DoDragDrop\(object, DragDropEffects\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.dodragdrop), 
[Control.DrawToBitmap\(Bitmap, Rectangle\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.drawtobitmap), 
[Control.EndInvoke\(IAsyncResult\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.endinvoke), 
[Control.FindForm\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.findform), 
[Control.GetTopLevel\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.gettoplevel), 
[Control.RaiseKeyEvent\(object, KeyEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.raisekeyevent), 
[Control.RaiseMouseEvent\(object, MouseEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.raisemouseevent), 
[Control.Focus\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.focus), 
[Control.FromChildHandle\(IntPtr\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.fromchildhandle), 
[Control.FromHandle\(IntPtr\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.fromhandle), 
[Control.GetChildAtPoint\(Point, GetChildAtPointSkip\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.getchildatpoint\#system\-windows\-forms\-control\-getchildatpoint\(system\-drawing\-point\-system\-windows\-forms\-getchildatpointskip\)), 
[Control.GetChildAtPoint\(Point\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.getchildatpoint\#system\-windows\-forms\-control\-getchildatpoint\(system\-drawing\-point\)), 
[Control.GetContainerControl\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.getcontainercontrol), 
[Control.GetScaledBounds\(Rectangle, SizeF, BoundsSpecified\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.getscaledbounds), 
[Control.GetNextControl\(Control, bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.getnextcontrol), 
[Control.GetStyle\(ControlStyles\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.getstyle), 
[Control.Hide\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.hide), 
[Control.InitLayout\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.initlayout), 
[Control.Invalidate\(Region\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invalidate\#system\-windows\-forms\-control\-invalidate\(system\-drawing\-region\)), 
[Control.Invalidate\(Region, bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invalidate\#system\-windows\-forms\-control\-invalidate\(system\-drawing\-region\-system\-boolean\)), 
[Control.Invalidate\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invalidate\#system\-windows\-forms\-control\-invalidate), 
[Control.Invalidate\(bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invalidate\#system\-windows\-forms\-control\-invalidate\(system\-boolean\)), 
[Control.Invalidate\(Rectangle\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invalidate\#system\-windows\-forms\-control\-invalidate\(system\-drawing\-rectangle\)), 
[Control.Invalidate\(Rectangle, bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invalidate\#system\-windows\-forms\-control\-invalidate\(system\-drawing\-rectangle\-system\-boolean\)), 
[Control.Invoke\(Delegate\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invoke\#system\-windows\-forms\-control\-invoke\(system\-delegate\)), 
[Control.Invoke\(Delegate, params object\[\]\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invoke\#system\-windows\-forms\-control\-invoke\(system\-delegate\-system\-object\(\)\)), 
[Control.InvokePaint\(Control, PaintEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invokepaint), 
[Control.InvokePaintBackground\(Control, PaintEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invokepaintbackground), 
[Control.IsKeyLocked\(Keys\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.iskeylocked), 
[Control.IsInputChar\(char\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.isinputchar), 
[Control.IsInputKey\(Keys\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.isinputkey), 
[Control.IsMnemonic\(char, string\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ismnemonic), 
[Control.NotifyInvalidate\(Rectangle\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.notifyinvalidate), 
[Control.InvokeOnClick\(Control, EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invokeonclick), 
[Control.OnAutoSizeChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onautosizechanged), 
[Control.OnBackColorChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onbackcolorchanged), 
[Control.OnBackgroundImageChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onbackgroundimagechanged), 
[Control.OnBackgroundImageLayoutChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onbackgroundimagelayoutchanged), 
[Control.OnBindingContextChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onbindingcontextchanged), 
[Control.OnCausesValidationChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.oncausesvalidationchanged), 
[Control.OnContextMenuChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.oncontextmenuchanged), 
[Control.OnContextMenuStripChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.oncontextmenustripchanged), 
[Control.OnCursorChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.oncursorchanged), 
[Control.OnDockChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ondockchanged), 
[Control.OnEnabledChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onenabledchanged), 
[Control.OnFontChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onfontchanged), 
[Control.OnForeColorChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onforecolorchanged), 
[Control.OnRightToLeftChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onrighttoleftchanged), 
[Control.OnNotifyMessage\(Message\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onnotifymessage), 
[Control.OnParentBackColorChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onparentbackcolorchanged), 
[Control.OnParentBackgroundImageChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onparentbackgroundimagechanged), 
[Control.OnParentBindingContextChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onparentbindingcontextchanged), 
[Control.OnParentCursorChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onparentcursorchanged), 
[Control.OnParentEnabledChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onparentenabledchanged), 
[Control.OnParentFontChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onparentfontchanged), 
[Control.OnParentForeColorChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onparentforecolorchanged), 
[Control.OnParentRightToLeftChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onparentrighttoleftchanged), 
[Control.OnParentVisibleChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onparentvisiblechanged), 
[Control.OnPrint\(PaintEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onprint), 
[Control.OnTabIndexChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ontabindexchanged), 
[Control.OnTabStopChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ontabstopchanged), 
[Control.OnTextChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ontextchanged), 
[Control.OnVisibleChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onvisiblechanged), 
[Control.OnParentChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onparentchanged), 
[Control.OnClick\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onclick), 
[Control.OnClientSizeChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onclientsizechanged), 
[Control.OnControlAdded\(ControlEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.oncontroladded), 
[Control.OnControlRemoved\(ControlEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.oncontrolremoved), 
[Control.OnCreateControl\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.oncreatecontrol), 
[Control.OnHandleCreated\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onhandlecreated), 
[Control.OnLocationChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onlocationchanged), 
[Control.OnHandleDestroyed\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onhandledestroyed), 
[Control.OnDoubleClick\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ondoubleclick), 
[Control.OnDragEnter\(DragEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ondragenter), 
[Control.OnDragOver\(DragEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ondragover), 
[Control.OnDragLeave\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ondragleave), 
[Control.OnDragDrop\(DragEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ondragdrop), 
[Control.OnGiveFeedback\(GiveFeedbackEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ongivefeedback), 
[Control.OnEnter\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onenter), 
[Control.InvokeGotFocus\(Control, EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invokegotfocus), 
[Control.OnGotFocus\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ongotfocus), 
[Control.OnHelpRequested\(HelpEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onhelprequested), 
[Control.OnInvalidated\(InvalidateEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.oninvalidated), 
[Control.OnKeyDown\(KeyEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onkeydown), 
[Control.OnKeyPress\(KeyPressEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onkeypress), 
[Control.OnKeyUp\(KeyEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onkeyup), 
[Control.OnLayout\(LayoutEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onlayout), 
[Control.OnLeave\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onleave), 
[Control.InvokeLostFocus\(Control, EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invokelostfocus), 
[Control.OnLostFocus\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onlostfocus), 
[Control.OnMarginChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmarginchanged), 
[Control.OnMouseDoubleClick\(MouseEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmousedoubleclick), 
[Control.OnMouseClick\(MouseEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmouseclick), 
[Control.OnMouseCaptureChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmousecapturechanged), 
[Control.OnMouseDown\(MouseEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmousedown), 
[Control.OnMouseEnter\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmouseenter), 
[Control.OnMouseLeave\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmouseleave), 
[Control.OnMouseHover\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmousehover), 
[Control.OnMouseMove\(MouseEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmousemove), 
[Control.OnMouseUp\(MouseEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmouseup), 
[Control.OnMouseWheel\(MouseEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmousewheel), 
[Control.OnMove\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onmove), 
[Control.OnPaint\(PaintEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onpaint), 
[Control.OnPaddingChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onpaddingchanged), 
[Control.OnPaintBackground\(PaintEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onpaintbackground), 
[Control.OnQueryContinueDrag\(QueryContinueDragEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onquerycontinuedrag), 
[Control.OnRegionChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onregionchanged), 
[Control.OnResize\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onresize), 
[Control.OnPreviewKeyDown\(PreviewKeyDownEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onpreviewkeydown), 
[Control.OnSizeChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onsizechanged), 
[Control.OnChangeUICues\(UICuesEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onchangeuicues), 
[Control.OnStyleChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onstylechanged), 
[Control.OnSystemColorsChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onsystemcolorschanged), 
[Control.OnValidating\(CancelEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onvalidating), 
[Control.OnValidated\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onvalidated), 
[Control.PerformLayout\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.performlayout\#system\-windows\-forms\-control\-performlayout), 
[Control.PerformLayout\(Control, string\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.performlayout\#system\-windows\-forms\-control\-performlayout\(system\-windows\-forms\-control\-system\-string\)), 
[Control.PointToClient\(Point\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.pointtoclient), 
[Control.PointToScreen\(Point\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.pointtoscreen), 
[Control.PreProcessMessage\(ref Message\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.preprocessmessage), 
[Control.PreProcessControlMessage\(ref Message\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.preprocesscontrolmessage), 
[Control.ProcessCmdKey\(ref Message, Keys\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.processcmdkey), 
[Control.ProcessDialogChar\(char\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.processdialogchar), 
[Control.ProcessDialogKey\(Keys\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.processdialogkey), 
[Control.ProcessKeyEventArgs\(ref Message\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.processkeyeventargs), 
[Control.ProcessKeyMessage\(ref Message\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.processkeymessage), 
[Control.ProcessKeyPreview\(ref Message\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.processkeypreview), 
[Control.ProcessMnemonic\(char\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.processmnemonic), 
[Control.RaiseDragEvent\(object, DragEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.raisedragevent), 
[Control.RaisePaintEvent\(object, PaintEventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.raisepaintevent), 
[Control.RecreateHandle\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.recreatehandle), 
[Control.RectangleToClient\(Rectangle\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.rectangletoclient), 
[Control.RectangleToScreen\(Rectangle\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.rectangletoscreen), 
[Control.ReflectMessage\(IntPtr, ref Message\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.reflectmessage), 
[Control.Refresh\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.refresh), 
[Control.ResetMouseEventArgs\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.resetmouseeventargs), 
[Control.ResetText\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.resettext), 
[Control.ResumeLayout\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.resumelayout\#system\-windows\-forms\-control\-resumelayout), 
[Control.ResumeLayout\(bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.resumelayout\#system\-windows\-forms\-control\-resumelayout\(system\-boolean\)), 
[Control.Scale\(SizeF\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.scale\#system\-windows\-forms\-control\-scale\(system\-drawing\-sizef\)), 
[Control.ScaleControl\(SizeF, BoundsSpecified\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.scalecontrol), 
[Control.Select\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.select\#system\-windows\-forms\-control\-select), 
[Control.Select\(bool, bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.select\#system\-windows\-forms\-control\-select\(system\-boolean\-system\-boolean\)), 
[Control.SelectNextControl\(Control, bool, bool, bool, bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.selectnextcontrol), 
[Control.SendToBack\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.sendtoback), 
[Control.SetBounds\(int, int, int, int\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.setbounds\#system\-windows\-forms\-control\-setbounds\(system\-int32\-system\-int32\-system\-int32\-system\-int32\)), 
[Control.SetBounds\(int, int, int, int, BoundsSpecified\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.setbounds\#system\-windows\-forms\-control\-setbounds\(system\-int32\-system\-int32\-system\-int32\-system\-int32\-system\-windows\-forms\-boundsspecified\)), 
[Control.SetBoundsCore\(int, int, int, int, BoundsSpecified\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.setboundscore), 
[Control.SetClientSizeCore\(int, int\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.setclientsizecore), 
[Control.SizeFromClientSize\(Size\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.sizefromclientsize), 
[Control.SetStyle\(ControlStyles, bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.setstyle), 
[Control.SetTopLevel\(bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.settoplevel), 
[Control.SetVisibleCore\(bool\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.setvisiblecore), 
[Control.RtlTranslateAlignment\(HorizontalAlignment\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.rtltranslatealignment\#system\-windows\-forms\-control\-rtltranslatealignment\(system\-windows\-forms\-horizontalalignment\)), 
[Control.RtlTranslateAlignment\(LeftRightAlignment\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.rtltranslatealignment\#system\-windows\-forms\-control\-rtltranslatealignment\(system\-windows\-forms\-leftrightalignment\)), 
[Control.RtlTranslateAlignment\(ContentAlignment\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.rtltranslatealignment\#system\-windows\-forms\-control\-rtltranslatealignment\(system\-drawing\-contentalignment\)), 
[Control.RtlTranslateHorizontal\(HorizontalAlignment\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.rtltranslatehorizontal), 
[Control.RtlTranslateLeftRight\(LeftRightAlignment\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.rtltranslateleftright), 
[Control.RtlTranslateContent\(ContentAlignment\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.rtltranslatecontent), 
[Control.Show\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.show), 
[Control.SuspendLayout\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.suspendlayout), 
[Control.Update\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.update), 
[Control.UpdateBounds\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.updatebounds\#system\-windows\-forms\-control\-updatebounds), 
[Control.UpdateBounds\(int, int, int, int\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.updatebounds\#system\-windows\-forms\-control\-updatebounds\(system\-int32\-system\-int32\-system\-int32\-system\-int32\)), 
[Control.UpdateBounds\(int, int, int, int, int, int\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.updatebounds\#system\-windows\-forms\-control\-updatebounds\(system\-int32\-system\-int32\-system\-int32\-system\-int32\-system\-int32\-system\-int32\)), 
[Control.UpdateZOrder\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.updatezorder), 
[Control.UpdateStyles\(\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.updatestyles), 
[Control.WndProc\(ref Message\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.wndproc), 
[Control.OnImeModeChanged\(EventArgs\)](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.onimemodechanged), 
[Control.AccessibilityObject](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.accessibilityobject), 
[Control.AccessibleDefaultActionDescription](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.accessibledefaultactiondescription), 
[Control.AccessibleDescription](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.accessibledescription), 
[Control.AccessibleName](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.accessiblename), 
[Control.AccessibleRole](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.accessiblerole), 
[Control.AllowDrop](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.allowdrop), 
[Control.Anchor](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.anchor), 
[Control.AutoScrollOffset](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.autoscrolloffset), 
[Control.LayoutEngine](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.layoutengine), 
[Control.BackColor](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.backcolor), 
[Control.BackgroundImage](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.backgroundimage), 
[Control.BackgroundImageLayout](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.backgroundimagelayout), 
[Control.BindingContext](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.bindingcontext), 
[Control.Bottom](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.bottom), 
[Control.Bounds](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.bounds), 
[Control.CanFocus](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.canfocus), 
[Control.CanRaiseEvents](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.canraiseevents), 
[Control.CanSelect](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.canselect), 
[Control.Capture](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.capture), 
[Control.CausesValidation](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.causesvalidation), 
[Control.CheckForIllegalCrossThreadCalls](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.checkforillegalcrossthreadcalls), 
[Control.ClientRectangle](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.clientrectangle), 
[Control.ClientSize](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.clientsize), 
[Control.CompanyName](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.companyname), 
[Control.ContainsFocus](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.containsfocus), 
[Control.ContextMenu](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.contextmenu), 
[Control.ContextMenuStrip](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.contextmenustrip), 
[Control.Controls](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.controls), 
[Control.Created](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.created), 
[Control.CreateParams](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.createparams), 
[Control.Cursor](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.cursor), 
[Control.DataBindings](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.databindings), 
[Control.DefaultBackColor](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.defaultbackcolor), 
[Control.DefaultCursor](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.defaultcursor), 
[Control.DefaultFont](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.defaultfont), 
[Control.DefaultForeColor](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.defaultforecolor), 
[Control.DefaultMargin](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.defaultmargin), 
[Control.DefaultMaximumSize](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.defaultmaximumsize), 
[Control.DefaultMinimumSize](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.defaultminimumsize), 
[Control.DefaultPadding](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.defaultpadding), 
[Control.DefaultSize](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.defaultsize), 
[Control.DisplayRectangle](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.displayrectangle), 
[Control.IsDisposed](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.isdisposed), 
[Control.Disposing](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.disposing), 
[Control.Dock](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.dock), 
[Control.DoubleBuffered](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.doublebuffered), 
[Control.Enabled](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.enabled), 
[Control.Focused](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.focused), 
[Control.Font](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.font), 
[Control.FontHeight](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.fontheight), 
[Control.ForeColor](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.forecolor), 
[Control.Handle](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.handle), 
[Control.HasChildren](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.haschildren), 
[Control.Height](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.height), 
[Control.IsHandleCreated](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ishandlecreated), 
[Control.InvokeRequired](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invokerequired), 
[Control.IsAccessible](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.isaccessible), 
[Control.IsMirrored](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.ismirrored), 
[Control.Left](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.left), 
[Control.Location](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.location), 
[Control.Margin](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.margin), 
[Control.MaximumSize](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.maximumsize), 
[Control.MinimumSize](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.minimumsize), 
[Control.ModifierKeys](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.modifierkeys), 
[Control.MouseButtons](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mousebuttons), 
[Control.MousePosition](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mouseposition), 
[Control.Name](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.name), 
[Control.Parent](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.parent), 
[Control.ProductName](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.productname), 
[Control.ProductVersion](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.productversion), 
[Control.RecreatingHandle](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.recreatinghandle), 
[Control.Region](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.region), 
[Control.RenderRightToLeft](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.renderrighttoleft), 
[Control.ResizeRedraw](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.resizeredraw), 
[Control.Right](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.right), 
[Control.RightToLeft](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.righttoleft), 
[Control.ScaleChildren](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.scalechildren), 
[Control.Site](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.site), 
[Control.Size](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.size), 
[Control.TabIndex](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.tabindex), 
[Control.TabStop](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.tabstop), 
[Control.Tag](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.tag), 
[Control.Text](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.text), 
[Control.Top](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.top), 
[Control.TopLevelControl](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.toplevelcontrol), 
[Control.ShowKeyboardCues](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.showkeyboardcues), 
[Control.ShowFocusCues](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.showfocuscues), 
[Control.UseWaitCursor](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.usewaitcursor), 
[Control.Visible](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.visible), 
[Control.Width](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.width), 
[Control.PreferredSize](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.preferredsize), 
[Control.Padding](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.padding), 
[Control.CanEnableIme](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.canenableime), 
[Control.DefaultImeMode](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.defaultimemode), 
[Control.ImeMode](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.imemode), 
[Control.ImeModeBase](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.imemodebase), 
[Control.PropagatingImeMode](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.propagatingimemode), 
[Control.BackColorChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.backcolorchanged), 
[Control.BackgroundImageChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.backgroundimagechanged), 
[Control.BackgroundImageLayoutChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.backgroundimagelayoutchanged), 
[Control.BindingContextChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.bindingcontextchanged), 
[Control.CausesValidationChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.causesvalidationchanged), 
[Control.ClientSizeChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.clientsizechanged), 
[Control.ContextMenuChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.contextmenuchanged), 
[Control.ContextMenuStripChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.contextmenustripchanged), 
[Control.CursorChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.cursorchanged), 
[Control.DockChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.dockchanged), 
[Control.EnabledChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.enabledchanged), 
[Control.FontChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.fontchanged), 
[Control.ForeColorChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.forecolorchanged), 
[Control.LocationChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.locationchanged), 
[Control.MarginChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.marginchanged), 
[Control.RegionChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.regionchanged), 
[Control.RightToLeftChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.righttoleftchanged), 
[Control.SizeChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.sizechanged), 
[Control.TabIndexChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.tabindexchanged), 
[Control.TabStopChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.tabstopchanged), 
[Control.TextChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.textchanged), 
[Control.VisibleChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.visiblechanged), 
[Control.Click](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.click), 
[Control.ControlAdded](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.controladded), 
[Control.ControlRemoved](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.controlremoved), 
[Control.DragDrop](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.dragdrop), 
[Control.DragEnter](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.dragenter), 
[Control.DragOver](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.dragover), 
[Control.DragLeave](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.dragleave), 
[Control.GiveFeedback](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.givefeedback), 
[Control.HandleCreated](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.handlecreated), 
[Control.HandleDestroyed](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.handledestroyed), 
[Control.HelpRequested](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.helprequested), 
[Control.Invalidated](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.invalidated), 
[Control.PaddingChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.paddingchanged), 
[Control.Paint](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.paint), 
[Control.QueryContinueDrag](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.querycontinuedrag), 
[Control.QueryAccessibilityHelp](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.queryaccessibilityhelp), 
[Control.DoubleClick](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.doubleclick), 
[Control.Enter](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.enter), 
[Control.GotFocus](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.gotfocus), 
[Control.KeyDown](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.keydown), 
[Control.KeyPress](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.keypress), 
[Control.KeyUp](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.keyup), 
[Control.Layout](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.layout), 
[Control.Leave](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.leave), 
[Control.LostFocus](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.lostfocus), 
[Control.MouseClick](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mouseclick), 
[Control.MouseDoubleClick](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mousedoubleclick), 
[Control.MouseCaptureChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mousecapturechanged), 
[Control.MouseDown](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mousedown), 
[Control.MouseEnter](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mouseenter), 
[Control.MouseLeave](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mouseleave), 
[Control.MouseHover](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mousehover), 
[Control.MouseMove](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mousemove), 
[Control.MouseUp](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mouseup), 
[Control.MouseWheel](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.mousewheel), 
[Control.Move](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.move), 
[Control.PreviewKeyDown](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.previewkeydown), 
[Control.Resize](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.resize), 
[Control.ChangeUICues](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.changeuicues), 
[Control.StyleChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.stylechanged), 
[Control.SystemColorsChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.systemcolorschanged), 
[Control.Validating](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.validating), 
[Control.Validated](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.validated), 
[Control.ParentChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.parentchanged), 
[Control.ImeModeChanged](https://learn.microsoft.com/dotnet/api/system.windows.forms.control.imemodechanged), 
[Component.Dispose\(\)](https://learn.microsoft.com/dotnet/api/system.componentmodel.component.dispose\#system\-componentmodel\-component\-dispose), 
[Component.Dispose\(bool\)](https://learn.microsoft.com/dotnet/api/system.componentmodel.component.dispose\#system\-componentmodel\-component\-dispose\(system\-boolean\)), 
[Component.GetService\(Type\)](https://learn.microsoft.com/dotnet/api/system.componentmodel.component.getservice), 
[Component.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.componentmodel.component.tostring), 
[Component.CanRaiseEvents](https://learn.microsoft.com/dotnet/api/system.componentmodel.component.canraiseevents), 
[Component.Events](https://learn.microsoft.com/dotnet/api/system.componentmodel.component.events), 
[Component.Site](https://learn.microsoft.com/dotnet/api/system.componentmodel.component.site), 
[Component.Container](https://learn.microsoft.com/dotnet/api/system.componentmodel.component.container), 
[Component.DesignMode](https://learn.microsoft.com/dotnet/api/system.componentmodel.component.designmode), 
[Component.Disposed](https://learn.microsoft.com/dotnet/api/system.componentmodel.component.disposed), 
[MarshalByRefObject.MemberwiseClone\(bool\)](https://learn.microsoft.com/dotnet/api/system.marshalbyrefobject.memberwiseclone), 
[MarshalByRefObject.GetLifetimeService\(\)](https://learn.microsoft.com/dotnet/api/system.marshalbyrefobject.getlifetimeservice), 
[MarshalByRefObject.InitializeLifetimeService\(\)](https://learn.microsoft.com/dotnet/api/system.marshalbyrefobject.initializelifetimeservice), 
[MarshalByRefObject.CreateObjRef\(Type\)](https://learn.microsoft.com/dotnet/api/system.marshalbyrefobject.createobjref), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring), 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone)

## Examples

<pre><code class="lang-csharp">public partial class Form1 : Form
{
    BrowserView webView;

    private IEngine engine;
    private IBrowser browser;

    public Form1()
    {
        webView = new BrowserView() { Dock = DockStyle.Fill };
        InitializeComponent();
        try
        {
            Task.Run(() =&gt; {
                engine = EngineFactory.Create(new EngineOptions.Builder()
                {
                    RenderingMode = RenderingMode.HardwareAccelerated
                }.Build());
                browser = engine.CreateBrowser();

            }).ContinueWith((t) =&gt;
            {
                webView.InitializeFrom(browser);
                browser.Navigation.LoadUrl("https://google.com");
            }, TaskScheduler.FromCurrentSynchronizationContext());
        }
        catch (Exception exception)
        {
            Debug.WriteLine(exception);
        }
        FormClosing += Form1_FormClosing;
        Controls.Add(webView);
    }

    private void Form1_FormClosing(object sender, FormClosingEventArgs e)
    {
        browser?.Dispose();
        engine?.Dispose();
    }
}</code></pre>

## Remarks

<p>
    To bind an instance of this view to a particular browser, use its
    <xref href="DotNetBrowser.Browser.BrowserViewExtensions.InitializeFrom(DotNetBrowser.Browser.IBrowserView%2cDotNetBrowser.Browser.IBrowser)" data-throw-if-not-resolved="false"></xref>
    method:
</p>
<code>
    browserView.InitializeFrom(browser);
</code>
<p>This method should be called from the UI thread.</p>

## Constructors

### <a id="DotNetBrowser_WinForms_BrowserView__ctor"></a> BrowserView\(\)

Initializes a new instance of the <xref href="DotNetBrowser.WinForms.BrowserView" data-throw-if-not-resolved="false"></xref> class.

```csharp
public BrowserView()
```

## Properties

### <a id="DotNetBrowser_WinForms_BrowserView_MenuItems"></a> MenuItems

The collection of the current context menu items.

```csharp
public ObservableCollection<MenuItemViewModel> MenuItems { get; }
```

#### Property Value

 [ObservableCollection](https://learn.microsoft.com/dotnet/api/system.collections.objectmodel.observablecollection\-1)<MenuItemViewModel\>

### <a id="DotNetBrowser_WinForms_BrowserView_SaveCreditCardHandler"></a> SaveCreditCardHandler

This handler is used when the user is prompted to save the credit cards in the credit card store,
if a different handler was not configured for the browser.

```csharp
public IHandler<SaveCreditCardParameters, SaveCreditCardResponse> SaveCreditCardHandler { get; }
```

#### Property Value

 IHandler<SaveCreditCardParameters, SaveCreditCardResponse\>

### <a id="DotNetBrowser_WinForms_BrowserView_SavePasswordHandler"></a> SavePasswordHandler

This handler is used when the user is prompted to save the credentials in the password store,
if a different handler was not configured for the browser.

```csharp
public IHandler<SavePasswordParameters, SavePasswordResponse> SavePasswordHandler { get; }
```

#### Property Value

 IHandler<SavePasswordParameters, SavePasswordResponse\>

### <a id="DotNetBrowser_WinForms_BrowserView_SaveUserDataProfileHandler"></a> SaveUserDataProfileHandler

This handler is used when the user is prompted to save the user data profiles in the user data profile store,
if a different handler was not configured for the browser.

```csharp
public IHandler<SaveUserDataProfileParameters, SaveUserDataProfileResponse> SaveUserDataProfileHandler { get; }
```

#### Property Value

 IHandler<SaveUserDataProfileParameters, SaveUserDataProfileResponse\>

### <a id="DotNetBrowser_WinForms_BrowserView_SelectCertificateHandler"></a> SelectCertificateHandler

This handler is used when the client SSL certificate should be selected,
if a different handler was not configured for the browser.

```csharp
public IHandler<SelectCertificateParameters, SelectCertificateResponse> SelectCertificateHandler { get; }
```

#### Property Value

 IHandler<SelectCertificateParameters, SelectCertificateResponse\>

### <a id="DotNetBrowser_WinForms_BrowserView_ShowContextMenuHandler"></a> ShowContextMenuHandler

The default context menu handler implementation for this browser view.

```csharp
public IHandler<ShowContextMenuParameters, ShowContextMenuResponse> ShowContextMenuHandler { get; }
```

#### Property Value

 IHandler<ShowContextMenuParameters, ShowContextMenuResponse\>

### <a id="DotNetBrowser_WinForms_BrowserView_StartDownloadHandler"></a> StartDownloadHandler

This handler is used when the browser is about to start downloading the file,
if a different handler was not configured for the browser.

```csharp
public IHandler<StartDownloadParameters, StartDownloadResponse> StartDownloadHandler { get; }
```

#### Property Value

 IHandler<StartDownloadParameters, StartDownloadResponse\>

### <a id="DotNetBrowser_WinForms_BrowserView_UpdatePasswordHandler"></a> UpdatePasswordHandler

This handler is used when the user is prompted to update the password in the password store,
if a different handler was not configured for the browser.

```csharp
public IHandler<UpdatePasswordParameters, UpdatePasswordResponse> UpdatePasswordHandler { get; }
```

#### Property Value

 IHandler<UpdatePasswordParameters, UpdatePasswordResponse\>

### <a id="DotNetBrowser_WinForms_BrowserView_UpdateUserDataProfileHandler"></a> UpdateUserDataProfileHandler

This handler is used when the user is prompted to update the user data profile in the user data profile store,
if a different handler was not configured for the browser.

```csharp
public IHandler<UpdateUserDataProfileParameters, UpdateUserDataProfileResponse> UpdateUserDataProfileHandler { get; }
```

#### Property Value

 IHandler<UpdateUserDataProfileParameters, UpdateUserDataProfileResponse\>

## Methods

### <a id="DotNetBrowser_WinForms_BrowserView_Focus"></a> Focus\(\)

Moves keyboard focus to this browser view.

```csharp
public bool Focus()
```

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a> if the input focus request was successful; otherwise, <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>.

#### Remarks

The inherited <xref href="System.Windows.Forms.Control.Focus" data-throw-if-not-resolved="false"></xref> only moves focus to this <xref href="System.Windows.Forms.Panel" data-throw-if-not-resolved="false"></xref>
itself, not to the hardware or off-screen child view it hosts, so it never actually
reaches the browser. This hides it and forwards focus to the active content view
directly instead.

### <a id="DotNetBrowser_WinForms_BrowserView_OnFocusRequested_System_Object_System_EventArgs_"></a> OnFocusRequested\(object, EventArgs\)

This method is used to handle <xref href="DotNetBrowser.Browser.IBrowser.FocusRequested" data-throw-if-not-resolved="false"></xref> event.

```csharp
public void OnFocusRequested(object sender, EventArgs e)
```

#### Parameters

`sender` [object](https://learn.microsoft.com/dotnet/api/system.object)

the event sender.

`e` [EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs)

the event arguments.

### <a id="DotNetBrowser_WinForms_BrowserView_OnVisibleChanged_System_EventArgs_"></a> OnVisibleChanged\(EventArgs\)

Raises the <xref href="System.Windows.Forms.Control.VisibleChanged" data-throw-if-not-resolved="false"></xref> event.

```csharp
protected override void OnVisibleChanged(EventArgs e)
```

#### Parameters

`e` [EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs)

An <xref href="System.EventArgs" data-throw-if-not-resolved="false"></xref> object that contains the event data.

