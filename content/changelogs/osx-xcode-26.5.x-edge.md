---
title: Xcode 26.5 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-26.5.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2026-06-03` (released `2026-06-08`)

- Android SDK Platform 37.0 added (android-34 removed)
- Bitrise CLI upgrade: `2.40.0` → `2.40.4`
- OpenJDK upgrade: `25.0.2` → `26.0.1`
- Kotlin upgrade: `2.3.21` → `2.4.0`
- ffmpeg `8.1.1` added
- SwiftLint upgrade: `0.63.2` → `0.63.3`
- LicensePlist upgrade: `3.27.8` → `3.27.9`
- Homebrew package upgrades

### Stack update `v2026-05-18`

- macOS update to 26.5 (25F71)
- Homebrew package upgrades

### Stack update `v2026-05-05`

- Most recent 26.5 simulators for iOS, watchOS, and tvOS added
- Homebrew package upgrades

### Stack update `v2026-05-05`

- This release contains the latest visionOS simulator. Others coming in the next release.  

- [Xcode 26.5 RC](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_5-release-notes) (build `17F42`)
- Homebrew package upgrades

### Stack update `v2026-04-28`

- [Xcode 26.5 Beta 3](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_5-release-notes) (build `17F5032f`)
- Homebrew package upgrades

### Stack update `v2026-04-20` (released 2026-04-21)

- Homebrew package upgrades

### Stack update `v2026-04-14`

- [Xcode 26.5 Beta 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_5-release-notes) (build `17F5022i`)
- Homebrew package upgrades

### Notice `v2026-04-13`

We've released the [Create Simulator Device Pair Step](https://bitrise.io/integrations/steps/xcode-create-device-pair) to give teams fine-grained control over simulator configuration. It solves the inconsistent default pair behavior that started with Xcode 26.4.

### Stack update `v2026-03-31`

Initial stack release with [Xcode 26.5 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_5-release-notes) (build `17F5012f`) on macOS 26.4 (25E246)
