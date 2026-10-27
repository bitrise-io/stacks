---
title: Xcode 27.1 changelog
summary: Changelog of stack updates
type: basic_page
---

## Updates

### Stack update `v2026-10-23` (released 2026-10-26)

- Next to [Apple's immediate certificate revocations](https://support.apple.com/en-us/149555), we untrust the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/) in Homebrew's trust store:
  - Homebrew `ca-certificates` upgrade: `2026-08-13` -> `2026-10-20`
  - `curl` itself didn't need an update: it uses the certificates from Homebrew's `ca-certificates`, so it rejects the compromised CAs now
  - The same applies to OpenSSL and other tools that use Homebrew's OpenSSL trust store

### Stack update `v2026-10-16` (released 2026-10-16)

Initial stack release with [Xcode 27.1](https://developer.apple.com/documentation/xcode-release-notes/xcode-27_1-release-notes) (build `27A9275`) on macOS 26.6.2 (25G83)
