
# Spell Checker

**Lead**
This documents describes how to configure spell checking with the required dictionaries, add or remove words from a custom dictionary, disable spell checking and more.


By default, spell checking is enabled and configured to use the `en-US` dictionary. Spell checker reviews the text in all text fields, as well as text areas, on the loaded web page and highlights all misspelled words. Spellschecker service is associated with profiles. To access and configure the spell checker for the specific `Profile`, use the `ISpellChecker` interface:


**C#**
```csharp
ISpellChecker spellChecker = profile.SpellChecker;
```

**VB**
```vb
Dim spellChecker As ISpellChecker = profile.SpellChecker
```



Another option is to use the `Engine.Profiles.Default.SpellChecker` property which returns the instance of  `ISpellChecker` service associated with the default profile.

## Adding languages

The spell checker can check the text in different languages on a single web page. To configure the required language, use the `spellChecker.Languages.Add()` method. Chromium downloads the dictionary files automatically from its web servers.


**C#**
```csharp
spellChecker.Languages.Add(Language.EnglishUs);
```

**VB**
```vb
spellChecker.Languages.Add(Language.EnglishUs)
```



**Note**
If Chromium cannot find the necessary dictionary, the `LanguageNotAvailableException` will be thrown.


**Note**
Languages configuration and dictionaries are stored in the [user data](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#user-data-directory). If you configure `IEngine` to use a specific user data directory, it will remember the language settings and restore them next time.


In order to wait until the corresponding language is laoded from the user data directory, use the following code:


**C#**
```csharp
spellChecker.Languages.Add(Language.EnglishUs).Wait();
```

**VB**
```vb
spellChecker.Languages.Add(Language.EnglishUs).Wait()
```



## Removing languages

Use the `spellChecker.Languages.Remove()` method to stop spell checking for a particular language:


**C#**
```csharp
spellChecker.Languages.Remove(Language.EnglishUs);
```

**VB**
```vb
spellChecker.Languages.Remove(Language.EnglishUs)
```



## Getting languages

To get the list of languages used for spellchecking, use the following code:


**C#**
```csharp
ISpellChecker spellChecker = Engine.Profiles.Default.SpellChecker;
IReadOnlyList<Language> languages = spellChecker.Languages.All;
```

**VB**
```vb
Dim spellChecker As ISpellChecker = Engine.Profiles.Default.SpellChecker
Dim languages As IReadOnlyList(Of Language) = spellChecker.Languages.All
```



## Custom dictionary

The spell checker supports the custom dictionary. You can access a custom dictionary using the `SpellChecker.CustomDictionary` property.

For example:


**C#**
```csharp
ISpellCheckDictionary dictionary = spellChecker.CustomDictionary;
```

**VB**
```vb
Dim dictionary As ISpellCheckDictionary = spellChecker.CustomDictionary
```



### Adding a word

You can add words to the custom dictionary using the `Add(string)` method:


**C#**
```csharp
bool success = dictionary.Add("John");
```

**VB**
```vb
Dim success As Boolean = dictionary.Add("John")
```



**Note**
DotNetBrowser has the following requirements for the words added to the custom dictionary: 
 - UTF-8 word encoding;
 - word length between 1 and 99 bytes; 
 - no leading or trailing ASCII whitespace.


### Removing a word

To remove a word from the custom dictionary, use the `Remove(string)` method as shown in the code sample below:


**C#**
```csharp
bool success = dictionary.Remove("John");
```

**VB**
```vb
Dim success As Boolean = dictionary.Remove("John")
```



## Disabling spell checking

By default, spell checking is enabled. You can disable it using the code sample below:


**C#**
```csharp
spellChecker.Enabled = false;
```

**VB**
```vb
spellChecker.Enabled = False
```



## Context menu

You can display context menu with suggestions when a user right clicks the highlighted misspelled word on the loaded web page. Use the `IBrowser.ShowContextMenuHandler` to display context menu with suggestions and menu item to add the misspelled word to the custom dictionary.

### WinForms

The code sample below demonstrates how to create and display WinForms context menu with suggestions and the **Add to Dictionary** menu item. Using this context menu, you can replace the misspelled word with one of the suggestions or add it to the custom dictionary.


**C#**

```csharp
browser.ShowContextMenuHandler =
    new AsyncHandler<ShowContextMenuParameters,
        ShowContextMenuResponse>(ShowMenu);
```

**VB**

```vb
browser.ShowContextMenuHandler =
     New AsyncHandler (Of ShowContextMenuParameters, ShowContextMenuResponse)(
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
            IEnumerable<string> suggestions = spellCheckMenu.DictionarySuggestions;
            if (suggestions != null)
            {
                // Add menu items with suggestions.
                foreach (string suggestion in suggestions)
                {
                    popupMenu.Items.Add(BuildMenuItem(suggestion, true, delegate
                    {
                        browser.ReplaceMisspelledWord(suggestion);
                        tcs.TrySetResult(ShowContextMenuResponse.Close());
                    }));
                }
            }

            // Add "Add to Dictionary" menu item.
            string addToDictionary =
                spellCheckMenu.AddToDictionaryMenuItemText ?? "Add to Dictionary";

            popupMenu.Items.Add(BuildMenuItem(addToDictionary, true, delegate
            {
                if (!string.IsNullOrWhiteSpace(spellCheckMenu.MisspelledWord))
                {
                    engine.Profiles.Default.SpellChecker?.CustomDictionary
                         ?.Add(spellCheckMenu.MisspelledWord);
                }

                tcs.TrySetResult(ShowContextMenuResponse.Close());
            }));

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
            Dim suggestions As IEnumerable(Of String) =
                    spellCheckMenu.DictionarySuggestions

            If suggestions IsNot Nothing Then
                ' Add menu items with suggestions.
                For Each suggestion As String In suggestions
                    popupMenu.Items.Add(BuildMenuItem(suggestion, True, Sub()
                        browser.ReplaceMisspelledWord(suggestion)
                        tcs.TrySetResult(ShowContextMenuResponse.Close())
                    End Sub))
                Next suggestion
            End If

            ' Add "Add to Dictionary" menu item.
            Dim addToDictionary As String =
                If (spellCheckMenu.AddToDictionaryMenuItemText, "Add to Dictionary")

            popupMenu.Items.Add(BuildMenuItem(addToDictionary, True, Sub()
                If Not String.IsNullOrWhiteSpace(spellCheckMenu.MisspelledWord) Then
                    engine.Profiles.Default.SpellChecker?.CustomDictionary? .Add(
                        spellCheckMenu.MisspelledWord)
                End If
                tcs.TrySetResult(ShowContextMenuResponse.Close())
            End Sub))

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
                Dim itemNotClicked As Boolean = args.CloseReason <>
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



If you right click a misspelled word, the context menu appears:
![WinForms Spell Checker Context Menu](https://teamdev.com/dotnetbrowser/img/articles/guides/spellchecker/winforms-context-menu.webp)

The complete example is available in our repo: [C#](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/csharp/winforms/ContextMenu.SpellCheck), [VB.NET](https://github.com/TeamDev-IP/DotNetBrowser-Examples/blob/master/vbnet/winforms/ContextMenu.SpellCheck).

### WPF

The code sample below demonstrates how to create and display a WPF context menu with suggestions and the **Add to Dictionary** menu item. Using this context menu, you can replace the misspelled word with one of the suggestions or add it to the custom dictionary.


**C#**

```csharp
browser.ShowContextMenuHandler =
    new AsyncHandler<ShowContextMenuParameters, 
                     ShowContextMenuResponse>(ShowContextMenu);
```

**VB**

```vb
browser.ShowContextMenuHandler =
    New AsyncHandler(Of ShowContextMenuParameters, ShowContextMenuResponse)(
        AddressOf ShowContextMenu)
```




**C#**

```csharp
private Task<ShowContextMenuResponse> ShowContextMenu(
    ShowContextMenuParameters parameters)
{
    TaskCompletionSource<ShowContextMenuResponse> tcs =
        new TaskCompletionSource<ShowContextMenuResponse>();

    SpellCheckMenu spellCheckMenu = parameters.SpellCheckMenu;
    WebView.Dispatcher?.BeginInvoke(new Action(() =>
    {
        System.Windows.Controls.ContextMenu popupMenu =
            new System.Windows.Controls.ContextMenu();

        IEnumerable<string> suggestions = spellCheckMenu.DictionarySuggestions;
        if (suggestions != null)
        {
            // Add menu items with suggestions.
            foreach (string suggestion in suggestions)
            {
                MenuItem menuItem =
                    BuildMenuItem(suggestion, true,
                                  delegate
                                  {
                                      browser.ReplaceMisspelledWord(suggestion);
                                      tcs.TrySetResult(ShowContextMenuResponse
                                                          .Close());
                                  });
                popupMenu.Items.Add(menuItem);
            }
        }

        // Add "Add to Dictionary" menu item.
        string addToDictionary =
            spellCheckMenu.AddToDictionaryMenuItemText ?? "Add to Dictionary";

        popupMenu.Items.Add(BuildMenuItem(addToDictionary, true, delegate
        {
            if (!string.IsNullOrWhiteSpace(spellCheckMenu.MisspelledWord))
            {
                engine.Profiles.Default.SpellChecker?.CustomDictionary
                     ?.Add(spellCheckMenu.MisspelledWord);
            }

            tcs.TrySetResult(ShowContextMenuResponse.Close());
        }));

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
    Dim spellCheckMenu As SpellCheckMenu = parameters.SpellCheckMenu
    WebView.Dispatcher?.BeginInvoke(New Action(Sub()
        Dim popupMenu As New Controls.ContextMenu()

        Dim suggestions As IEnumerable(Of String) = spellCheckMenu.DictionarySuggestions
        If suggestions IsNot Nothing Then
            ' Add menu items with suggestions.
            For Each suggestion As String In suggestions
                Dim menuItem As MenuItem = BuildMenuItem(suggestion, True, Sub()
                    browser.ReplaceMisspelledWord(suggestion)
                    tcs.TrySetResult(ShowContextMenuResponse.Close())
                End Sub)
                popupMenu.Items.Add(menuItem)
            Next suggestion
        End If

        ' Add "Add to Dictionary" menu item.
        Dim addToDictionary As String =
                If(spellCheckMenu.AddToDictionaryMenuItemText, "Add to Dictionary")

        popupMenu.Items.Add(BuildMenuItem(addToDictionary, True, Sub()
            If Not String.IsNullOrWhiteSpace(spellCheckMenu.MisspelledWord) Then
                engine.Profiles.Default.SpellChecker?.CustomDictionary?.Add(
                    spellCheckMenu.MisspelledWord)
            End If

            tcs.TrySetResult(ShowContextMenuResponse.Close())
        End Sub))
        AddHandler popupMenu.Closed, Sub(sender, args)
            tcs.TrySetResult(ShowContextMenuResponse.Close())
        End Sub

        popupMenu.IsOpen = True
    End Sub))
    Return tcs.Task
End Function
```



If you right click a misspelled word, the context menu appears:
![WPF Spell Checker Context Menu](https://teamdev.com/dotnetbrowser/img/articles/guides/spellchecker/wpf-context-menu.webp)

### Avalonia UI

The code sample below demonstrates how to create and display an Avalonia UI context menu with suggestions and the **Add to Dictionary** menu item. Using this context menu, you can replace the misspelled word with one of the suggestions or add it to the custom dictionary.


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

    SpellCheckMenu spellCheckMenu = parameters.SpellCheckMenu;
    Dispatcher.UIThread.InvokeAsync(() =>
    {
        Avalonia.Controls.ContextMenu? cm = new();
        cm.Placement = PlacementMode.Pointer;
        Point point = new Point(parameters.Location.X, parameters.Location.Y);
        cm.PlacementRect = new Rect(point, new Size(1, 1));

        IEnumerable<string> suggestions = spellCheckMenu.DictionarySuggestions;
        if (suggestions != null)
        {
            // Add menu items with suggestions.
            foreach (string suggestion in suggestions)
            {
                MenuItem menuItem =
                    BuildMenuItem(suggestion, true, true,
                                  delegate
                                  {
                                      browser.ReplaceMisspelledWord(suggestion);
                                      tcs.TrySetResult(ShowContextMenuResponse
                                         .Close());
                                  });
                cm.Items.Add(menuItem);
            }
        }

        // Add "Add to Dictionary" menu item.
        string addToDictionary =
            spellCheckMenu.AddToDictionaryMenuItemText ?? "Add to Dictionary";

        cm.Items.Add(BuildMenuItem(addToDictionary, true, true, delegate
        {
            if (!string.IsNullOrWhiteSpace(spellCheckMenu.MisspelledWord))
            {
                engine.Profiles.Default.SpellChecker?.CustomDictionary
                     ?.Add(spellCheckMenu.MisspelledWord);
            }

            tcs.TrySetResult(ShowContextMenuResponse.Close());
        }));

        cm.Closed += (s, a) => tcs.TrySetResult(ShowContextMenuResponse.Close());
        cm.Open(BrowserView);
    });
    return tcs.Task;
}
```

If you right click a misspelled word, the context menu appears:
![Avalonia Spell Checker Context Menu](https://teamdev.com/dotnetbrowser/img/articles/guides/spellchecker/avalonia-context-menu.webp)

## Spell checker events

When a text field or text area on the loaded web page is in focus, the spell checker automatically checks the text and highlights the misspelled words. To get notifications when the text has been checked, use the `IBrowser.SpellCheckCompleted` event as shown in the code sample below:


**C#**
```csharp
browser.SpellCheckCompleted += (s, e) => 
{
    // The text that has been checked.
    string text = e.CheckedText;
    // The list of the spell checking results.
    foreach(SpellCheckingResult spellCheckingResult in e.Results)
    {
        // The location of the first symbol in the mis-spelled word 
        // in the checked text that is considered as mis-spelled 
        // by the spell checker.
        uint location = spellCheckingResult.Location;
        // The length of the mis-spelled word in the checked text.
        uint length = spellCheckingResult.Length;
    }
};
```

**VB**
```vb
AddHandler browser.SpellCheckCompleted, Sub(s, e)
    ' The text that has been checked.
    Dim text As String = e.CheckedText
    ' The list of the spell checking results.
    For Each spellCheckingResult As SpellCheckingResult In e.Results
        ' The location of the first symbol in the mis-spelled word
        ' in the checked text that is considered as mis-spelled
        ' by the spell checker.
        Dim location As UInteger = spellCheckingResult.Location
        ' The length of the mis-spelled word in the checked text.
        Dim length As UInteger = spellCheckingResult.Length
    Next
End Sub
```


