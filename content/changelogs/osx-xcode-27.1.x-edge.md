---
title: Xcode 27.1 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-27.1.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2026-10-20` (released 2026-10-20)

- iOS 27.2, tvOS 27.2, watchOS 27.2, and visionOS 27.2 simulator runtimes upgraded to RC builds (`24B114`, `24K118`, `24S116`, `24N118`)
- Firebase CLI upgrade: `15.33.0` → `15.34.0`
- Fastlane upgrade: `2.241.0` → `2.241.1`
- Node.js upgrade: `26.11.1` → `26.12.0`
- danger-swift upgrade: `3.23.0` → `3.23.1`
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
