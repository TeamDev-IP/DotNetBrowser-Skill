
# Migrating from 2.3 to 2.4

**Lead**
In DotNetBrowser 2.4 the Printing API was re-introduced. This caused a few API changes. In this migration guide we describe what API has been changed in 2.4 and what alternatives you should use instead.


## Added or updated API

### Printing

#### PrintHandler

The `PrintHandler` was replaced with `RequestPrintHandler` in DotNetBrowser 2.4.

**v2.3**


**C#**
```csharp
browser.PrintHandler =
    new Handler<PrintParameters, PrintResponse>(p =>
    {
        return PrintResponse.ShowPrintPreview();
    });
```

**VB**
```vb
browser.PrintHandler = 
    New Handler(Of PrintParameters, PrintResponse)(Function(p)
        Return PrintResponse.ShowPrintPreview()
End Function)
```



**v2.4**


**C#**
```csharp
browser.RequestPrintHandler =
    new Handler<RequestPrintParameters, RequestPrintResponse>(p =>
    {
        return RequestPrintResponse.ShowPrintPreview();
    });
```

**VB**
```vb
browser.RequestPrintHandler = 
    New Handler(Of RequestPrintParameters, RequestPrintResponse)(Function(p)
        Return RequestPrintResponse.ShowPrintPreview()
End Function)
```



### Authentication

The `AuthenticateParameters` class has been extended with the `Realm` property. This property can be used to obtain the realm of the authentication challenge. 
