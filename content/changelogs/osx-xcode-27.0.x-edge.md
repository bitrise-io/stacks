---
title: Xcode 27.0 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-27.0.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2026-09-01`

- iOS 18.6 simulator runtime installed on the stack
- New preinstalled CLI tools: `1Password CLI`, `Sentry CLI`
- Flutter upgraded: `3.38.7` → `3.47.0`
- Node.js, Go, and Ruby asdf runtimes upgraded; Node.js `26.7.0` added
- Android SDK: `build-tools` upgraded to `37.0.0`, NDK upgraded to `27.3.13750724`, `platforms;android-37.1` added, `platforms;android-35` removed
- Tuist updated to `4.205.0`
- Homebrew package upgrades

### Stack update `v2026-08-25`

- [Xcode 27.0 Beta 6](https://developer.apple.com/documentation/xcode-release-notes/xcode-27-release-notes) (build `27A5252f`) on macOS 26.6.1 (25G76)
- Homebrew package upgrades
- Tuist updated to `4.202.0`


### Stack update `v2026-08-11`

- [Xcode 27.0 Beta 5](https://developer.apple.com/documentation/xcode-release-notes/xcode-27-release-notes) (build `27A5237l`) on macOS 26.6.1 (25G76)
- OS update 26.6.1 to address [Screen Sharing](https://support.apple.com/en-us/148170) vulnerability
- Homebrew package upgrades

Runtimes: Runtimes: iOS 18.6 is not included in this stack. If you still need it, use the [Xcode Test Without Building step](https://github.com/bitrise-steplib/bitrise-step-xcode-test-without-building) to run the required tests on an older, stable stack.

### Stack update `v2026-07-21`

- [Xcode 27.0 Beta 4](https://developer.apple.com/documentation/xcode-release-notes/xcode-27-release-notes) (build `27A5228h`) on macOS 26.5.1 (25F80)
- Kotlin upgrade: `2.4.0` → `2.4.10`
- Bitrise CLI upgrade: `2.40.8` → `2.42.0`
- Homebrew package upgrades

### Stack update `v2026-07-07`

- [Xcode 27.0 Beta 3](https://developer.apple.com/documentation/xcode-release-notes/xcode-27-release-notes) (build `27A5218g`) on macOS 26.5.1 (25F80)
- Homebrew package upgrades

### Stack update `v2026-06-23`

- [Xcode 27.0 Beta 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-27-release-notes) (build `27A5209h`) on macOS 26.5.1 (25F80)
- Homebrew package upgrades

### Stack update `v2026-06-09`

Initial stack release with [Xcode 27.0 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-27-release-notes) (build `27A5194q`) on macOS 26.5.1 (25F80)
