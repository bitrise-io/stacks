---
title: Xcode 27.0 changelog
summary: Changelog of stack updates
type: basic_page
---

## Updates

### Stack update `v2026-10-30`

- The default `curl` has been changed to Homebrew `curl`, which uses the trust store updated for the eMudhra compromise. We recommend this version of `curl`. If your workflow requires the system `curl`, call it by its full path: `/usr/bin/curl`

### Stack update `v2026-10-23` (released 2026-10-26)

- Next to [Apple's immediate certificate revocations](https://support.apple.com/en-us/149555), we untrust the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/) in Homebrew's trust store:
  - Homebrew `ca-certificates` upgrade: `2026-08-13` -> `2026-10-20`
  - `curl` itself didn't need an update: it uses the certificates from Homebrew's `ca-certificates`, so it rejects the compromised CAs now
  - The same applies to OpenSSL and other tools that use Homebrew's OpenSSL trust store

### Stack update `v2026-10-16`

- iOS 27.1 simulator runtime installed
- New iOS 27.1 simulator device: iPhone Duo
- Bitrise CLI upgrade: `2.43.4` -> `3.2.1`

### Stack update `v2026-09-15`

Initial stack release with [Xcode 27.0](https://developer.apple.com/documentation/xcode-release-notes/xcode-27-release-notes) (build `27A266a`) on macOS 26.6.2 (25G83)
