---
title: Xcode 26.4 with changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-26.4.x.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2026-04-01`

- Added iOS 18.6 and watchOS 11.5 simulator runtimes
- Homebrew `5.1.1` -> `5.1.3`

### Stack update `v2026-03-25`

Initial stack release with [Xcode 26.4](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_4-release-notes) (build `17E192`) on macOS 26.2

Known issue: The iOS simulator runtimes on this stack differ from [our usual policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html). These limitations will be addressed in the next release:

- iOS 17.5 is not included (end of life)
- iOS 18.6 is not available due to compatibility constraints

Major differences compared to the previous stable stack (Xcode 26.3):

- Android emulator version: `36.1.9` -> `36.4.10`
- Android platform-tools version: `36.0.0` -> `37.0.0`
- Kotlin version: `2.2.10` -> `2.3.20`
