# <a id="DotNetBrowser_WinUi3_BrowserView"></a> Class BrowserView

Namespace: [DotNetBrowser.WinUi3](DotNetBrowser.WinUi3.md)  
Assembly: DotNetBrowser.WinUi3.dll  

The WinUI3-based implementation of browser view.

```csharp
[WinRTRuntimeClassName("Microsoft.UI.Xaml.IUIElementOverrides")]
[WinRTExposedType(typeof(DotNetBrowser_WinUi3_BrowserViewWinRTTypeDetails))]
public sealed class BrowserView : ContentControl, IEquatable<DependencyObject>, IAnimationObject, IVisualElement, IVisualElement2, IEquatable<UIElement>, IEquatable<FrameworkElement>, IEquatable<Control>, IWinRTObject, IDynamicInterfaceCastable, IEquatable<ContentControl>, IBrowserView
```

#### Inheritance

[object](https://learn.microsoft.com/dotnet/api/system.object) ← 
[DependencyObject](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject) ← 
[UIElement](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement) ← 
[FrameworkElement](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement) ← 
[Control](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control) ← 
[ContentControl](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol) ← 
[BrowserView](DotNetBrowser.WinUi3.BrowserView.md)

#### Implements

[IEquatable<DependencyObject\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1), 
[IAnimationObject](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.composition.ianimationobject), 
[IVisualElement](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.composition.ivisualelement), 
[IVisualElement2](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.composition.ivisualelement2), 
[IEquatable<UIElement\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1), 
[IEquatable<FrameworkElement\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1), 
[IEquatable<Control\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1), 
IWinRTObject, 
[IDynamicInterfaceCastable](https://learn.microsoft.com/dotnet/api/system.runtime.interopservices.idynamicinterfacecastable), 
[IEquatable<ContentControl\>](https://learn.microsoft.com/dotnet/api/system.iequatable\-1), 
IBrowserView

#### Inherited Members

[ContentControl.As<I\>\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.as), 
[ContentControl.FromAbi\(IntPtr\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.fromabi), 
[ContentControl.Equals\(ContentControl\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.equals\#microsoft\-ui\-xaml\-controls\-contentcontrol\-equals\(microsoft\-ui\-xaml\-controls\-contentcontrol\)), 
[ContentControl.Equals\(object\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.equals\#microsoft\-ui\-xaml\-controls\-contentcontrol\-equals\(system\-object\)), 
[ContentControl.GetHashCode\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.gethashcode), 
[ContentControl.ContentProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.contentproperty), 
[ContentControl.ContentTemplateProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.contenttemplateproperty), 
[ContentControl.ContentTemplateSelectorProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.contenttemplateselectorproperty), 
[ContentControl.ContentTransitionsProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.contenttransitionsproperty), 
[ContentControl.Content](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.content), 
[ContentControl.ContentTemplate](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.contenttemplate), 
[ContentControl.ContentTemplateRoot](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.contenttemplateroot), 
[ContentControl.ContentTemplateSelector](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.contenttemplateselector), 
[ContentControl.ContentTransitions](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.contentcontrol.contenttransitions), 
[Control.As<I\>\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.as), 
[Control.GetIsTemplateFocusTarget\(FrameworkElement\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.getistemplatefocustarget), 
[Control.SetIsTemplateFocusTarget\(FrameworkElement, bool\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.setistemplatefocustarget), 
[Control.GetIsTemplateKeyTipTarget\(DependencyObject\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.getistemplatekeytiptarget), 
[Control.SetIsTemplateKeyTipTarget\(DependencyObject, bool\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.setistemplatekeytiptarget), 
[Control.FromAbi\(IntPtr\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.fromabi), 
[Control.Equals\(Control\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.equals\#microsoft\-ui\-xaml\-controls\-control\-equals\(microsoft\-ui\-xaml\-controls\-control\)), 
[Control.Equals\(object\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.equals\#microsoft\-ui\-xaml\-controls\-control\-equals\(system\-object\)), 
[Control.GetHashCode\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.gethashcode), 
[Control.RemoveFocusEngagement\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.removefocusengagement), 
[Control.ApplyTemplate\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.applytemplate), 
[Control.BackgroundProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.backgroundproperty), 
[Control.BackgroundSizingProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.backgroundsizingproperty), 
[Control.BorderBrushProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.borderbrushproperty), 
[Control.BorderThicknessProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.borderthicknessproperty), 
[Control.CharacterSpacingProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.characterspacingproperty), 
[Control.CornerRadiusProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.cornerradiusproperty), 
[Control.DefaultStyleKeyProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.defaultstylekeyproperty), 
[Control.DefaultStyleResourceUriProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.defaultstyleresourceuriproperty), 
[Control.ElementSoundModeProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.elementsoundmodeproperty), 
[Control.FontFamilyProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.fontfamilyproperty), 
[Control.FontSizeProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.fontsizeproperty), 
[Control.FontStretchProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.fontstretchproperty), 
[Control.FontStyleProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.fontstyleproperty), 
[Control.FontWeightProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.fontweightproperty), 
[Control.ForegroundProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.foregroundproperty), 
[Control.HorizontalContentAlignmentProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.horizontalcontentalignmentproperty), 
[Control.IsEnabledProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.isenabledproperty), 
[Control.IsFocusEngagedProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.isfocusengagedproperty), 
[Control.IsFocusEngagementEnabledProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.isfocusengagementenabledproperty), 
[Control.IsTemplateFocusTargetProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.istemplatefocustargetproperty), 
[Control.IsTemplateKeyTipTargetProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.istemplatekeytiptargetproperty), 
[Control.IsTextScaleFactorEnabledProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.istextscalefactorenabledproperty), 
[Control.PaddingProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.paddingproperty), 
[Control.RequiresPointerProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.requirespointerproperty), 
[Control.TabNavigationProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.tabnavigationproperty), 
[Control.TemplateProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.templateproperty), 
[Control.VerticalContentAlignmentProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.verticalcontentalignmentproperty), 
[Control.Background](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.background), 
[Control.BackgroundSizing](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.backgroundsizing), 
[Control.BorderBrush](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.borderbrush), 
[Control.BorderThickness](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.borderthickness), 
[Control.CharacterSpacing](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.characterspacing), 
[Control.CornerRadius](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.cornerradius), 
[Control.DefaultStyleResourceUri](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.defaultstyleresourceuri), 
[Control.ElementSoundMode](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.elementsoundmode), 
[Control.FontFamily](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.fontfamily), 
[Control.FontSize](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.fontsize), 
[Control.FontStretch](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.fontstretch), 
[Control.FontStyle](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.fontstyle), 
[Control.FontWeight](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.fontweight), 
[Control.Foreground](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.foreground), 
[Control.HorizontalContentAlignment](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.horizontalcontentalignment), 
[Control.IsEnabled](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.isenabled), 
[Control.IsFocusEngaged](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.isfocusengaged), 
[Control.IsFocusEngagementEnabled](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.isfocusengagementenabled), 
[Control.IsTextScaleFactorEnabled](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.istextscalefactorenabled), 
[Control.Padding](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.padding), 
[Control.RequiresPointer](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.requirespointer), 
[Control.TabNavigation](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.tabnavigation), 
[Control.Template](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.template), 
[Control.VerticalContentAlignment](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.verticalcontentalignment), 
[Control.FocusDisengaged](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.focusdisengaged), 
[Control.FocusEngaged](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.focusengaged), 
[Control.IsEnabledChanged](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.controls.control.isenabledchanged), 
[FrameworkElement.As<I\>\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.as), 
[FrameworkElement.DeferTree\(DependencyObject\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.defertree), 
[FrameworkElement.FromAbi\(IntPtr\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.fromabi), 
[FrameworkElement.Equals\(FrameworkElement\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.equals\#microsoft\-ui\-xaml\-frameworkelement\-equals\(microsoft\-ui\-xaml\-frameworkelement\)), 
[FrameworkElement.Equals\(object\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.equals\#microsoft\-ui\-xaml\-frameworkelement\-equals\(system\-object\)), 
[FrameworkElement.GetHashCode\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.gethashcode), 
[FrameworkElement.FindName\(string\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.findname), 
[FrameworkElement.SetBinding\(DependencyProperty, BindingBase\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.setbinding), 
[FrameworkElement.GetBindingExpression\(DependencyProperty\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.getbindingexpression), 
[FrameworkElement.ActualHeightProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.actualheightproperty), 
[FrameworkElement.ActualThemeProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.actualthemeproperty), 
[FrameworkElement.ActualWidthProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.actualwidthproperty), 
[FrameworkElement.AllowFocusOnInteractionProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.allowfocusoninteractionproperty), 
[FrameworkElement.AllowFocusWhenDisabledProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.allowfocuswhendisabledproperty), 
[FrameworkElement.DataContextProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.datacontextproperty), 
[FrameworkElement.FlowDirectionProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.flowdirectionproperty), 
[FrameworkElement.FocusVisualMarginProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.focusvisualmarginproperty), 
[FrameworkElement.FocusVisualPrimaryBrushProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.focusvisualprimarybrushproperty), 
[FrameworkElement.FocusVisualPrimaryThicknessProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.focusvisualprimarythicknessproperty), 
[FrameworkElement.FocusVisualSecondaryBrushProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.focusvisualsecondarybrushproperty), 
[FrameworkElement.FocusVisualSecondaryThicknessProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.focusvisualsecondarythicknessproperty), 
[FrameworkElement.HeightProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.heightproperty), 
[FrameworkElement.HorizontalAlignmentProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.horizontalalignmentproperty), 
[FrameworkElement.LanguageProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.languageproperty), 
[FrameworkElement.MarginProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.marginproperty), 
[FrameworkElement.MaxHeightProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.maxheightproperty), 
[FrameworkElement.MaxWidthProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.maxwidthproperty), 
[FrameworkElement.MinHeightProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.minheightproperty), 
[FrameworkElement.MinWidthProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.minwidthproperty), 
[FrameworkElement.NameProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.nameproperty), 
[FrameworkElement.RequestedThemeProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.requestedthemeproperty), 
[FrameworkElement.StyleProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.styleproperty), 
[FrameworkElement.TagProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.tagproperty), 
[FrameworkElement.VerticalAlignmentProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.verticalalignmentproperty), 
[FrameworkElement.WidthProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.widthproperty), 
[FrameworkElement.ActualHeight](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.actualheight), 
[FrameworkElement.ActualTheme](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.actualtheme), 
[FrameworkElement.ActualWidth](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.actualwidth), 
[FrameworkElement.AllowFocusOnInteraction](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.allowfocusoninteraction), 
[FrameworkElement.AllowFocusWhenDisabled](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.allowfocuswhendisabled), 
[FrameworkElement.BaseUri](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.baseuri), 
[FrameworkElement.DataContext](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.datacontext), 
[FrameworkElement.FlowDirection](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.flowdirection), 
[FrameworkElement.FocusVisualMargin](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.focusvisualmargin), 
[FrameworkElement.FocusVisualPrimaryBrush](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.focusvisualprimarybrush), 
[FrameworkElement.FocusVisualPrimaryThickness](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.focusvisualprimarythickness), 
[FrameworkElement.FocusVisualSecondaryBrush](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.focusvisualsecondarybrush), 
[FrameworkElement.FocusVisualSecondaryThickness](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.focusvisualsecondarythickness), 
[FrameworkElement.Height](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.height), 
[FrameworkElement.HorizontalAlignment](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.horizontalalignment), 
[FrameworkElement.IsLoaded](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.isloaded), 
[FrameworkElement.Language](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.language), 
[FrameworkElement.Margin](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.margin), 
[FrameworkElement.MaxHeight](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.maxheight), 
[FrameworkElement.MaxWidth](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.maxwidth), 
[FrameworkElement.MinHeight](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.minheight), 
[FrameworkElement.MinWidth](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.minwidth), 
[FrameworkElement.Name](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.name), 
[FrameworkElement.Parent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.parent), 
[FrameworkElement.RequestedTheme](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.requestedtheme), 
[FrameworkElement.Resources](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.resources), 
[FrameworkElement.Style](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.style), 
[FrameworkElement.Tag](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.tag), 
[FrameworkElement.Triggers](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.triggers), 
[FrameworkElement.VerticalAlignment](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.verticalalignment), 
[FrameworkElement.Width](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.width), 
[FrameworkElement.ActualThemeChanged](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.actualthemechanged), 
[FrameworkElement.DataContextChanged](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.datacontextchanged), 
[FrameworkElement.EffectiveViewportChanged](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.effectiveviewportchanged), 
[FrameworkElement.LayoutUpdated](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.layoutupdated), 
[FrameworkElement.Loaded](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.loaded), 
[FrameworkElement.Loading](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.loading), 
[FrameworkElement.SizeChanged](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.sizechanged), 
[FrameworkElement.Unloaded](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.frameworkelement.unloaded), 
[UIElement.As<I\>\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.as), 
[UIElement.TryStartDirectManipulation\(Pointer\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.trystartdirectmanipulation), 
[UIElement.RegisterAsScrollPort\(UIElement\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.registerasscrollport), 
[UIElement.FromAbi\(IntPtr\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.fromabi), 
[UIElement.Equals\(UIElement\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.equals\#microsoft\-ui\-xaml\-uielement\-equals\(microsoft\-ui\-xaml\-uielement\)), 
[UIElement.Equals\(object\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.equals\#microsoft\-ui\-xaml\-uielement\-equals\(system\-object\)), 
[UIElement.GetHashCode\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.gethashcode), 
[UIElement.Measure\(Size\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.measure), 
[UIElement.Arrange\(Rect\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.arrange), 
[UIElement.CapturePointer\(Pointer\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.capturepointer), 
[UIElement.ReleasePointerCapture\(Pointer\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.releasepointercapture), 
[UIElement.ReleasePointerCaptures\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.releasepointercaptures), 
[UIElement.AddHandler\(RoutedEvent, object, bool\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.addhandler), 
[UIElement.RemoveHandler\(RoutedEvent, object\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.removehandler), 
[UIElement.TransformToVisual\(UIElement\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.transformtovisual), 
[UIElement.InvalidateMeasure\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.invalidatemeasure), 
[UIElement.InvalidateArrange\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.invalidatearrange), 
[UIElement.UpdateLayout\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.updatelayout), 
[UIElement.CancelDirectManipulations\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.canceldirectmanipulations), 
[UIElement.StartDragAsync\(PointerPoint\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.startdragasync), 
[UIElement.StartBringIntoView\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.startbringintoview\#microsoft\-ui\-xaml\-uielement\-startbringintoview), 
[UIElement.StartBringIntoView\(BringIntoViewOptions\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.startbringintoview\#microsoft\-ui\-xaml\-uielement\-startbringintoview\(microsoft\-ui\-xaml\-bringintoviewoptions\)), 
[UIElement.TryInvokeKeyboardAccelerator\(ProcessKeyboardAcceleratorEventArgs\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.tryinvokekeyboardaccelerator), 
[UIElement.Focus\(FocusState\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.focus), 
[UIElement.StartAnimation\(ICompositionAnimationBase\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.startanimation), 
[UIElement.StopAnimation\(ICompositionAnimationBase\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.stopanimation), 
[UIElement.PopulatePropertyInfo\(string, AnimationPropertyInfo\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.populatepropertyinfo), 
[UIElement.GetVisualInternal\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.getvisualinternal), 
[UIElement.AccessKeyProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.accesskeyproperty), 
[UIElement.AccessKeyScopeOwnerProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.accesskeyscopeownerproperty), 
[UIElement.AllowDropProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.allowdropproperty), 
[UIElement.BringIntoViewRequestedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.bringintoviewrequestedevent), 
[UIElement.CacheModeProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.cachemodeproperty), 
[UIElement.CanBeScrollAnchorProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.canbescrollanchorproperty), 
[UIElement.CanDragProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.candragproperty), 
[UIElement.CharacterReceivedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.characterreceivedevent), 
[UIElement.ClipProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.clipproperty), 
[UIElement.CompositeModeProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.compositemodeproperty), 
[UIElement.ContextFlyoutProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.contextflyoutproperty), 
[UIElement.ContextRequestedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.contextrequestedevent), 
[UIElement.DoubleTappedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.doubletappedevent), 
[UIElement.DragEnterEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.dragenterevent), 
[UIElement.DragLeaveEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.dragleaveevent), 
[UIElement.DragOverEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.dragoverevent), 
[UIElement.DropEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.dropevent), 
[UIElement.ExitDisplayModeOnAccessKeyInvokedProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.exitdisplaymodeonaccesskeyinvokedproperty), 
[UIElement.FocusStateProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.focusstateproperty), 
[UIElement.GettingFocusEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.gettingfocusevent), 
[UIElement.HighContrastAdjustmentProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.highcontrastadjustmentproperty), 
[UIElement.HoldingEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.holdingevent), 
[UIElement.IsAccessKeyScopeProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.isaccesskeyscopeproperty), 
[UIElement.IsDoubleTapEnabledProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.isdoubletapenabledproperty), 
[UIElement.IsHitTestVisibleProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.ishittestvisibleproperty), 
[UIElement.IsHoldingEnabledProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.isholdingenabledproperty), 
[UIElement.IsRightTapEnabledProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.isrighttapenabledproperty), 
[UIElement.IsTabStopProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.istabstopproperty), 
[UIElement.IsTapEnabledProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.istapenabledproperty), 
[UIElement.KeyDownEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keydownevent), 
[UIElement.KeyTipHorizontalOffsetProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keytiphorizontaloffsetproperty), 
[UIElement.KeyTipPlacementModeProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keytipplacementmodeproperty), 
[UIElement.KeyTipTargetProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keytiptargetproperty), 
[UIElement.KeyTipVerticalOffsetProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keytipverticaloffsetproperty), 
[UIElement.KeyUpEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keyupevent), 
[UIElement.KeyboardAcceleratorPlacementModeProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keyboardacceleratorplacementmodeproperty), 
[UIElement.KeyboardAcceleratorPlacementTargetProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keyboardacceleratorplacementtargetproperty), 
[UIElement.LightsProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.lightsproperty), 
[UIElement.LosingFocusEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.losingfocusevent), 
[UIElement.ManipulationCompletedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationcompletedevent), 
[UIElement.ManipulationDeltaEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationdeltaevent), 
[UIElement.ManipulationInertiaStartingEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationinertiastartingevent), 
[UIElement.ManipulationModeProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationmodeproperty), 
[UIElement.ManipulationStartedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationstartedevent), 
[UIElement.ManipulationStartingEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationstartingevent), 
[UIElement.NoFocusCandidateFoundEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.nofocuscandidatefoundevent), 
[UIElement.OpacityProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.opacityproperty), 
[UIElement.PointerCanceledEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointercanceledevent), 
[UIElement.PointerCaptureLostEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointercapturelostevent), 
[UIElement.PointerCapturesProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointercapturesproperty), 
[UIElement.PointerEnteredEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointerenteredevent), 
[UIElement.PointerExitedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointerexitedevent), 
[UIElement.PointerMovedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointermovedevent), 
[UIElement.PointerPressedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointerpressedevent), 
[UIElement.PointerReleasedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointerreleasedevent), 
[UIElement.PointerWheelChangedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointerwheelchangedevent), 
[UIElement.PreviewKeyDownEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.previewkeydownevent), 
[UIElement.PreviewKeyUpEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.previewkeyupevent), 
[UIElement.ProjectionProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.projectionproperty), 
[UIElement.RenderTransformOriginProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.rendertransformoriginproperty), 
[UIElement.RenderTransformProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.rendertransformproperty), 
[UIElement.RightTappedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.righttappedevent), 
[UIElement.ShadowProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.shadowproperty), 
[UIElement.TabFocusNavigationProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.tabfocusnavigationproperty), 
[UIElement.TabIndexProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.tabindexproperty), 
[UIElement.TappedEvent](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.tappedevent), 
[UIElement.Transform3DProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.transform3dproperty), 
[UIElement.TransitionsProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.transitionsproperty), 
[UIElement.UseLayoutRoundingProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.uselayoutroundingproperty), 
[UIElement.UseSystemFocusVisualsProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.usesystemfocusvisualsproperty), 
[UIElement.VisibilityProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.visibilityproperty), 
[UIElement.XYFocusDownNavigationStrategyProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusdownnavigationstrategyproperty), 
[UIElement.XYFocusDownProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusdownproperty), 
[UIElement.XYFocusKeyboardNavigationProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocuskeyboardnavigationproperty), 
[UIElement.XYFocusLeftNavigationStrategyProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusleftnavigationstrategyproperty), 
[UIElement.XYFocusLeftProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusleftproperty), 
[UIElement.XYFocusRightNavigationStrategyProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusrightnavigationstrategyproperty), 
[UIElement.XYFocusRightProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusrightproperty), 
[UIElement.XYFocusUpNavigationStrategyProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusupnavigationstrategyproperty), 
[UIElement.XYFocusUpProperty](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusupproperty), 
[UIElement.AccessKey](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.accesskey), 
[UIElement.AccessKeyScopeOwner](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.accesskeyscopeowner), 
[UIElement.ActualOffset](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.actualoffset), 
[UIElement.ActualSize](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.actualsize), 
[UIElement.AllowDrop](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.allowdrop), 
[UIElement.CacheMode](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.cachemode), 
[UIElement.CanBeScrollAnchor](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.canbescrollanchor), 
[UIElement.CanDrag](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.candrag), 
[UIElement.CenterPoint](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.centerpoint), 
[UIElement.Clip](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.clip), 
[UIElement.CompositeMode](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.compositemode), 
[UIElement.ContextFlyout](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.contextflyout), 
[UIElement.DesiredSize](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.desiredsize), 
[UIElement.ExitDisplayModeOnAccessKeyInvoked](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.exitdisplaymodeonaccesskeyinvoked), 
[UIElement.FocusState](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.focusstate), 
[UIElement.HighContrastAdjustment](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.highcontrastadjustment), 
[UIElement.IsAccessKeyScope](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.isaccesskeyscope), 
[UIElement.IsDoubleTapEnabled](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.isdoubletapenabled), 
[UIElement.IsHitTestVisible](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.ishittestvisible), 
[UIElement.IsHoldingEnabled](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.isholdingenabled), 
[UIElement.IsRightTapEnabled](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.isrighttapenabled), 
[UIElement.IsTabStop](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.istabstop), 
[UIElement.IsTapEnabled](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.istapenabled), 
[UIElement.KeyTipHorizontalOffset](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keytiphorizontaloffset), 
[UIElement.KeyTipPlacementMode](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keytipplacementmode), 
[UIElement.KeyTipTarget](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keytiptarget), 
[UIElement.KeyTipVerticalOffset](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keytipverticaloffset), 
[UIElement.KeyboardAcceleratorPlacementMode](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keyboardacceleratorplacementmode), 
[UIElement.KeyboardAcceleratorPlacementTarget](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keyboardacceleratorplacementtarget), 
[UIElement.KeyboardAccelerators](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keyboardaccelerators), 
[UIElement.Lights](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.lights), 
[UIElement.ManipulationMode](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationmode), 
[UIElement.Opacity](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.opacity), 
[UIElement.OpacityTransition](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.opacitytransition), 
[UIElement.PointerCaptures](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointercaptures), 
[UIElement.Projection](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.projection), 
[UIElement.RasterizationScale](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.rasterizationscale), 
[UIElement.RenderSize](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.rendersize), 
[UIElement.RenderTransform](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.rendertransform), 
[UIElement.RenderTransformOrigin](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.rendertransformorigin), 
[UIElement.Rotation](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.rotation), 
[UIElement.RotationAxis](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.rotationaxis), 
[UIElement.RotationTransition](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.rotationtransition), 
[UIElement.Scale](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.scale), 
[UIElement.ScaleTransition](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.scaletransition), 
[UIElement.Shadow](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.shadow), 
[UIElement.TabFocusNavigation](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.tabfocusnavigation), 
[UIElement.TabIndex](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.tabindex), 
[UIElement.Transform3D](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.transform3d), 
[UIElement.TransformMatrix](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.transformmatrix), 
[UIElement.Transitions](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.transitions), 
[UIElement.Translation](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.translation), 
[UIElement.TranslationTransition](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.translationtransition), 
[UIElement.UseLayoutRounding](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.uselayoutrounding), 
[UIElement.UseSystemFocusVisuals](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.usesystemfocusvisuals), 
[UIElement.Visibility](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.visibility), 
[UIElement.XYFocusDown](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusdown), 
[UIElement.XYFocusDownNavigationStrategy](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusdownnavigationstrategy), 
[UIElement.XYFocusKeyboardNavigation](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocuskeyboardnavigation), 
[UIElement.XYFocusLeft](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusleft), 
[UIElement.XYFocusLeftNavigationStrategy](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusleftnavigationstrategy), 
[UIElement.XYFocusRight](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusright), 
[UIElement.XYFocusRightNavigationStrategy](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusrightnavigationstrategy), 
[UIElement.XYFocusUp](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusup), 
[UIElement.XYFocusUpNavigationStrategy](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xyfocusupnavigationstrategy), 
[UIElement.XamlRoot](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.xamlroot), 
[UIElement.AccessKeyDisplayDismissed](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.accesskeydisplaydismissed), 
[UIElement.AccessKeyDisplayRequested](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.accesskeydisplayrequested), 
[UIElement.AccessKeyInvoked](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.accesskeyinvoked), 
[UIElement.BringIntoViewRequested](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.bringintoviewrequested), 
[UIElement.CharacterReceived](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.characterreceived), 
[UIElement.ContextCanceled](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.contextcanceled), 
[UIElement.ContextRequested](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.contextrequested), 
[UIElement.DoubleTapped](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.doubletapped), 
[UIElement.DragEnter](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.dragenter), 
[UIElement.DragLeave](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.dragleave), 
[UIElement.DragOver](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.dragover), 
[UIElement.DragStarting](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.dragstarting), 
[UIElement.Drop](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.drop), 
[UIElement.DropCompleted](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.dropcompleted), 
[UIElement.GettingFocus](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.gettingfocus), 
[UIElement.GotFocus](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.gotfocus), 
[UIElement.Holding](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.holding), 
[UIElement.KeyDown](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keydown), 
[UIElement.KeyUp](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.keyup), 
[UIElement.LosingFocus](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.losingfocus), 
[UIElement.LostFocus](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.lostfocus), 
[UIElement.ManipulationCompleted](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationcompleted), 
[UIElement.ManipulationDelta](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationdelta), 
[UIElement.ManipulationInertiaStarting](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationinertiastarting), 
[UIElement.ManipulationStarted](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationstarted), 
[UIElement.ManipulationStarting](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.manipulationstarting), 
[UIElement.NoFocusCandidateFound](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.nofocuscandidatefound), 
[UIElement.PointerCanceled](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointercanceled), 
[UIElement.PointerCaptureLost](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointercapturelost), 
[UIElement.PointerEntered](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointerentered), 
[UIElement.PointerExited](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointerexited), 
[UIElement.PointerMoved](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointermoved), 
[UIElement.PointerPressed](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointerpressed), 
[UIElement.PointerReleased](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointerreleased), 
[UIElement.PointerWheelChanged](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.pointerwheelchanged), 
[UIElement.PreviewKeyDown](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.previewkeydown), 
[UIElement.PreviewKeyUp](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.previewkeyup), 
[UIElement.ProcessKeyboardAccelerators](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.processkeyboardaccelerators), 
[UIElement.RightTapped](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.righttapped), 
[UIElement.Tapped](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.uielement.tapped), 
[DependencyObject.FromAbi\(IntPtr\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.fromabi), 
[DependencyObject.Equals\(DependencyObject\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.equals\#microsoft\-ui\-xaml\-dependencyobject\-equals\(microsoft\-ui\-xaml\-dependencyobject\)), 
[DependencyObject.Equals\(object\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.equals\#microsoft\-ui\-xaml\-dependencyobject\-equals\(system\-object\)), 
[DependencyObject.GetHashCode\(\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.gethashcode), 
[DependencyObject.GetValue\(DependencyProperty\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.getvalue), 
[DependencyObject.SetValue\(DependencyProperty, object\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.setvalue), 
[DependencyObject.ClearValue\(DependencyProperty\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.clearvalue), 
[DependencyObject.ReadLocalValue\(DependencyProperty\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.readlocalvalue), 
[DependencyObject.GetAnimationBaseValue\(DependencyProperty\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.getanimationbasevalue), 
[DependencyObject.RegisterPropertyChangedCallback\(DependencyProperty, DependencyPropertyChangedCallback\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.registerpropertychangedcallback), 
[DependencyObject.UnregisterPropertyChangedCallback\(DependencyProperty, long\)](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.unregisterpropertychangedcallback), 
[DependencyObject.Dispatcher](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.dispatcher), 
[DependencyObject.DispatcherQueue](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.dependencyobject.dispatcherqueue), 
[object.Equals\(object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\)), 
[object.Equals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.equals\#system\-object\-equals\(system\-object\-system\-object\)), 
[object.GetHashCode\(\)](https://learn.microsoft.com/dotnet/api/system.object.gethashcode), 
[object.GetType\(\)](https://learn.microsoft.com/dotnet/api/system.object.gettype), 
[object.ReferenceEquals\(object?, object?\)](https://learn.microsoft.com/dotnet/api/system.object.referenceequals), 
[object.ToString\(\)](https://learn.microsoft.com/dotnet/api/system.object.tostring)

## Examples

<pre><code class="lang-csharp">&lt;Window x:Class="WinUIApp1.MainWindow"
        xmlns="http://schemas.microsoft.com/winfx/2006/xaml/presentation"
        xmlns:x="http://schemas.microsoft.com/winfx/2006/xaml"
        xmlns:local="using:WinUIApp1"
        xmlns:mc="http://schemas.openxmlformats.org/markup-compatibility/2006"
        xmlns:d="http://schemas.microsoft.com/expression/blend/2008"
        xmlns:winui3="using:DotNetBrowser.WinUi3"
        mc:Ignorable="d"&gt;

    &lt;Grid&gt;
        &lt;local:BrowserTabs x:Name="tabs" VerticalAlignment="Stretch" VerticalContentAlignment="Stretch" /&gt;
    &lt;/Grid&gt;
&lt;/Window&gt;</code></pre>
<pre><code class="lang-csharp">public partial class MainWindow : Window
{
    private IEngine engine;
    private IBrowser browser;

    public MainWindow()
    {
        try
        {
            InitializeComponent();

            Task.Run(() =&gt; {
                engine = EngineFactory.Create(new EngineOptions.Builder()
                {
                    RenderingMode = RenderingMode.HardwareAccelerated
                }.Build());
                browser = engine.CreateBrowser();

            }).ContinueWith((t) =&gt;
            {
                BrowserView.InitializeFrom(browser);
                BrowserView.Window = this;
                browser.Navigation.LoadUrl("https://www.teamdev.com/");
            }, TaskScheduler.FromCurrentSynchronizationContext());
        }
        catch (Exception ex)
        {
            Debug.WriteLine(ex);
        }
    }

    private void Window_Closing(object sender, System.ComponentModel.CancelEventArgs e)
    {
        engine.Dispose();
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

### <a id="DotNetBrowser_WinUi3_BrowserView__ctor"></a> BrowserView\(\)

Initializes a new instance of the <xref href="DotNetBrowser.WinUi3.BrowserView" data-throw-if-not-resolved="false"></xref> class.

```csharp
public BrowserView()
```

## Properties

### <a id="DotNetBrowser_WinUi3_BrowserView_MenuItems"></a> MenuItems

The collection of the current context menu items.

```csharp
public ObservableCollection<MenuItemViewModel> MenuItems { get; }
```

#### Property Value

 [ObservableCollection](https://learn.microsoft.com/dotnet/api/system.collections.objectmodel.observablecollection\-1)<[MenuItemViewModel](DotNetBrowser.WinUi3.ContextMenu.MenuItemViewModel.md)\>

### <a id="DotNetBrowser_WinUi3_BrowserView_SaveCreditCardHandler"></a> SaveCreditCardHandler

This handler is used when the user is prompted to save the credit cards in the credit card store,
if a different handler was not configured for the browser.

```csharp
public IHandler<SaveCreditCardParameters, SaveCreditCardResponse> SaveCreditCardHandler { get; }
```

#### Property Value

 IHandler<SaveCreditCardParameters, SaveCreditCardResponse\>

### <a id="DotNetBrowser_WinUi3_BrowserView_SavePasswordHandler"></a> SavePasswordHandler

This handler is used when the user is prompted to save the credentials in the password store,
if a different handler was not configured for the browser.

```csharp
public IHandler<SavePasswordParameters, SavePasswordResponse> SavePasswordHandler { get; }
```

#### Property Value

 IHandler<SavePasswordParameters, SavePasswordResponse\>

### <a id="DotNetBrowser_WinUi3_BrowserView_SaveUserDataProfileHandler"></a> SaveUserDataProfileHandler

This handler is used when the user is prompted to save the user data profiles in the user data profile store,
if a different handler was not configured for the browser.

```csharp
public IHandler<SaveUserDataProfileParameters, SaveUserDataProfileResponse> SaveUserDataProfileHandler { get; }
```

#### Property Value

 IHandler<SaveUserDataProfileParameters, SaveUserDataProfileResponse\>

### <a id="DotNetBrowser_WinUi3_BrowserView_SelectCertificateHandler"></a> SelectCertificateHandler

This handler is used when the client SSL certificate should be selected,
if a different handler was not configured for the browser.

```csharp
public IHandler<SelectCertificateParameters, SelectCertificateResponse> SelectCertificateHandler { get; }
```

#### Property Value

 IHandler<SelectCertificateParameters, SelectCertificateResponse\>

### <a id="DotNetBrowser_WinUi3_BrowserView_ShowContextMenuHandler"></a> ShowContextMenuHandler

The default context menu handler implementation for this browser view.

```csharp
public IHandler<ShowContextMenuParameters, ShowContextMenuResponse> ShowContextMenuHandler { get; }
```

#### Property Value

 IHandler<ShowContextMenuParameters, ShowContextMenuResponse\>

### <a id="DotNetBrowser_WinUi3_BrowserView_StartDownloadHandler"></a> StartDownloadHandler

This handler is used when the browser is about to start downloading the file,
if a different handler was not configured for the browser.

```csharp
public IHandler<StartDownloadParameters, StartDownloadResponse> StartDownloadHandler { get; }
```

#### Property Value

 IHandler<StartDownloadParameters, StartDownloadResponse\>

### <a id="DotNetBrowser_WinUi3_BrowserView_UpdatePasswordHandler"></a> UpdatePasswordHandler

This handler is used when the user is prompted to update the password in the password store,
if a different handler was not configured for the browser.

```csharp
public IHandler<UpdatePasswordParameters, UpdatePasswordResponse> UpdatePasswordHandler { get; }
```

#### Property Value

 IHandler<UpdatePasswordParameters, UpdatePasswordResponse\>

### <a id="DotNetBrowser_WinUi3_BrowserView_UpdateUserDataProfileHandler"></a> UpdateUserDataProfileHandler

This handler is used when the user is prompted to update the user data profile in the user data profile store,
if a different handler was not configured for the browser.

```csharp
public IHandler<UpdateUserDataProfileParameters, UpdateUserDataProfileResponse> UpdateUserDataProfileHandler { get; }
```

#### Property Value

 IHandler<UpdateUserDataProfileParameters, UpdateUserDataProfileResponse\>

## Methods

### <a id="DotNetBrowser_WinUi3_BrowserView_Focus_Microsoft_UI_Xaml_FocusState_"></a> Focus\(FocusState\)

Moves keyboard focus to this browser view.

```csharp
public bool Focus(FocusState value)
```

#### Parameters

`value` [FocusState](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.focusstate)

The reason focus was requested, used to determine which focus indicator to display.

#### Returns

 [bool](https://learn.microsoft.com/dotnet/api/system.boolean)

<a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">true</a> if the input focus request was successful; otherwise, <a href="https://learn.microsoft.com/dotnet/csharp/language-reference/builtin-types/bool">false</a>.

#### Remarks

This view itself is not a tab stop (<code>IsTabStop</code> defaults to <code>false</code> on
<xref href="Microsoft.UI.Xaml.Controls.ContentControl" data-throw-if-not-resolved="false"></xref>, so the embedded browser content occupies a single Tab
stop instead of two); the inherited <xref href="Microsoft.UI.Xaml.UIElement.Focus(Microsoft.UI.Xaml.FocusState)" data-throw-if-not-resolved="false"></xref> is
therefore a no-op here. This hides it and forwards focus directly to the hardware or
off-screen content view instead.

### <a id="DotNetBrowser_WinUi3_BrowserView_InitializeComponent"></a> InitializeComponent\(\)

InitializeComponent()

```csharp
public void InitializeComponent()
```

### <a id="DotNetBrowser_WinUi3_BrowserView_SetWindow_Microsoft_UI_Xaml_Window_"></a> SetWindow\(Window\)

Sets the <xref href="Microsoft.UI.Xaml.Window" data-throw-if-not-resolved="false"></xref> instance that represent the application window.

```csharp
public void SetWindow(Window window)
```

#### Parameters

`window` [Window](https://learn.microsoft.com/windows/windows\-app\-sdk/api/winrt/microsoft.ui.xaml.window)

The <xref href="Microsoft.UI.Xaml.Window" data-throw-if-not-resolved="false"></xref> instance that represent the application window.

