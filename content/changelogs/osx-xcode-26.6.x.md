---
title: Xcode 26.6 changelog
summary: Changelog of stack updates
type: basic_page
---

## Updates

### Stack update `v2026-10-23` (released 2026-10-26)

- Next to [Apple's immediate certificate revocations](https://support.apple.com/en-us/149555), we untrust the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/) in Homebrew's trust store:
  - Homebrew `ca-certificates` upgrade: `2026-05-14` -> `2026-10-20`
  - This covers OpenSSL and other tools that use Homebrew's OpenSSL trust store
- The default `curl` has been changed to Homebrew `curl`, which uses the trust store updated for the eMudhra compromise. We recommend this version of `curl`. If your workflow requires the system `curl`, call it by its full path: `/usr/bin/curl`

### Stack update `v2026-09-25` (released 2026-09-30)

- New preinstalled CLI tools: `1Password CLI`, `Sentry CLI`

### Stack update `v2026-08-13` released on `2026-08-17`

- Fix: Register the simulator app with launch services.

### Stack update `v2026-08-11`

- OS update 26.6.1 to address [Screen Sharing](https://support.apple.com/en-us/148170) vulnerability
- Bitrise CLI upgrade: `2.40.7` → `2.42.2`
- Bitrise guest agent upgrade: `2.2.0` → `2.10.1`
- Homebrew package upgrades

### Stack update `v2026-06-26`

Initial stack release with [Xcode 26.6](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_6-release-notes) (build `17F113`) on macOS 26.2 (25C56)
