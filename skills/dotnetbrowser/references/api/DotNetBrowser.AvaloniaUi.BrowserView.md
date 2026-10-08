# <a id="DotNetBrowser_AvaloniaUi_BrowserView"></a> Class BrowserView

Namespace: [DotNetBrowser.AvaloniaUi](DotNetBrowser.AvaloniaUi.md)  
Assembly: DotNetBrowser.AvaloniaUi.dll  

The Avalonia-based implementation of a browser view.

```csharp
public class BrowserView : UserControl, INotifyPropertyChanged, IDataContextProvider, ILogical, IThemeVariantHost, IResourceHost, IResourceNode, IStyleHost, ISetLogicalParent, ISetInheritanceParent, ISupportInitialize, IStyleable, INamed, IInputElement, IDataTemplateHost, ISetterValue, IBrowserView
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
AvaloniaObject ← 
Animatable ← 
StyledElement ← 
Visual ← 
Layoutable ← 
Interactive ← 
InputElement ← 
Control ← 
TemplatedControl ← 
ContentControl ← 
UserControl ← 
[BrowserView](DotNetBrowser.AvaloniaUi.BrowserView.md)

#### Implements

[INotifyPropertyChanged](https://learn.microsoft.com/dotnet/api/system.componentmodel.inotifypropertychanged), 
IDataContextProvider, 
ILogical, 
IThemeVariantHost, 
IResourceHost, 
IResourceNode, 
IStyleHost, 
ISetLogicalParent, 
ISetInheritanceParent, 
[ISupportInitialize](https://learn.microsoft.com/dotnet/api/system.componentmodel.isupportinitialize), 
IStyleable, 
INamed, 
IInputElement, 
IDataTemplateHost, 
ISetterValue, 
[IBrowserView](DotNetBrowser.Browser.IBrowserView.md)

#### Inherited Members

ContentControl.ContentProperty, 
ContentControl.ContentTemplateProperty, 
ContentControl.HorizontalContentAlignmentProperty, 
ContentControl.VerticalContentAlignmentProperty, 
ContentControl.OnPropertyChanged\(AvaloniaPropertyChangedEventArgs\), 
ContentControl.RegisterContentPresenter\(ContentPresenter\), 
ContentControl.Content, 
ContentControl.ContentTemplate, 
ContentControl.Presenter, 
ContentControl.HorizontalContentAlignment, 
ContentControl.VerticalContentAlignment, 
TemplatedControl.BackgroundProperty, 
TemplatedControl.BackgroundSizingProperty, 
TemplatedControl.BorderBrushProperty, 
TemplatedControl.BorderThicknessProperty, 
TemplatedControl.CornerRadiusProperty, 
TemplatedControl.FontFamilyProperty, 
TemplatedControl.FontFeaturesProperty, 
TemplatedControl.FontSizeProperty, 
TemplatedControl.FontStyleProperty, 
TemplatedControl.FontWeightProperty, 
TemplatedControl.FontStretchProperty, 
TemplatedControl.ForegroundProperty, 
TemplatedControl.PaddingProperty, 
TemplatedControl.TemplateProperty, 
TemplatedControl.IsTemplateFocusTargetProperty, 
TemplatedControl.TemplateAppliedEvent, 
TemplatedControl.GetIsTemplateFocusTarget\(Control\), 
TemplatedControl.SetIsTemplateFocusTarget\(Control, bool\), 
TemplatedControl.ApplyTemplate\(\), 
TemplatedControl.GetTemplateFocusTarget\(\), 
TemplatedControl.OnAttachedToLogicalTree\(LogicalTreeAttachmentEventArgs\), 
TemplatedControl.OnDetachedFromLogicalTree\(LogicalTreeAttachmentEventArgs\), 
TemplatedControl.OnApplyTemplate\(TemplateAppliedEventArgs\), 
TemplatedControl.OnTemplateChanged\(AvaloniaPropertyChangedEventArgs\), 
TemplatedControl.Background, 
TemplatedControl.BackgroundSizing, 
TemplatedControl.BorderBrush, 
TemplatedControl.BorderThickness, 
TemplatedControl.CornerRadius, 
TemplatedControl.FontFamily, 
TemplatedControl.FontFeatures, 
TemplatedControl.FontSize, 
TemplatedControl.FontStyle, 
TemplatedControl.FontWeight, 
TemplatedControl.FontStretch, 
TemplatedControl.Foreground, 
TemplatedControl.Padding, 
TemplatedControl.Template, 
TemplatedControl.TemplateApplied, 
Control.FocusAdornerProperty, 
Control.TagProperty, 
Control.ContextMenuProperty, 
Control.ContextFlyoutProperty, 
Control.RequestBringIntoViewEvent, 
Control.ContextRequestedEvent, 
Control.LoadedEvent, 
Control.UnloadedEvent, 
Control.SizeChangedEvent, 
Control.GetTemplateFocusTarget\(\), 
Control.OnLoaded\(RoutedEventArgs\), 
Control.OnUnloaded\(RoutedEventArgs\), 
Control.OnSizeChanged\(SizeChangedEventArgs\), 
Control.OnAttachedToVisualTreeCore\(VisualTreeAttachmentEventArgs\), 
Control.OnDetachedFromVisualTreeCore\(VisualTreeAttachmentEventArgs\), 
Control.OnGotFocus\(GotFocusEventArgs\), 
Control.OnLostFocus\(RoutedEventArgs\), 
Control.OnCreateAutomationPeer\(\), 
Control.OnPointerReleased\(PointerReleasedEventArgs\), 
Control.OnKeyUp\(KeyEventArgs\), 
Control.OnPropertyChanged\(AvaloniaPropertyChangedEventArgs\), 
Control.FocusAdorner, 
Control.DataTemplates, 
Control.ContextMenu, 
Control.ContextFlyout, 
Control.IsLoaded, 
Control.Tag, 
Control.ContextRequested, 
Control.Loaded, 
Control.Unloaded, 
Control.SizeChanged, 
InputElement.FocusableProperty, 
InputElement.IsEnabledProperty, 
InputElement.IsEffectivelyEnabledProperty, 
InputElement.CursorProperty, 
InputElement.IsKeyboardFocusWithinProperty, 
InputElement.IsFocusedProperty, 
InputElement.IsHitTestVisibleProperty, 
InputElement.IsPointerOverProperty, 
InputElement.IsTabStopProperty, 
InputElement.GotFocusEvent, 
InputElement.LostFocusEvent, 
InputElement.KeyDownEvent, 
InputElement.KeyUpEvent, 
InputElement.TabIndexProperty, 
InputElement.TextInputEvent, 
InputElement.TextInputMethodClientRequestedEvent, 
InputElement.PointerEnteredEvent, 
InputElement.PointerExitedEvent, 
InputElement.PointerMovedEvent, 
InputElement.PointerPressedEvent, 
InputElement.PointerReleasedEvent, 
InputElement.PointerCaptureLostEvent, 
InputElement.PointerWheelChangedEvent, 
InputElement.TappedEvent, 
InputElement.HoldingEvent, 
InputElement.DoubleTappedEvent, 
InputElement.Focus\(NavigationMethod, KeyModifiers\), 
InputElement.OnDetachedFromVisualTreeCore\(VisualTreeAttachmentEventArgs\), 
InputElement.OnAttachedToVisualTreeCore\(VisualTreeAttachmentEventArgs\), 
InputElement.OnGotFocus\(GotFocusEventArgs\), 
InputElement.OnLostFocus\(RoutedEventArgs\), 
InputElement.OnKeyDown\(KeyEventArgs\), 
InputElement.OnKeyUp\(KeyEventArgs\), 
InputElement.OnTextInput\(TextInputEventArgs\), 
InputElement.OnPointerEntered\(PointerEventArgs\), 
InputElement.OnPointerExited\(PointerEventArgs\), 
InputElement.OnPointerMoved\(PointerEventArgs\), 
InputElement.OnPointerPressed\(PointerPressedEventArgs\), 
InputElement.OnPointerReleased\(PointerReleasedEventArgs\), 
InputElement.OnPointerCaptureLost\(PointerCaptureLostEventArgs\), 
InputElement.OnPointerWheelChanged\(PointerWheelEventArgs\), 
InputElement.OnPropertyChanged\(AvaloniaPropertyChangedEventArgs\), 
InputElement.UpdateIsEffectivelyEnabled\(\), 
InputElement.Focusable, 
InputElement.IsEnabled, 
InputElement.Cursor, 
InputElement.IsKeyboardFocusWithin, 
InputElement.IsFocused, 
InputElement.IsHitTestVisible, 
InputElement.IsPointerOver, 
InputElement.IsTabStop, 
InputElement.IsEffectivelyEnabled, 
InputElement.TabIndex, 
InputElement.KeyBindings, 
InputElement.IsEnabledCore, 
InputElement.GestureRecognizers, 
InputElement.GotFocus, 
InputElement.LostFocus, 
InputElement.KeyDown, 
InputElement.KeyUp, 
InputElement.TextInput, 
InputElement.TextInputMethodClientRequested, 
InputElement.PointerEntered, 
InputElement.PointerExited, 
InputElement.PointerMoved, 
InputElement.PointerPressed, 
InputElement.PointerReleased, 
InputElement.PointerCaptureLost, 
InputElement.PointerWheelChanged, 
InputElement.Tapped, 
InputElement.Holding, 
InputElement.DoubleTapped, 
Interactive.AddHandler\(RoutedEvent, Delegate, RoutingStrategies, bool\), 
Interactive.AddHandler<TEventArgs\>\(RoutedEvent<TEventArgs\>, EventHandler<TEventArgs\>?, RoutingStrategies, bool\), 
Interactive.RemoveHandler\(RoutedEvent, Delegate\), 
Interactive.RemoveHandler<TEventArgs\>\(RoutedEvent<TEventArgs\>, EventHandler<TEventArgs\>?\), 
Interactive.RaiseEvent\(RoutedEventArgs\), 
Interactive.BuildEventRoute\(RoutedEvent\), 
Layoutable.DesiredSizeProperty, 
Layoutable.WidthProperty, 
Layoutable.HeightProperty, 
Layoutable.MinWidthProperty, 
Layoutable.MaxWidthProperty, 
Layoutable.MinHeightProperty, 
Layoutable.MaxHeightProperty, 
Layoutable.MarginProperty, 
Layoutable.HorizontalAlignmentProperty, 
Layoutable.VerticalAlignmentProperty, 
Layoutable.UseLayoutRoundingProperty, 
Layoutable.UpdateLayout\(\), 
Layoutable.ApplyTemplate\(\), 
Layoutable.Measure\(Size\), 
Layoutable.Arrange\(Rect\), 
Layoutable.InvalidateMeasure\(\), 
Layoutable.InvalidateArrange\(\), 
Layoutable.AffectsMeasure<T\>\(params AvaloniaProperty\[\]\), 
Layoutable.AffectsArrange<T\>\(params AvaloniaProperty\[\]\), 
Layoutable.MeasureCore\(Size\), 
Layoutable.MeasureOverride\(Size\), 
Layoutable.ArrangeCore\(Rect\), 
Layoutable.ArrangeOverride\(Size\), 
Layoutable.OnAttachedToVisualTreeCore\(VisualTreeAttachmentEventArgs\), 
Layoutable.OnDetachedFromVisualTreeCore\(VisualTreeAttachmentEventArgs\), 
Layoutable.OnMeasureInvalidated\(\), 
Layoutable.OnPropertyChanged\(AvaloniaPropertyChangedEventArgs\), 
Layoutable.OnVisualParentChanged\(Visual?, Visual?\), 
Layoutable.Width, 
Layoutable.Height, 
Layoutable.MinWidth, 
Layoutable.MaxWidth, 
Layoutable.MinHeight, 
Layoutable.MaxHeight, 
Layoutable.Margin, 
Layoutable.HorizontalAlignment, 
Layoutable.VerticalAlignment, 
Layoutable.DesiredSize, 
Layoutable.IsMeasureValid, 
Layoutable.IsArrangeValid, 
Layoutable.UseLayoutRounding, 
Layoutable.EffectiveViewportChanged, 
Layoutable.LayoutUpdated, 
Visual.BoundsProperty, 
Visual.ClipToBoundsProperty, 
Visual.ClipProperty, 
Visual.IsVisibleProperty, 
Visual.OpacityProperty, 
Visual.OpacityMaskProperty, 
Visual.EffectProperty, 
Visual.HasMirrorTransformProperty, 
Visual.RenderTransformProperty, 
Visual.RenderTransformOriginProperty, 
Visual.FlowDirectionProperty, 
Visual.VisualParentProperty, 
Visual.ZIndexProperty, 
Visual.GetFlowDirection\(Visual\), 
Visual.SetFlowDirection\(Visual, FlowDirection\), 
Visual.InvalidateVisual\(\), 
Visual.Render\(DrawingContext\), 
Visual.AffectsRender<T\>\(params AvaloniaProperty\[\]\), 
Visual.OnPropertyChanged\(AvaloniaPropertyChangedEventArgs\), 
Visual.LogicalChildrenCollectionChanged\(object?, NotifyCollectionChangedEventArgs\), 
Visual.OnAttachedToVisualTreeCore\(VisualTreeAttachmentEventArgs\), 
Visual.OnDetachedFromVisualTreeCore\(VisualTreeAttachmentEventArgs\), 
Visual.OnAttachedToVisualTree\(VisualTreeAttachmentEventArgs\), 
Visual.OnDetachedFromVisualTree\(VisualTreeAttachmentEventArgs\), 
Visual.OnVisualParentChanged\(Visual?, Visual?\), 
Visual.InvalidateMirrorTransform\(\), 
Visual.Bounds, 
Visual.ClipToBounds, 
Visual.Clip, 
Visual.IsEffectivelyVisible, 
Visual.IsVisible, 
Visual.Opacity, 
Visual.OpacityMask, 
Visual.Effect, 
Visual.HasMirrorTransform, 
Visual.RenderTransform, 
Visual.RenderTransformOrigin, 
Visual.FlowDirection, 
Visual.ZIndex, 
Visual.VisualChildren, 
Visual.VisualRoot, 
Visual.BypassFlowDirectionPolicies, 
Visual.AttachedToVisualTree, 
Visual.DetachedFromVisualTree, 
StyledElement.DataContextProperty, 
StyledElement.NameProperty, 
StyledElement.ParentProperty, 
StyledElement.TemplatedParentProperty, 
StyledElement.ThemeProperty, 
StyledElement.BeginInit\(\), 
StyledElement.EndInit\(\), 
StyledElement.ApplyStyling\(\), 
StyledElement.InitializeIfNeeded\(\), 
StyledElement.TryGetResource\(object, ThemeVariant?, out object?\), 
StyledElement.LogicalChildrenCollectionChanged\(object?, NotifyCollectionChangedEventArgs\), 
StyledElement.OnAttachedToLogicalTree\(LogicalTreeAttachmentEventArgs\), 
StyledElement.OnDetachedFromLogicalTree\(LogicalTreeAttachmentEventArgs\), 
StyledElement.OnDataContextChanged\(EventArgs\), 
StyledElement.OnDataContextBeginUpdate\(\), 
StyledElement.OnDataContextEndUpdate\(\), 
StyledElement.OnInitialized\(\), 
StyledElement.OnPropertyChanged\(AvaloniaPropertyChangedEventArgs\), 
StyledElement.Name, 
StyledElement.Classes, 
StyledElement.DataContext, 
StyledElement.IsInitialized, 
StyledElement.Styles, 
StyledElement.StyleKey, 
StyledElement.Resources, 
StyledElement.TemplatedParent, 
StyledElement.Theme, 
StyledElement.LogicalChildren, 
StyledElement.PseudoClasses, 
StyledElement.StyleKeyOverride, 
StyledElement.Parent, 
StyledElement.ActualThemeVariant, 
StyledElement.AttachedToLogicalTree, 
StyledElement.DetachedFromLogicalTree, 
StyledElement.DataContextChanged, 
StyledElement.Initialized, 
StyledElement.ResourcesChanged, 
StyledElement.ActualThemeVariantChanged, 
Animatable.TransitionsProperty, 
Animatable.OnPropertyChangedCore\(AvaloniaPropertyChangedEventArgs\), 
Animatable.Transitions, 
AvaloniaObject.CheckAccess\(\), 
AvaloniaObject.VerifyAccess\(\), 
AvaloniaObject.ClearValue\(AvaloniaProperty\), 
AvaloniaObject.ClearValue<T\>\(AvaloniaProperty<T\>\), 
AvaloniaObject.ClearValue<T\>\(StyledProperty<T\>\), 
AvaloniaObject.ClearValue<T\>\(DirectPropertyBase<T\>\), 
AvaloniaObject.Equals\(object?\), 
AvaloniaObject.GetHashCode\(\), 
AvaloniaObject.GetValue\(AvaloniaProperty\), 
AvaloniaObject.GetValue<T\>\(StyledProperty<T\>\), 
AvaloniaObject.GetValue<T\>\(DirectPropertyBase<T\>\), 
AvaloniaObject.GetBaseValue<T\>\(StyledProperty<T\>\), 
AvaloniaObject.IsAnimating\(AvaloniaProperty\), 
AvaloniaObject.IsSet\(AvaloniaProperty\), 
AvaloniaObject.SetValue\(AvaloniaProperty, object?, BindingPriority\), 
AvaloniaObject.SetValue<T\>\(StyledProperty<T\>, T, BindingPriority\), 
AvaloniaObject.SetValue<T\>\(DirectPropertyBase<T\>, T\), 
AvaloniaObject.SetCurrentValue\(AvaloniaProperty, object?\), 
AvaloniaObject.SetCurrentValue<T\>\(StyledProperty<T\>, T\), 
AvaloniaObject.Bind\(AvaloniaProperty, IBinding\), 
AvaloniaObject.Bind\(AvaloniaProperty, IObservable<object?\>, BindingPriority\), 
AvaloniaObject.Bind<T\>\(StyledProperty<T\>, IObservable<object?\>, BindingPriority\), 
AvaloniaObject.Bind<T\>\(StyledProperty<T\>, IObservable<T\>, BindingPriority\), 
AvaloniaObject.Bind<T\>\(StyledProperty<T\>, IObservable<BindingValue<T\>\>, BindingPriority\), 
AvaloniaObject.Bind<T\>\(DirectPropertyBase<T\>, IObservable<object?\>\), 
AvaloniaObject.Bind<T\>\(DirectPropertyBase<T\>, IObservable<T\>\), 
AvaloniaObject.Bind<T\>\(DirectPropertyBase<T\>, IObservable<BindingValue<T\>\>\), 
AvaloniaObject.CoerceValue\(AvaloniaProperty\), 
AvaloniaObject.UpdateDataValidation\(AvaloniaProperty, BindingValueType, Exception?\), 
AvaloniaObject.OnPropertyChangedCore\(AvaloniaPropertyChangedEventArgs\), 
AvaloniaObject.OnPropertyChanged\(AvaloniaPropertyChangedEventArgs\), 
AvaloniaObject.RaisePropertyChanged<T\>\(DirectPropertyBase<T\>, T, T\), 
AvaloniaObject.SetAndRaise<T\>\(DirectPropertyBase<T\>, ref T, T\), 
AvaloniaObject.InheritanceParent, 
AvaloniaObject.this\[AvaloniaProperty\], 
AvaloniaObject.this\[IndexerDescriptor\], 
AvaloniaObject.PropertyChanged, 
[object.Equals\(object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.MemberwiseClone\(\)](https://learn.microsoft.com/dotnet/api/system.object.memberwiseclone), 
[object.ReferenceEquals\(object, object\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

#### Extension Methods

[BrowserViewExtensions.InitializeFrom\(IBrowserView, IBrowser\)](DotNetBrowser.Browser.BrowserViewExtensions.md\#DotNetBrowser\_Browser\_BrowserViewExtensions\_InitializeFrom\_DotNetBrowser\_Browser\_IBrowserView\_DotNetBrowser\_Browser\_IBrowser\_)

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

### <a id="DotNetBrowser_AvaloniaUi_BrowserView__ctor"></a> BrowserView\(\)

```csharp
public BrowserView()
```

## Properties

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_CreatePopupHandler"></a> CreatePopupHandler

This handler will be used when browser decides whether a new popup instance can be created or not,
if a different handler was not configured for the browser.

```csharp
public IHandler<CreatePopupParameters, CreatePopupResponse> CreatePopupHandler { get; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[CreatePopupParameters](DotNetBrowser.Browser.Handlers.CreatePopupParameters.md), [CreatePopupResponse](DotNetBrowser.Browser.Handlers.CreatePopupResponse.md)\>

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_MenuItems"></a> MenuItems

The collection of the current context menu items.

```csharp
public ObservableCollection<MenuItemViewModel> MenuItems { get; }
```

#### Property Value

 [ObservableCollection](https://learn.microsoft.com/dotnet/api/system.collections.objectmodel.observablecollection\-1)<MenuItemViewModel\>

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_OpenExtensionActionPopupHandler"></a> OpenExtensionActionPopupHandler

This handler is used for handling the popups that are requested to be shown by the extension action,
if a different handler was not configured for the browser.

```csharp
public IHandler<OpenExtensionActionPopupParameters> OpenExtensionActionPopupHandler { get; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-1.md)<[OpenExtensionActionPopupParameters](DotNetBrowser.Browser.Handlers.OpenExtensionActionPopupParameters.md)\>

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_OpenPopupHandler"></a> OpenPopupHandler

This handler is used when a new popup browser instance should be opened,
if a different handler was not configured for the browser.

```csharp
public IHandler<OpenPopupParameters> OpenPopupHandler { get; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-1.md)<[OpenPopupParameters](DotNetBrowser.Browser.Handlers.OpenPopupParameters.md)\>

#### Remarks

<p><b>Important:</b> the engine will be blocked until you return control from the callback.</p>

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_SaveCreditCardHandler"></a> SaveCreditCardHandler

This handler is used when the user is prompted to save the credit cards in the credit card store,
if a different handler was not configured for the browser.

```csharp
public IHandler<SaveCreditCardParameters, SaveCreditCardResponse> SaveCreditCardHandler { get; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SaveCreditCardParameters](DotNetBrowser.Card.Handlers.SaveCreditCardParameters.md), [SaveCreditCardResponse](DotNetBrowser.Card.Handlers.SaveCreditCardResponse.md)\>

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_SavePasswordHandler"></a> SavePasswordHandler

This handler is used when the user is prompted to save the credentials in the password store,
if a different handler was not configured for the browser.

```csharp
public IHandler<SavePasswordParameters, SavePasswordResponse> SavePasswordHandler { get; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SavePasswordParameters](DotNetBrowser.Passwords.Handlers.SavePasswordParameters.md), [SavePasswordResponse](DotNetBrowser.Passwords.Handlers.SavePasswordResponse.md)\>

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_SaveUserDataProfileHandler"></a> SaveUserDataProfileHandler

This handler is used when the user is prompted to save the user data profiles in the user data profile store,
if a different handler was not configured for the browser.

```csharp
public IHandler<SaveUserDataProfileParameters, SaveUserDataProfileResponse> SaveUserDataProfileHandler { get; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SaveUserDataProfileParameters](DotNetBrowser.UserData.Handlers.SaveUserDataProfileParameters.md), [SaveUserDataProfileResponse](DotNetBrowser.UserData.Handlers.SaveUserDataProfileResponse.md)\>

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_SelectCertificateHandler"></a> SelectCertificateHandler

This handler is used when the client SSL certificate should be selected,
if a different handler was not configured for the browser.

```csharp
public IHandler<SelectCertificateParameters, SelectCertificateResponse> SelectCertificateHandler { get; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[SelectCertificateParameters](DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateParameters.md), [SelectCertificateResponse](DotNetBrowser.Browser.Dialogs.Handlers.SelectCertificateResponse.md)\>

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_ShowContextMenuHandler"></a> ShowContextMenuHandler

The default context menu handler implementation for this browser view.

```csharp
public IHandler<ShowContextMenuParameters, ShowContextMenuResponse> ShowContextMenuHandler { get; set; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[ShowContextMenuParameters](DotNetBrowser.Browser.Handlers.ShowContextMenuParameters.md), [ShowContextMenuResponse](DotNetBrowser.Browser.Handlers.ShowContextMenuResponse.md)\>

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_StartDownloadHandler"></a> StartDownloadHandler

This handler is used when the browser is about to start downloading the file,
if a different handler was not configured for the browser.

```csharp
public IHandler<StartDownloadParameters, StartDownloadResponse> StartDownloadHandler { get; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[StartDownloadParameters](DotNetBrowser.Downloads.Handlers.StartDownloadParameters.md), [StartDownloadResponse](DotNetBrowser.Downloads.Handlers.StartDownloadResponse.md)\>

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_UpdatePasswordHandler"></a> UpdatePasswordHandler

This handler is used when the user is prompted to update the password in the password store,
if a different handler was not configured for the browser.

```csharp
public IHandler<UpdatePasswordParameters, UpdatePasswordResponse> UpdatePasswordHandler { get; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[UpdatePasswordParameters](DotNetBrowser.Passwords.Handlers.UpdatePasswordParameters.md), [UpdatePasswordResponse](DotNetBrowser.Passwords.Handlers.UpdatePasswordResponse.md)\>

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_UpdateUserDataProfileHandler"></a> UpdateUserDataProfileHandler

This handler is used when the user is prompted to update the user data profile in the user data profile store,
if a different handler was not configured for the browser.

```csharp
public IHandler<UpdateUserDataProfileParameters, UpdateUserDataProfileResponse> UpdateUserDataProfileHandler { get; }
```

#### Property Value

 [IHandler](DotNetBrowser.Handlers.IHandler\-2.md)<[UpdateUserDataProfileParameters](DotNetBrowser.UserData.Handlers.UpdateUserDataProfileParameters.md), [UpdateUserDataProfileResponse](DotNetBrowser.UserData.Handlers.UpdateUserDataProfileResponse.md)\>

## Methods

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_Focus_Avalonia_Input_NavigationMethod_Avalonia_Input_KeyModifiers_"></a> Focus\(NavigationMethod, KeyModifiers\)

Moves keyboard focus to this browser view.

```csharp
public bool Focus(NavigationMethod method = NavigationMethod.Unspecified, KeyModifiers keyModifiers = KeyModifiers.None)
```

#### Parameters

`method` NavigationMethod

The method by which focus was requested.

`keyModifiers` KeyModifiers

The keyboard modifiers that were pressed at the time of the request.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a> if the input focus request was successful; otherwise, <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>.

#### Remarks

This view itself is not a focus scope stop (<code>Focusable="False"</code> in XAML, so the
embedded browser content occupies a single Tab stop instead of two); focusing it
directly is a no-op. This hides the inherited method and forwards focus to the
hardware or off-screen content view instead.

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_InitializeComponent_System_Boolean_"></a> InitializeComponent\(bool\)

Wires up the controls and optionally loads XAML markup and attaches dev tools (if Avalonia.Diagnostics package is referenced).

```csharp
[ExcludeFromCodeCoverage]
public void InitializeComponent(bool loadXaml = true)
```

#### Parameters

`loadXaml` [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

Should the XAML be loaded into the component.

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_OnFocusRequested_System_Object_System_EventArgs_"></a> OnFocusRequested\(object, EventArgs\)

Event handler for <xref href="DotNetBrowser.Browser.IBrowser.FocusRequested" data-throw-if-not-resolved="false"></xref> event.

```csharp
public void OnFocusRequested(object sender, EventArgs e)
```

#### Parameters

`sender` [object](https://learn.microsoft.com/dotnet/api/system.object)

the sender of the event

`e` [EventArgs](https://learn.microsoft.com/dotnet/api/system.eventargs)

the event args

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_OnGotFocus_Avalonia_Input_GotFocusEventArgs_"></a> OnGotFocus\(GotFocusEventArgs\)

Called before the <xref href="Avalonia.Input.InputElement.GotFocus" data-throw-if-not-resolved="false"></xref> event occurs.

```csharp
protected override void OnGotFocus(GotFocusEventArgs e)
```

#### Parameters

`e` GotFocusEventArgs

The event args.

### <a id="DotNetBrowser_AvaloniaUi_BrowserView_OnPropertyChanged_Avalonia_AvaloniaPropertyChangedEventArgs_"></a> OnPropertyChanged\(AvaloniaPropertyChangedEventArgs\)

Called when a avalonia property changes on the object.

```csharp
protected override void OnPropertyChanged(AvaloniaPropertyChangedEventArgs change)
```

#### Parameters

`change` AvaloniaPropertyChangedEventArgs

The property change details.

