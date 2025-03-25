---
title: Xcode 16.3 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-16.3.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2025-03-25`

- [Xcode 16.3 RC](https://developer.apple.com/documentation/xcode-release-notes/xcode-16_3-release-notes) replaces Beta 3
- Homebrew package upgrades

### Stack update `v2025-03-18`

- [Xcode 16.3 Beta 3](https://developer.apple.com/documentation/xcode-release-notes/xcode-16_3-release-notes) replaces Beta 2
- Note: the simulator runtime of `visionOS 2.4 beta 4` is not installed as download currently fails with Xcode Beta 3 (Radar: `FB16927952`)
- The pre-configured git user details are now `Bitrise CI` (`git config user.name`) and `noreply@bitrise.io` (`git config user.email`)
- Homebrew package upgrades

### Stack update `v2025-03-06`

- [Xcode 16.3 Beta 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-16_3-release-notes) replaces Beta 1
- Android SDK Platform 35 (`platforms;35`) is now preinstalled
- Homebrew package upgrades

### Stack update `v2025-02-24`

Initial release of the stack with [Xcode 16.3 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-16_3-release-notes).


