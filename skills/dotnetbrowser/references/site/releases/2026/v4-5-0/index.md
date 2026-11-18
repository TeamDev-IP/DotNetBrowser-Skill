# DotNetBrowser 4.5.0

Version 4.5.0 · Posted on 2026-11-18

## Sandbox on macOS

The Chromium sandbox is now enabled by default on macOS, as it already is on
Windows and Linux. It isolates Chromium subprocesses to help protect the
system from untrusted web content.

To restore the previous behavior on macOS, set `SandboxDisabled` to `true` in
the engine options. Disabling the sandbox reduces security. See the
[Chromium guide][guides-chromium-sandbox] for details.

## Audio capture

You can now capture the audio played by a browser as raw PCM data. You can
configure the channel layout, sample rate, and buffer size, and choose whether
to mute the source during capture. This can be used to include audio in a video
processing pipeline alongside captured browser frames.

Start a capture session and handle audio data before playback begins:

```csharp
var session = browser.Audio.StartCapture();
session.DataCaptured += (sender, e) =>
{
    float[] samples = e.GetChannelData(0);
    // Process the samples from the first channel.
};
```

Call `session.Stop()` when you no longer need to capture audio. See the
[Media guide][guides-audio-capture] for more details.

## Chromium Task Manager

You can now open the Chromium Task Manager to monitor the processes used by an
engine and their resource usage, including memory, CPU, GPU, and network usage.
The window covers all browsers in the engine and is read-only.

To open the Task Manager window:

```csharp
engine.TaskManager.Show();
```

See the [Chromium guide][guides-task-manager] for more details.

## Chromium 158.0.8127.37

We upgraded Chromium to a newer version. The upgrade
includes security fixes for the following critical vulnerabilities:

* [CVE-2026-126885: Use after free in ServiceWorker][cve-2026-126885]
* [CVE-2026-126895: Use after free in CSS][cve-2026-126895]
* [CVE-2026-131031: Out of bounds write in GPU][cve-2026-131031]
* [CVE-2026-131060: Buffer overflow in Media][cve-2026-131060]
* [CVE-2026-130975: Use after free in WebAudio][cve-2026-130975]

See the Chromium release announcements for more details:

* [November 11][chromium-nov-11-2026]
* [November 17][chromium-nov-17-2026]

[guides-chromium-sandbox]: https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#sandbox
[guides-audio-capture]: https://teamdev.com/dotnetbrowser/docs/guides/gs/media/#capturing-audio
[guides-task-manager]: https://teamdev.com/dotnetbrowser/docs/guides/gs/chromium/#task-manager
[cve-2026-126885]: https://nvd.nist.gov/vuln/detail/CVE-2026-126885
[cve-2026-126895]: https://nvd.nist.gov/vuln/detail/CVE-2026-126895
[cve-2026-131031]: https://nvd.nist.gov/vuln/detail/CVE-2026-131031
[cve-2026-131060]: https://nvd.nist.gov/vuln/detail/CVE-2026-131060
[cve-2026-130975]: https://nvd.nist.gov/vuln/detail/CVE-2026-130975
[chromium-nov-11-2026]: https://chromereleases.googleblog.com/2026/11/stable-channel-update-for-desktop_01744469280.html
[chromium-nov-17-2026]: https://chromereleases.googleblog.com/2026/11/stable-channel-update-for-desktop_01699533288.html
