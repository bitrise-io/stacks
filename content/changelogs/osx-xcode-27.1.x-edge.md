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

### Stack update `v2026-10-02` (released 2026-10-02)

- Bitrise CLI upgrade: `3.0.0` → `3.1.0`
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
