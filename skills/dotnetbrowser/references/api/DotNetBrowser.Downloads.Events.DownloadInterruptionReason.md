# <a id="DotNetBrowser_Downloads_Events_DownloadInterruptionReason"></a> Enum DownloadInterruptionReason

Namespace: [DotNetBrowser.Downloads.Events](DotNetBrowser.Downloads.Events.md)  
Assembly: DotNetBrowser.dll  

Possible download interruption reason.

```csharp
public enum DownloadInterruptionReason
```

## Fields

`Crash = 50` 

The browser crashed.
Internal use only:  resume pending downloads if possible.



`FileAccessDenied = 3` 

The file cannot be accessed due to security restrictions.
"Access Denied".



`FileBlocked = 11` 

The file was blocked due to local policy.
"Blocked"



`FileFailed = 2` 

Generic file operation failure.
"File Error".



`FileHashMismatch = 14` 

The partial file didn't match the expected hash.



`FileNameTooLong = 5` 

The directory or file name is too long.
"Path Too Long".



`FileNoSpace = 4` 

There is not enough room on the drive.
"Disk Full".



`FileSameAsSource = 15` 

The source and the target of the download were the same



`FileSecurityCheckFailed = 12` 

An attempt to check the safety of the download failed due to unexpected
reasons. See http:///crbug.com/153212.



`FileTooLarge = 6` 

The file is too large for the file system to handle.
"File Too Large".



`FileTooShort = 13` 

An attempt was made to seek past the end of a file in opening
a file (as part of resuming a previously interrupted download).



`FileTransientError = 10` 

The file was in use.
Too many files are opened at once.
We have run out of memory.
"Temporary Problem".



`FileVirusInfected = 7` 

The file contains a virus.
"Virus".



`NetworkDisconnected = 22` 

The network connection has been lost.
"Connection Lost".



`NetworkFailed = 20` 

Generic network failure.
"Network Error".



`NetworkInvalidRequest = 24` 

The network request was invalid. This may be due to the original URL or a
redirected URL:
- Having an unsupported scheme.
- Being an invalid URL.
- Being disallowed by policy.



`NetworkServerDown = 23` 

The server has gone down.
"Server Down".



`NetworkTimeout = 21` 

The network operation timed out.
"Operation Timed Out".



`ServerBadContent = 33` 

The server does not have the requested data.
"Unable to get file".



`ServerCertProblem = 35` 

Server certificate problem.



`ServerContentLengthMismatch = 38` 

The server sent fewer bytes than the content-length header. It may indicate
that the connection was closed prematurely, or the Content-Length header was
invalid. The download is only interrupted if strong validators are present.
Otherwise, it is treated as finished.



`ServerFailed = 30` 

The server indicates that the operation has failed (generic).
"Server Error".



`ServerForbidden = 36` 

Server access forbidden.



`ServerNoRange = 31` 

The server does not support range requests.
Internal use only:  must restart from the beginning.



`ServerUnauthorized = 34` 

Server didn't authorize access to resource.



`ServerUnreachable = 37` 

Unexpected server response. This might indicate that the responding server
may not be the intended server.



`Unknown = 1` 

There is no interruption reason.



`UserCanceled = 40` 

The user canceled the download.
"Canceled".



`UserShutdown = 41` 

The user shut down the browser.
Internal use only:  resume pending downloads if possible.



