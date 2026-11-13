---
title: Xcode 27.2 changelog
summary: Changelog of stack updates
type: basic_page
---

## Updates

### Stack update `v2026-11-12`

- Git upgrade: `2.55.0` -> `2.56.1`
- Homebrew `libunistring` upgrade: `1.4.2` -> `1.5`
- Homebrew `pcre2` upgrade: `10.48` -> `10.49`

### Stack update `v2026-10-30`

- Initial stack release with [Xcode 27.2](https://developer.apple.com/documentation/xcode-release-notes/xcode-27_2-release-notes) (build `27B52`) on macOS 26.6.2 (25G83)
- Following [Apple's workaround](https://support.apple.com/en-us/149555), we untrust the [compromised eMudhra intermediate CAs](https://bitrise.io/blog/post/emudhra-certificate-compromise-bitrise) in the macOS system trust store (`/etc/ssl/cert.pem`), used by the system `curl` (`/usr/bin/curl`), `git` and other built-in tools