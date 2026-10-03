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

### Stack update `v2026-10-02` (released 2026-10-03)

- Bitrise CLI upgrade: `3.0.0` -> `3.1.0`
- AWS CLI upgrade: `2.37.5` -> `2.37.7`
- Android emulator version: `37.1.11` -> `37.2.12`
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
