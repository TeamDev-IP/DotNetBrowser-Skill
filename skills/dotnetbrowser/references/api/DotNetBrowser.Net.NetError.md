# <a id="DotNetBrowser_Net_NetError"></a> Enum NetError

Namespace: [DotNetBrowser.Net](DotNetBrowser.Net.md)  
Assembly: DotNetBrowser.dll  

The network errors.

```csharp
public enum NetError
```

## Fields

`Aborted = -3` 

An operation was aborted ( due to user action).



`AccessDenied = -10` 

Permission to access a resource, other than the network, was denied.



`AddUserCertFailed = -503` 

An error adding to the OS certificate database  = e.g. OS X Keychain,.



`AddressInUse = -147` 

Returned when attempting to bind an address that is already in use.



`AddressInvalid = -108` 

The IP address or port number is invalid  = e.g., cannot connect to the IP
address 0 or the port 0.



`AddressUnreachable = -109` 

The IP address is unreachable.  This usually means that there is no route
to the specified host or network.



`AlpnNegotiationFailed = -122` 

The request to negotiate an alternate protocol failed.



`BadSslClientAuthCert = -117` 

The SSL handshake failed because of a bad or missing client certificate.



`BlobDereferencedWhileBuilding = -904` 

The renderer destructed the blob before it was done transferring, and there were no outstanding references to
keep the blob alive.



`BlobFileWriteFailed = -902` 

A file could not be created or written.



`BlobInvalidConstructionArguments = -900` 

The construction arguments are invalid.



`BlobOutOfMemory = -901` 

There is not enough memory for the blob.



`BlobReferencedBlobBroken = -905` 

A blob referenced during construction is broken, or a browser-side builder tries to build a blob with a blob
reference that is not finished constructing.



`BlobReferencedFileUnavailable = -906` 

A file referenced during construction is not accessible to the renderer trying to create the blob.



`BlobSourceDiedInTransit = -903` 

The renderer was destroyed while data was in transit.



`BlockedByAdministrator = -22` 

The request was blocked by the URL blacklist configured by the domain administrator.



`BlockedByClient = -20` 

The client chose to block the request.



`BlockedByCsp = -30` 

The request was blocked by a Content Security Policy.



`BlockedByFingerprintingProtection = -34` 

The request was blocked by fingerprinting protections.



`BlockedByLocalNetworkAccessChecks = -385` 

The connection is blocked by private network access checks.



`BlockedByOrb = -32` 

The request was blocked by CORB or ORB.



`BlockedByResponse = -27` 

The request failed because the response was delivered along with requirements
which are not met ('X-Frame-Options' and 'Content-Security-Policy' ancestor
checks and 'Cross-Origin-Resource-Policy', for instance).



`BlockedInIncognitoByAdministrator = -35` 

The request was blocked by the Incognito Mode URL block list configured by the domain administrator.



`CacheAuthFailureAfterRead = -410` 

Received a challenge after the transaction has read some data, and the
credentials aren't available. There isn't a way to get them at that point.



`CacheChecksumMismatch = -408` 

The cache found an entry with an invalid checksum. This can be returned from
attempts to read from the cache. It is an internal error, returned by the
SimpleCache backend, but not by any URLRequest methods or members.



`CacheChecksumReadFailure = -407` 

The cache was unable to read a checksum record on an entry. This can be
returned from attempts to read from the cache. It is an internal error,
returned by the SimpleCache backend, but not by any URLRequest methods
or members.



`CacheCreateFailure = -405` 

The disk cache is unable to create this entry.



`CacheDoomFailure = -412` 

The disk cache is unable to doom this entry.



`CacheEntryNotSuitable = -411` 

Internal not-quite error code for the HTTP cache. In-memory hints suggest
that the cache entry would not have been useable with the transaction's
current configuration (e.g. load flags, mode, etc.).



`CacheLockTimeout = -409` 

Internal error code for the HTTP cache. The cache lock timeout has fired.



`CacheMiss = -400` 

The cache does not have the requested entry.



`CacheOpenFailure = -404` 

The disk cache is unable to open this entry.



`CacheOpenOrCreateFailure = -413` 

The disk cache is unable to open or create this entry.



`CacheOperationNotSupported = -403` 

The operation is not supported for this entry.



`CacheRace = -406` 

Multiple transactions are racing to create disk cache entries. This is an
internal error returned from the HttpCache to the HttpCacheTransaction that
tells the transaction to restart the entry-creation logic because the state
of the cache has changed.



`CacheReadFailure = -401` 

Unable to read from the disk cache.



`CacheWriteFailure = -402` 

Unable to write to the disk cache.



`CachedIpAddressSpaceBlockedByLocalNetworkAccessPolicy = -384` 

The IP address space of the cached remote endpoint is blocked by private network access check.



`CertAuthorityInvalid = -202` 

<p>
    The server responded with a certificate that is signed by an authority we don't trust.
    The could mean:
</p>
<p>
    1. An attacker has substituted the real certificate for a cert that
    contains his public key and is signed by his cousin.
</p>
<p>
    2. The server operator has a legitimate certificate from a CA we don't
    know about, but should trust.
</p>
<p>
    3. The server is presenting a self-signed certificate, providing no
    defense against active attackers  = but foiling passive attackers.
</p>



`CertCommonNameInvalid = -200` 

<p>
    The server responded with a certificate whose common name did not match the host name.
    This could mean:
</p>
<p>
    1. An attacker has redirected our traffic to his server and is presenting a certificate
    for which he knows the private key.
</p>
<p>
    2. The server is misconfigured and responding with the wrong cert.
</p>
<p>
    3. The user is on a wireless network and is being redirected to the network's login page.
</p>
<p>
    4. The OS has used a DNS search suffix and the server doesn't have a certificate for
    the abbreviated name in the address bar.
</p>



`CertContainsErrors = -203` 

<p>
    The server responded with a certificate that contains errors.
    This error is not recoverable.
</p>
<p>
    MSDN describes this error as follows:
    "The SSL certificate contains errors."
    NOTE: It's unclear how this differs from ERR_CERT_INVALID. For consistency,
    use that code instead of this one from now on.
</p>



`CertDatabaseChanged = -714` 

The certificate database changed in some way.



`CertDateInvalid = -201` 

<p>
    The server responded with a certificate that, by our clock, appears to
    either not yet be valid or to have expired.  This could mean:
</p>
<p>
    1. An attacker is presenting an old certificate for which he has managed
    to obtain the private key.
</p>
<p>
    2. The server is misconfigured and is not presenting a valid cert.
</p>
<p>
    3. Our clock is wrong.
</p>



`CertEnd = -220` 

The value immediately past the last certificate error code.



`CertInvalid = -207` 

<p>
    The server responded with a certificate that is invalid.
    This error is not recoverable.
</p>
<p>
    MSDN describes this error as follows:
    "The SSL certificate is invalid."
</p>



`CertKnownInterceptionBlocked = -217` 

Indicates that a certificate is blocked due to known interception or manipulation.

This value is typically returned when a certificate validation process detects that
    the certificate has been intercepted or altered by a known intermediary, such as a security appliance or
    malicious actor. Applications can use this status to identify and respond to potential security
    threats.

`CertNameConstraintViolation = -212` 

The certificate claimed DNS names that are in violation of name constraints.



`CertNoRevocationMechanism = -204` 

The certificate has no mechanism for determining if it is revoked.  In
effect, this certificate cannot be revoked.



`CertNonUniqueName = -210` 

The host name specified in the certificate is not unique.



`CertRevoked = -206` 

The server responded with a certificate has been revoked.
We have the capability to ignore this error, but it is probably not the
thing to do.



`CertSelfSignedLocalNetwork = -219` 

The certificate is self-signed and it is being used for either an RFC1918 IP literal URL, or a URL ending in
<code>.local</code>.



`CertTransparencyRequired = -214` 

Certificate Transparency was required for this connection, but the server
did not provide CT information that complied with the policy.



`CertUnableToCheckRevocation = -205` 

<p>
    Revocation information for the security certificate for this site is not
    available.  This could mean:
</p>
<p>
    1. An attacker has compromised the private key in the certificate and is
    blocking our attempt to find out that the cert was revoked.
</p>
<p>
    2. The certificate is unrevoked, but the revocation server is busy or
    unavailable.
</p>



`CertValidityTooLong = -213` 

The certificate's validity period is too long.



`CertVerifierChanged = -716` 

The certificate verifier configuration changed in some way.



`CertWeakKey = -211` 

The server responded with a certificate that contains a weak key  = e.g.
a too-small RSA key.



`CertWeakSignatureAlgorithm = -208` 

The server responded with a certificate that is signed using a weak
signature algorithm.



`ClientAuthCertTypeUnsupported = -151` 

Server request for client certificate did not contain any types we support.



`ConnectionAborted = -103` 

A connection timed out as a result of not receiving an ACK for data sent.
This can include a FIN packet that did not get ACK'd.



`ConnectionClosed = -100` 

A connection was closed (corresponding to a TCP FIN).



`ConnectionFailed = -104` 

A connection attempt failed.



`ConnectionRefused = -102` 

A connection attempt was refused.



`ConnectionReset = -101` 

A connection was reset  = corresponding to a TCP RST.



`ConnectionTimedOut = -118` 

A connection attempt timed out.



`ContentDecodingFailed = -330` 

Content decoding of the response body failed.



`ContentDecodingInitFailed = -371` 

Initializing content decoding failed.



`ContentLengthMismatch = -354` 

The HTTP response body transferred fewer bytes than were advertised by the
Content-Length header when the connection is closed.



`ContextShutDown = -26` 

The request failed because the URLRequestContext is shutting down, or has
been shut down.



`CtConsistencyProofParsingFailed = -171` 

Certificate Transparency: Failed to parse the received consistency proof.



`CtSthIncomplete = -169` 

Certificate Transparency: Received a signed tree head whose JSON parsing was
OK but was missing some of the fields.



`CtSthParsingFailed = -168` 

Certificate Transparency: Received a signed tree head that failed to parse.



`DictionaryLoadFailed = -387` 

The compression dictionary cannot be loaded.



`DisallowedUrlScheme = -301` 

The scheme of the URL is disallowed.



`DnsCacheInvalidationInProgress = -815` 

Returned when DNS cache invalidation is in progress. This is a transient error. Callers may want to retry later.



`DnsCacheMiss = -804` 

The entry was not found in cache, for cache-only lookups.



`DnsFormatError = -816` 

The DNS server responded with a format error response code.



`DnsMalformedResponse = -800` 

DNS resolver received a malformed response.



`DnsNameHttpsOnly = -809` 

DNS identified the request as disallowed for insecure connection (<code>http</code>/<code>ws</code>).
The error should be handled as if an HTTP redirect was received to redirect to <code>https</code> or <code>wss</code>.



`DnsNoMatchingSupportedAlpn = -811` 

The hostname resolution of an HTTPS record was expected to be resolved with ALPN values of supported
protocols, but did not.



`DnsNotImplemented = -818` 

The DNS server responded that the query type is not implemented.



`DnsOtherFailure = -820` 

The DNS server responded with an rcode indicating that the request failed, but there is no specific error code
for the rcode.



`DnsRefused = -819` 

The DNS server responded that the request was refused.



`DnsRequestCancelled = -810` 

All DNS requests associated with this job have been cancelled.



`DnsSearchEmpty = -805` 

Suffix search list rules prevent resolution of the given host name.



`DnsSecureProbeRecordInvalid = -814` 

When checking whether secure DNS can be used, the response returned for the requested probe record either had
no answer or was invalid.



`DnsSecureResolverHostnameResolutionFailed = -808` 

Failed to resolve the hostname of a DNS-over-HTTPS server.



`DnsServerFailure = -817` 

The DNS server responded with a server failure response code.



`DnsServerRequiresTcp = -801` 

DNS server requires TCP



`DnsSortError = -806` 

Failed to sort addresses according to RFC3484.



`DnsTimedOut = -803` 

DNS transaction timed out.



`EarlyDataRejected = -178` 

TLS 1.3 early data was rejected by the server. This will be received before
any data is returned from the socket. The request should be retried with
early data disabled.



`EchFallbackCertificateInvalid = -184` 

ECH was enabled, the server was unable to decrypt the encrypted <code>ClientHello</code>, and additionally did not
present a certificate valid for the public name.



`EchNotNegotiated = -183` 

ECH was enabled, but the server was unable to decrypt the encrypted <code>ClientHello</code>.



`EmptyResponse = -324` 

The server closed the connection without sending any data.



`EncodingDetectionFailed = -340` 

Detecting the encoding of the response failed.



`Failed = -2` 

A generic failure occurred.



`FileExists = -16` 

The file already exists.



`FileNoSpace = -18` 

Not enough room left on the disk.



`FileNotFound = -6` 

The file or directory cannot be found.



`FilePathTooLong = -17` 

The path or file name is too long.



`FileTooBig = -8` 

The file is too large.



`FileVirusInfected = -19` 

The file has a virus.



`HeadersTruncated = -357` 

The HTTP headers were truncated by an EOF.



`HostResolverQueueTooLarge = -119` 

There are too many pending DNS resolves, so a request in the queue was aborted.



`Http11Required = -365` 

HTTP_1_1_REQUIRED error code received on HTTP/2 session.



`Http2CompressionError = -363` 

Decoding or encoding of compressed HTTP/2 headers failed.



`Http2FlowControlError = -361` 

The peer violated HTTP/2 flow control.



`Http2FrameSizeError = -362` 

The peer sent an improperly sized HTTP/2 frame.



`Http2InadequateTransportSecurity = -360` 

Transport security is inadequate for the HTTP/2 version.



`Http2RstStreamNoErrorReceived = -372` 

Received HTTP/2 RST_STREAM frame with NO_ERROR error code. This error should
be handled internally by HTTP/2 code, and should not make it above the
SpdyStream layer.



`Http2StreamClosed = -376` 

Received an HTTP/2 frame on a closed stream.



`HttpResponseCodeFailure = -379` 

The server returned a non-2xx HTTP response code.
Note that this error is only used by certain APIs that interpret the HTTP
response itself. URLRequest for instance just passes most non-2xx
response back as success.



`IcannNameCollision = -166` 

Resolving a hostname to an IP address list included the IPv4 address
"127.0.53.53". This is a special IP address which ICANN has recommended to
indicate there was a name collision, and alert admins to a potential
problem.



`ImportCaCertFailed = -705` 

CA import failed due to some other error.



`ImportCaCertNotCa = -703` 

CA import failed - not a CA cert.



`ImportCertAlreadyExists = -704` 

Import failed - certificate already exists in database.
Note it's a little weird this is an error but reimporting a PKCS12 is ok
= no-op,.  That's how Mozilla does it, though.



`ImportServerCertFailed = -706` 

Server certificate import failed due to some internal error.



`IncompleteChunkedEncoding = -355` 

The HTTP response body is transferred with Chunked-Encoding, but the
terminating zero-length chunk was never sent when the connection is closed.



`IncompleteSpdyHeaders = -347` 

SPDY Headers have been received, but not all of them - status or version
headers are missing, so we're expecting additional frames to complete them.



`InconsistentIpAddressSpace = -383` 

The IP address space of the remote endpoint differed from the previous observed value during the same request.



`InsecureResponse = -501` 

The server's response was insecure  = e.g. there was a cert error,.



`InsufficientResources = -12` 

There were not enough resources to complete the operation.



`InternetDisconnected = -106` 

The Internet connection has been lost.



`InvalidArgument = -4` 

An argument to the function is incorrect.



`InvalidAuthCredentials = -338` 

Credentials could not be established during HTTP Authentication.



`InvalidChunkedEncoding = -321` 

Error in chunked transfer encoding.



`InvalidEchConfigList = -182` 

The <code>ECHConfigList</code> fetched over DNS cannot be parsed.



`InvalidHandle = -5` 

The handle or file descriptor is invalid.



`InvalidHttpResponse = -370` 

The server was expected to return an HTTP/1.x response, but did not. Rather
than treat it as HTTP/0.9, this error is returned.



`InvalidRedirect = -303` 

Attempting to load an URL resulted in a redirect to an invalid URL.



`InvalidResponse = -320` 

The server's response was invalid.



`InvalidSignedExchange = -504` 

An error occurred while handling a signed exchange.



`InvalidUrl = -300` 

The URL is invalid.



`InvalidWebBundle = -505` 

An error occurred while handling a Web Bundle source.



`IoPending = -1` 

An asynchronous IO operation is not yet complete.  This usually does not
indicate a fatal error.  Typically this error will be generated as a
notification to wait for some external notification that the IO operation
finally completed.



`KeyGenerationFailed = -710` 

Key generation failed.



`MalformedIdentity = -329` 

The identity used for authentication is invalid.



`MandatoryProxyConfigurationFailed = -131` 

A mandatory proxy configuration could not be used. Currently this means that
a mandatory PAC script could not be fetched, parsed or executed.



`MethodNotSupported = -322` 

The server did not support the request method.



`MisconfiguredAuthEnvironment = -343` 

The environment was not set up correctly for authentication  = for
example, no KDC could be found or the principal is unknown.



`MissingAuthCredentials = -341` 

= GSSAPI, No Kerberos credentials were available during HTTP Authentication.



`MsgTooBig = -142` 

The message was too large for the transport.
= for example a UDP message which exceeds size threshold,.



`NameNotResolved = -105` 

The host name could not be resolved.



`NameResolutionFailed = -137` 

An error occurred when trying to do a name resolution  = DNS,.



`NetworkAccessDenied = -138` 

Permission to access the network was denied. This is used to distinguish
errors that were most likely caused by a firewall from other access denied errors.
See also ERR_ACCESS_DENIED.



`NetworkAccessRevoked = -33` 

The request was blocked because it originated from a frame that has disabled network access.



`NetworkChanged = -21` 

The network changed.



`NetworkIoSuspended = -331` 

An operation could not be completed because all network IO
is suspended.



`NoBufferSpace = -176` 

No socket buffer space is available.



`NoPrivateKeyForCert = -502` 

The server responded to a &lt;keygen&gt; with a generated client cert that we
don't have the matching private key for.



`NoSupportedProxies = -336` 

There are no supported proxies in the provided list.



`NotImplemented = -11` 

The operation failed because of unimplemented functionality.



`Ok = 1` 

No error.



`OutOfMemory = -13` 

Memory allocation failed.



`PacNotInDhcp = -348` 

No PAC URL configuration could be retrieved from DHCP. This can indicate
either a failure to retrieve the DHCP configuration, or that there was no
PAC URL configured in DHCP.



`PacScriptFailed = -327` 

The evaluation of the PAC script failed.



`PacScriptTerminated = -367` 

The PAC script terminated fatally and must be reloaded.



`Pkcs12ImportBadPassword = -701` 

PKCS #12 import failed due to incorrect password.



`Pkcs12ImportFailed = -702` 

PKCS #12 import failed due to other error.



`Pkcs12ImportInvalidFile = -708` 

PKCS #12 import failed due to invalid/corrupt file.



`Pkcs12ImportInvalidMac = -707` 

PKCS #12 import failed due to invalid MAC.



`Pkcs12ImportUnsupported = -709` 

PKCS #12 import failed due to unsupported features.



`PreconnectMaxSocketLimit = -133` 

We've hit the max socket limit for the socket pool while preconnecting.
We don't bother trying to preconnect more sockets.



`PrivateKeyExportFailed = -712` 

Failure to export private key.



`ProxyAuthRequested = -127` 

The proxy requested authentication  = for tunnel establishment.



`ProxyAuthRequestedWithNoConnection = -364` 

Proxy Auth Requested without a valid Client Socket Handle.



`ProxyAuthUnsupported = -115` 

The proxy requested authentication  = for tunnel establishment, with an unsupported method.



`ProxyCertificateInvalid = -136` 

The certificate presented by the HTTPS Proxy was invalid.



`ProxyConnectionFailed = -130` 

Could not create a connection to the proxy server. An error occurred either
in resolving its name, or in connecting a socket to it. Note that this does
NOT include failures during the actual "CONNECT" method of an HTTP proxy.



`ProxyDelegateCanceledConnectRequest = -187` 

The proxy delegate cancelled the proxy connection request.



`ProxyDelegateCanceledConnectResponse = -188` 

The proxy delegate cancelled the proxy connection response.



`ProxyHttp11Required = -366` 

HTTP_1_1_REQUIRED error code received on HTTP/2 session to proxy.



`ProxyUnableToConnectToDestination = -186` 

An attempt to proxy a request failed because the proxy was not able to successfully connect to the destination.



`QuicCertRootNotKnown = -380` 

The certificate presented on a QUIC connection does not chain to a known root
and the origin connected to is not on a list of domains where unknown roots
are allowed.



`QuicGoawayRequestCanBeRetried = -381` 

A <code>GOAWAY</code> frame has been received indicating that the request has not been processed and is safe to retry.



`QuicHandshakeFailed = -358` 

The QUIC crypto handshake failed. This means that the server was unable
to read any requests sent, so they may be resent.



`QuicProtocolError = -356` 

There is a QUIC protocol error.



`ReadIfReadyNotImplemented = -174` 

Socket ReadIfReady support is not implemented. This error should not be user
visible, because the normal Read() method is used as a fallback.



`RequestRangeNotSatisfiable = -328` 

The response was 416  = Requested range not satisfiable, and the server cannot
satisfy the range requested.



`ResponseBodyTooBigToDrain = -345` 

The HTTP response was too big to drain.



`ResponseHeadersMultipleContentDisposition = -349` 

The HTTP response contained multiple Content-Disposition headers.



`ResponseHeadersMultipleContentLength = -346` 

The HTTP response contained multiple distinct Content-Length headers.



`ResponseHeadersMultipleLocation = -350` 

The HTTP response contained multiple Location headers.



`ResponseHeadersTooBig = -325` 

The headers section of the response is too large.



`SelfSignedCertGenerationFailed = -713` 

Self-signed certificate generation failed.



`SocketIsConnected = -23` 

The socket is already connected.



`SocketNotConnected = -15` 

The socket is not connected.



`SocketReceiveBufferSizeUnchangeable = -162` 

Failed to set the socket's receive buffer size as requested, despite success
return code from setsockopt.



`SocketSendBufferSizeUnchangeable = -163` 

Failed to set the socket's send buffer size as requested, despite success
return code from setsockopt.



`SocketSetReceiveBufferSizeError = -160` 

Failed to set the socket's receive buffer size as requested.



`SocketSetSendBufferSizeError = -161` 

Failed to set the socket's send buffer size as requested.



`SocksConnectionFailed = -120` 

Failed establishing a connection to the SOCKS proxy server for a target host.



`SocksConnectionHostUnreachable = -121` 

The SOCKS proxy server failed establishing connection to the target host
because that host is unreachable.



`SpdyPingFailed = -352` 

SPDY server didn't respond to the PING message.



`SpdyProtocolError = -337` 

There is a SPDY protocol error.



`SpdyServerRefusedStream = -351` 

SPDY server refused the stream. Client should retry. This should never be a
user-visible error.



`SslBadRecordMacAlert = -126` 

An SSL peer sent us a fatal bad_record_mac alert. This has been observed from servers with
buggy DEFLATE support.



`SslClientAuthCertBadFormat = -164` 

Failed to import a client certificate from the platform store into the SSL
library.



`SslClientAuthCertNeeded = -110` 

The server requested a client certificate for SSL client authentication.



`SslClientAuthCertNoPrivateKey = -135` 

The SSL client certificate has no private key.



`SslClientAuthNoCommonAlgorithms = -177` 

There were no common signature algorithms between our client certificate
private key and the server's preferences.



`SslClientAuthPrivateKeyAccessDenied = -134` 

The permission to use the SSL client certificate's private key was denied.



`SslClientAuthSignatureFailed = -141` 

<p>
    We were unable to sign the CertificateVerify data of an SSL client auth
    handshake with the client certificate's private key.
</p>
<p>
    Possible causes for this include the user implicitly or explicitly
    denying access to the private key, the private key may not be valid for
    signing, the key may be relying on a cached handle which is no longer
    valid, or the CSP won't allow arbitrary data to be signed.
</p>



`SslDecompressionFailureAlert = -125` 

An SSL peer sent us a fatal decompression_failure alert. This typically occurs when a peer
selects DEFLATE compression in the mistaken belief that it supports it.



`SslDecryptErrorAlert = -153` 

An SSL peer sent us a fatal decrypt_error alert. This typically occurs when
a peer could not correctly verify a signature (in CertificateVerify or
ServerKeyExchange) or validate a Finished message.



`SslKeyUsageIncompatible = -181` 

The server's certificate has a keyUsage extension incompatible with the
negotiated TLS key exchange method.



`SslNoRenegotiation = -123` 

The peer sent an SSL no_renegotiation alert message.



`SslObsoleteCipher = -172` 

The SSL server required an unsupported cipher suite that has since been
removed. This error will temporarily be signaled on a fallback for one or two
releases immediately following a cipher suite's removal, after which the
fallback will be removed.



`SslPinnedKeyNotInCertChain = -150` 

The certificate didn't match the built-in public key pins for the host name.
The pins are set in net/http/transport_security_state.cc and require that one
of a set of public keys exist on the path from the leaf to the root.



`SslProtocolError = -107` 

An SSL protocol error occurred.



`SslRenegotiationRequested = -114` 

The server requested a renegotiation  = rehandshake,.



`SslServerCertBadFormat = -167` 

The SSL server presented a certificate which could not be decoded. This is
not a certificate error code as no X509Certificate object is available. This
error is fatal.



`SslServerCertChanged = -156` 

The SSL server certificate changed in a renegotiation.



`SslUnrecognizedNameAlert = -159` 

The SSL server sent us a fatal unrecognized_name alert.



`SslVersionOrCipherMismatch = -113` 

The client and server don't support a common SSL protocol version or cipher suite.



`TemporarilyThrottled = -139` 

The request throttler module cancelled this request to avoid DDOS.



`TimedOut = -7` 

An operation timed out.



`Tls13DowngradeDetected = -180` 

TLS 1.3 was enabled, but a lower version was negotiated and the server
returned a value indicating it supported TLS 1.3. This is part of a security
check in TLS 1.3, but it may also indicate the user is behind a buggy
TLS-terminating proxy which implemented TLS 1.2 incorrectly. (See
https://crbug.com/boringssl/226.)



`TooManyAcceptChRestarts = -382` 

The <code>ACCEPT_CH</code> restart has been triggered too many times.



`TooManyRedirects = -310` 

Attempting to load an URL resulted in too many redirects.



`TooManyRetries = -375` 

An HTTP transaction was retried too many times due for authentication or
invalid certificates. This may be due to a bug in the net stack that would
otherwise infinite loop, or if the server or proxy continually requests fresh
credentials or presents a fresh invalid certificate.



`TrustTokenOperationFailed = -506` 

A Trust Tokens protocol operation-executing request failed for one of a
number of reasons (precondition failure, internal error, bad response).



`TrustTokenOperationSuccessWithoutSendingRequest = -507` 

When handling a Trust Tokens protocol operation-executing request, the system
was able to execute the request's Trust Tokens operation without sending the
request to its destination: for instance, the results could have been present
in a local cache (for redemption) or the operation could have been diverted
to a local provider (for "platform-provided" issuance).



`TunnelConnectionFailed = -111` 

A tunnel connection through the proxy could not be established.



`UnableToReuseConnectionForProxyAuth = -170` 

The attempt to reuse a connection to send proxy auth credentials failed
before the AuthController was used to generate credentials. The caller should
reuse the controller with a new connection. This error is only used
internally by the network stack.



`UndocumentedSecurityLibraryStatus = -344` 

An undocumented SSPI or GSSAPI status code was returned.



`Unexpected = -9` 

An unexpected error.  This may be caused by a programming mistake or an invalid assumption.



`UnexpectedContentDictionaryHeader = -388` 

The header of a dictionary-compressed stream does not match the expected value.



`UnexpectedProxyAuth = -323` 

The response was 407  = Proxy Authentication Required,, yet we did not send
the request to a proxy.



`UnexpectedSecurityLibraryStatus = -342` 

An unexpected, but documented, SSPI or GSSAPI status code was returned.



`Unknown = 2` 

The error is unknown.



`UnknownUrlScheme = -302` 

The scheme of the URL is unknown.



`UnsafePort = -312` 

Attempting to load an URL with an unsafe port number.  These are port
numbers that correspond to services, which are not robust to spurious input
that may be constructed as a result of an allowed web construct  = e.g., HTTP
looks a lot like SMTP, so form submission to port 25 is denied,.



`UnsafeRedirect = -311` 

Attempting to load an URL resulted in an unsafe redirect  = e.g., a redirect
to file:// is considered unsafe.



`UnsupportedAuthScheme = -339` 

An HTTP Authentication scheme was tried which is not supported on this
machine.



`UploadFileChanged = -14` 

The file upload failed because the file's modification time was different from the expectation.



`UploadStreamRewindNotSupported = -25` 

The upload failed because the upload stream needed to be re-read, due to a
retry or a redirect, but the upload stream doesn't support that operation.



`WinsockUnexpectedWrittenBytes = -124` 

Winsock sometimes reports more data written than passed.  This is probably due to a broken LSP.



`WrongVersionOnEarlyData = -179` 

TLS 1.3 early data was offered, but the server responded with TLS 1.2 or
earlier. This is an internal error code to account for a
backwards-compatibility issue with early data and TLS 1.2. It will be
received before any data is returned from the socket. The request should be
retried with early data disabled.
See https://tools.ietf.org/html/rfc8446#appendix-D.3 for details.



`WsProtocolError = -145` 

Websocket protocol error. Indicates that we are terminating the connection
due to a malformed frame or other protocol violation.



`WsThrottleQueueTooLarge = -154` 

There are too many pending WebSocketJob instances, so the new job was not
pushed to the queue.



`WsUpgrade = -173` 

When a WebSocket handshake is done successfully and the connection has been
upgraded, the URLRequest is cancelled with this error code.



`ZstdWindowSizeTooBig = -386` 

Content decoding failed due to the zstd window size being too big (over 8 MB).



