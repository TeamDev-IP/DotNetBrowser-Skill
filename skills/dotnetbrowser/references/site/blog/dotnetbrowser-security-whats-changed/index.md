# DotNetBrowser Security: What’s Changed

Over the past two months, our engineering and security teams have been
speaking with enterprise customers across healthcare, finance, telecom,
industrial automation, and other sectors about software security, supply-chain
transparency, and the EU Cyber Resilience Act (CRA).

These conversations helped us better understand what customers need from their
software vendors as CRA-related processes and expectations become part of their
own product security work.

This post summarizes several practical changes and resources we have introduced
around DotNetBrowser security, vulnerability handling, software transparency,
and Chromium updates.

## 1. CRA information page

We have published a dedicated page describing our approach to product
security and the CRA: [https://teamdev.com/dotnetbrowser/cra][cra]

The page brings together information about DotNetBrowser security
practices, vulnerability handling, software supply-chain transparency, and other
topics that may be relevant to customers working with CRA requirements.

It is intended as a practical reference for customers evaluating
DotNetBrowser as part of their own security and regulatory processes.

## 2. Software Bill of Materials (SBOM)

Software supply-chain transparency is becoming increasingly important for
enterprise software.

Because DotNetBrowser embeds Chromium and also includes several other software
components, customers may need machine-readable information about
the software included in a particular DotNetBrowser release.

We now generate and publish a CycloneDX Software Bill of Materials (SBOM)
for DotNetBrowser releases.

The SBOM provides machine-readable information about DotNetBrowser
components and dependencies, including the Chromium version used by
a particular release.

This makes it easier to work with Software Composition Analysis and
vulnerability-management tools such as Dependency-Track, Black Duck, Snyk, and
similar systems.

SBOM files are available in the [DotNetBrowser release
notes][release-notes].

## 3. Coordinated Vulnerability Disclosure policy

We have also formalized our Coordinated Vulnerability Disclosure (CVD) process:

[https://teamdev.com/cvd-policy/][cvd-policy]

The policy explains how security researchers, customers, and partners can
report potential vulnerabilities to TeamDev and how we handle those reports.

It provides a clear contact point for security-related reports and
describes our vulnerability intake, assessment, communication, and remediation
process.

## 4. Chromium updates and security fixes

A significant part of DotNetBrowser's security surface comes from Chromium.

Chromium receives frequent security updates, which means staying current with
upstream releases is an important part of maintaining DotNetBrowser.

Our release process is designed to integrate new Chromium versions and their
security fixes quickly while preserving DotNetBrowser API compatibility wherever
possible.

This helps customers update DotNetBrowser without treating every Chromium
security release as a large application migration.

We also monitor the other third-party components included with
DotNetBrowser and update them when necessary.

## What this means for DotNetBrowser customers

For teams responsible for application security, software architecture, or vendor
assessment, these changes provide more information and more structured security
data around DotNetBrowser.

You can:

- review our CRA information page: [https://teamdev.com/dotnetbrowser/cra][cra]
- review our Coordinated Vulnerability Disclosure policy:
  [https://teamdev.com/cvd-policy/][cvd-policy]
- use DotNetBrowser SBOMs in your software composition and
  vulnerability-management processes
- follow [DotNetBrowser release notes][release-notes] for Chromium updates and
  security-related changes

We will continue improving the security information and tooling we provide
around DotNetBrowser as customer requirements and the broader software
security landscape evolve.

[cra]: https://teamdev.com/dotnetbrowser/cra
[cvd-policy]: https://teamdev.com/cvd-policy
[release-notes]: https://teamdev.com/dotnetbrowser/releases/
