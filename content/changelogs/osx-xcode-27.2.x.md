---
title: Xcode 27.2 changelog
summary: Changelog of stack updates
type: basic_page
---

## Updates

### Stack update `v2026-10-30`

- Initial stack release with [Xcode 27.2](https://developer.apple.com/documentation/xcode-release-notes/xcode-27_2-release-notes) (build `27B52`) on macOS 26.6.2 (25G83)
- Following [Apple's workaround](https://support.apple.com/en-us/149555), we untrust the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/) in the macOS system trust store (`/etc/ssl/cert.pem`), used by the system `curl` (`/usr/bin/curl`), `git` and other built-in tools