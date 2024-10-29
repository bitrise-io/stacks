---
title: Xcode 16.1 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-16.1.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2024-10-28` (released 2024-10-29)

**Known issue**: Remote access screen sharing is not working (SSH access does work). We are working on a fix.

- This stack is now based on macOS Sequoia (15.0)
- Homebrew package upgrades

### Stack update `v2024-10-24

- Homebrew package upgrades

### Stack update `v2024-10-22`

- [Xcode 16.1 RC](https://developer.apple.com/documentation/xcode-release-notes/xcode-16-release-notes) replaces Beta 3.
- Homebrew package upgrades

### Stack update `v2024-09-18`

- [Xcode 16.1 Beta 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-16_1-release-notes) replaces Beta 1.
- Homebrew package upgrades
- Known issue: the AWS CLI (`aws`) fails to run with the error message `/opt/homebrew/Cellar/awscli/2.17.53/libexec/bin/python: No such file or directory`

### Stack update `v2024-09-10`

- Homebrew package upgrades

### Stack update `v2024-08-26` (released on 2024-08-28)

- Homebrew package upgrades
- JDK 8 is not preinstalled anymore
- The old preinstalled Flutter version (3.7.12) has been removed. Flutter 3.22.0 remains preinstalled and is still the default.
- Android SDK cleanups:
  - Only the latest build-tools package (35) is preinstalled. Android Gradle Plugin automatically downloads any missing build-tools packages during configuration if the project requires a different version.
  - Removed NDK 24.0.8215888 as it's no longer the LTS release. The current LTS version (26.3.11579264) is still preinstalled.

### Stack update `v2024-08-21`

- Homebrew package upgrades

### Stack update `v2024-08-13`

- Initial release of the stack with [Xcode 16.1 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-16_1-release-notes).


