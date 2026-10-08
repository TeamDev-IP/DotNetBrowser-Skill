
# Migrating from 4.1.1 to 4.2.0

## Chromium bundle ID changed on macOS

The Chromium bundle ID changed from `org.chromium.Chromium` to
`com.teamdev.Platinum`. Because macOS identifies applications by their bundle
ID, it treats the updated build as a new application on first launch.

As a result, any macOS permission previously granted to your application —
such as camera, microphone, screen recording, notifications, or accessibility
access — may be re-requested. Grant them once, and normal operation resumes.

Applications or enterprise policies that reference `org.chromium.Chromium` by
bundle ID must be updated to use `com.teamdev.Platinum`.