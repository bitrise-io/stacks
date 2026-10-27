---
title: Xcode 27.1 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

## Updates

### Stack update `v2026-10-21` (released 2026-10-21)

- macOS update: `26.6.1` (`25G76`) → `27.0.1` (`26A434`)
- Next to [Apple's immediate certificate revocations](https://support.apple.com/en-us/149555), we untrust the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/) in Homebrew's trust store:
  - Homebrew `ca-certificates` upgrade: `2026-09-25` -> `2026-10-20`
  - `curl` itself didn't need an update: it uses the certificates from Homebrew's `ca-certificates`, so it rejects the compromised CAs now
  - The same applies to OpenSSL and other tools that use Homebrew's OpenSSL trust store
- Bitrise guest agent upgrade: `2.10.1` → `2.10.7`
- GitHub CLI upgrade: `2.102.0` → `2.102.1`
- AWS CLI upgrade: `2.38.1` → `2.38.3`
- Google Cloud CLI upgrade: `587.0.0` → `590.0.0`
- pre-commit upgrade: `4.6.2` → `4.7.0`
- uv upgrade: `0.12.21` → `0.13.4`
- `Python` additional preinstalled version: `3.14.8` → `3.13.16`
- Homebrew package upgrades

### Stack update `v2026-10-20`

- Homebrew package upgrades

### Stack update `v2026-10-15` (released 2026-10-15)

- Bitrise CLI upgrade: `3.1.0` → `3.2.1`
- AWS CLI upgrade: `2.37.9` → `2.38.1`
- Firebase CLI upgrade: `15.32.1` → `15.33.0`
- 1Password CLI upgrade: `2.40.0` → `2.41.0`
- OpenVPN upgrade: `2.7.7` → `2.7.8`
- Fastlane upgrade: `2.240.1` → `2.241.0`
- Kotlin upgrade: `2.4.20` → `2.4.21`
- Node.js upgrade: `26.10.0` → `26.11.1`
- `Python` additional preinstalled version: `3.15.0`
- Homebrew package upgrades

### Stack update `v2026-10-06`

- [Xcode 27.1 RC](https://developer.apple.com/documentation/xcode-release-notes/xcode-27_1-release-notes) (build `27A9275`)
- Fixed: `xcodebuild` no longer hangs on a keychain prompt or fails with `-25308` when it resolves private Swift package repos over HTTPS. Homebrew's git now stores credentials through Apple's `git-credential-osxkeychain`, so Xcode's `git` can read them.
- Homebrew package upgrades

### Stack update `v2026-10-02` (released 2026-10-05)

This stack update addresses the iOS 27.1 and watchOS 26.5 simulator problems mentioned below, in which simulator runtimes were getting unmounted during test runs.

- Git upgrade: `2.55.0` → `2.56.0`
- GitHub CLI upgrade: `2.101.0` → `2.102.0`
- AWS CLI upgrade: `2.37.5` → `2.37.7`
- Google Cloud CLI upgrade: `582.0.0` → `587.0.0`
- Firebase CLI upgrade: `15.31.0` → `15.32.1`
- yq upgrade: `4.53.6` → `4.54.1`
- Android Emulator upgrade: `37.1.11` → `37.2.12`
- LicensePlist upgrade: `3.28.2` → `3.28.3`
- uv upgrade: `0.12.7` → `0.12.21`
- Homebrew package upgrades

### Stack update `v2026-09-29` (released 2026-09-29)

- **Note**: We have observed the iOS 27.1 and watchOS 26.5 simulators getting unmounted during test runs, causing test failures. We are working on a fix.

- `applesimutils` removed: its Homebrew tap is no longer maintained and doesn't work with recent Homebrew versions. Use `xcrun simctl` instead.
- Homebrew package upgrades

### Stack update `v2026-09-18`

Initial stack release with [Xcode 27.1 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-27_1-release-notes) (build `27A9269`) on macOS 26.6.1 (25G76)
