
# Authentication

**Lead**
This guide provides the list of supported authentication types and describes how to handle various authentication requests.


## Proxy, Basic, Digest, and NTLM authentication

To handle Proxy, Basic, Digest or NTLM authentication, use the `AuthenticateHandler`. You can provide the required username and password programmatically, display a username/password prompt, or just cancel an authentication request.

To check whether the authentication request is issued by a proxy server, use the `AuthenticateParameters.IsProxy` property. See the code sample below:


**C#**
```csharp
network.AuthenticateHandler = new Handler<AuthenticateParameters, AuthenticateResponse>(p =>
{
    if (p.IsProxy)
    {
        // This authentication request is issued by a proxy server.
    }
    // ...
});
```

**VB**
```vb
network.AuthenticateHandler = 
    New Handler(Of AuthenticateParameters, AuthenticateResponse)(Function(p)
        If p.IsProxy Then
            ' This authentication request is issued by a proxy server.
        End If
        ' ...
    End Function)
```



The following code sample demonstrates how to provide the required credentials:


**C#**
```csharp
network.AuthenticateHandler = new Handler<AuthenticateParameters, AuthenticateResponse>(p =>
    AuthenticateResponse.Continue("<username>", "<password>"));
```

**VB**
```vb
network.AuthenticateHandler = 
    New Handler(Of AuthenticateParameters, AuthenticateResponse)(Function(p) 
        Return AuthenticateResponse.Continue("<username>", "<password>")
    End Function)
```



To cancel the authentication request, use the following approach:


**C#**
```csharp
network.AuthenticateHandler = new Handler<AuthenticateParameters, AuthenticateResponse>(p =>
    AuthenticateResponse.Cancel());
```

**VB**
```vb
network.AuthenticateHandler = 
    New Handler(Of AuthenticateParameters, AuthenticateResponse)(Function(p) 
        Return AuthenticateResponse.Cancel()
    End Function)
```



## HTTPS client certificate

At the start of an SSL or TLS session, the web server may require the client application to submit a client certificate for authentication. Upon receiving the certificate, the server uses it to identify the certificate's source and determine whether the client should be given an access.

If the web server is enabled with the client certificate authentication, only the users who attempt to connect from the clients with the valid client certificates succeed. 

By default, DotNetBrowser cancels all certificates. To perform authentication and select the desired client certificate, use the `SelectCertificateHandler`. You can instruct the web server which one to use:


**C#**
```csharp
// Select the last client certificate in the list of available
// client certificates.
browser.SelectCertificateHandler = 
    new Handler<SelectCertificateParameters, SelectCertificateResponse>(p =>
    {
        return SelectCertificateResponse.Select(p.Certificates.Count() - 1);
    });
```

**VB**
```vb
' Select the last client certificate in the list of available
' client certificates.
browser.SelectCertificateHandler = 
    New Handler(Of SelectCertificateParameters, SelectCertificateResponse)(Function(p)
        Return SelectCertificateResponse.Select(p.Certificates.Count() - 1)
    End Function)
```



It is also possible to display a dialog to select the required available client certificates.

To cancel a client certificate authentication, use the following approach:


**C#**
```csharp
browser.SelectCertificateHandler = 
    new Handler<SelectCertificateParameters, SelectCertificateResponse>(p =>
    {
        return SelectCertificateResponse.Cancel();
    });
```

**VB**
```vb
browser.SelectCertificateHandler = 
    New Handler(Of SelectCertificateParameters, SelectCertificateResponse)(Function(p)
        Return SelectCertificateResponse.Cancel()
    End Function)
```



### Custom client certificate

DotNetBrowser allows selecting a custom client certificate that is not installed, and as a result, is not available in the given list of the client certificates. The following example demonstrates how to select a custom client certificate:


**C#**
```csharp
string clientCertFile = "<cert-file>.pfx";
string clientCertPassword = "<cert-password>";
// ...
X509Certificate2 certificate = new X509Certificate2(Path.GetFullPath(clientCertFile),
                                                    clientCertPassword,
                                                    X509KeyStorageFlags.Exportable);
Certificate cert = new Certificate(certificate);

browser.SelectCertificateHandler
    = new Handler<SelectCertificateParameters, SelectCertificateResponse>(p =>
    {
        return SelectCertificateResponse.Select(cert);
    });
```

**VB**
```vb
Dim clientCertFile As String = "<cert-file>.pfx"
Dim clientCertPassword As String = "<cert-password>"
' ...
Dim certificate As New X509Certificate2(Path.GetFullPath(clientCertFile), 
                                        clientCertPassword,
                                        X509KeyStorageFlags.Exportable)
Dim cert As New Certificate(certificate)

browser.SelectCertificateHandler = 
    New Handler(Of SelectCertificateParameters, SelectCertificateResponse)(Function(p)
        Return SelectCertificateResponse.Select(cert)
    End Function)
```



In the code sample above, a custom client certificate is loaded from the `<cert-file>` using PKCS12 keystore and `<cert-password>`, and a `Certificate` with this client certificate is created.
