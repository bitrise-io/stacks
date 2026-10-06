---
title: Xcode 27.2 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-27.2.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2026-10-06` (released 2026-10-06)

- AWS CLI upgrade: `2.37.7` → `2.37.9`
- 1Password CLI upgrade: `2.39.0` → `2.40.0`
- CMake upgrade: `4.4.3` → `4.4.4`
- iOS 27.1 simulator runtime upgrade: build `24A94401` → `24A94232`
- Homebrew package upgrades

### Stack update `v2026-10-02` (released 2026-10-05)

- Android SDK: Emulator upgraded to `37.2.12`
- Bitrise CLI upgrade: `3.0.0` → `3.1.0`
- Git upgrade: `2.55.0` → `2.56.0`
- GitHub CLI upgrade: `2.101.0` → `2.102.0`
- AWS CLI upgrade: `2.37.5` → `2.37.7`
- Google Cloud CLI upgrade: `582.0.0` → `587.0.0`
- Firebase CLI upgrade: `15.31.0` → `15.32.1`
- yq upgrade: `4.53.6` → `4.54.1`
- LicensePlist upgrade: `3.28.2` → `3.28.3`
- Homebrew package upgrades

### Stack update `v2026-09-29` (released 2026-09-29)

- [Xcode 27.2 Beta 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-27_2-release-notes) (build `27B5028f`) on macOS 26.6.1 (25G76)
- `applesimutils` removed: its Homebrew tap is no longer maintained and doesn't work with recent Homebrew versions. Use `xcrun simctl` instead.
- Homebrew package upgrades

### Stack update `v2026-09-18`

- AWS CLI upgraded: `2.36.47` → `2.36.48`
- Homebrew package upgrades

### Stack update `v2026-09-17`

Initial stack release with [Xcode 27.2 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-27_2-release-notes) (build `27B5019j`) on macOS 26.6.1 (25G76)
