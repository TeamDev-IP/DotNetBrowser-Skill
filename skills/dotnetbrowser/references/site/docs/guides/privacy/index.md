
# Privacy practices

**Lead**
This document gives an overview of how DotNetBrowser works with personal data, whether it is collected, stored, or sent to third parties.


DotNetBrowser is a .NET library that integrates with Chromium and consists of two parts: the DotNetBrowser library itself and Chromium.

## DotNetBrowser

DotNetBrowser doesn't collect, store, or send any personal data to the external web servers or third parties. It allows enabling [logging](https://teamdev.com/dotnetbrowser/docs/guides/troubleshoot/logging/) and store the log messages in a file on a local file system. The log messages include a lot of information required for the debugging purposes. All the sensitive information like login, passwords, keyboard and mouse events, the dragged text, the product license key, etc. is excluded from the log messages and replaced with asterisks (***).

## Chromium

Google Chrome is based on Chromium. Everything described in [Google Chrome Privacy Policy](https://www.google.com/intl/en/chrome/privacy/) can be applicable to Chromium. We recommend that you read this document to find out how to control the information that's collected, stored, and shared when you use the Google Chrome browser on your computer. What personal information is provided to Google or stored in your Google Account.

DotNetBrowser uses its own Chromium build. In this build, some features that work with the personal data are disabled:

- The `chrome://settings/` page is not accessible. So, you cannot choose to store the data like passwords, payment cards, and billing information in your [Google Account](https://policies.google.com/privacy/key-terms?hl=en#toc-terms-account) by turning on sync.
- No built-in [Google API Keys](https://teamdev.com/dotnetbrowser/docs/guides/gs/engine/#google-apis), so the geolocation feature that tracks your location and sends requests to the Google web servers is disabled by default.
- The usage statistics and crash reports are not sent to Google.
- Chromium automatic updates are disabled.
