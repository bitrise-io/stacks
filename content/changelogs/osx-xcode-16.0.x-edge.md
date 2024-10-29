---
title: Xcode 16.0 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-16.0.x-edge.md" %}}) for a snapshot of what is currently installed.

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

- Homebrew package upgrades

### Stack update `v2024-10-08`

- Homebrew package upgrades
- Tool version updates:
NodeJS
- "20.13.1"   --> 20.17.0
- "22.1.0"  --> 22.9.0
Python:
- "3.12.4" --> 3.12.6
GO:
- "1.22.3" --> 1.22.7
Ruby:
- "3.1.5" --> 3.1.6
- "3.2.4" --> 3.2.5
- "3.3.4" -->  3.3.5

### Stack update `v2024-09-18`

- [Xcode 16.0](https://developer.apple.com/documentation/xcode-release-notes/xcode-16-release-notes) replaces RC 1.
- Homebrew package upgrades
- Known issue: the AWS CLI (`aws`) fails to run with the error message `/opt/homebrew/Cellar/awscli/2.17.53/libexec/bin/python: No such file or directory`

### Stack update `v2024-09-10`

- [Xcode 16.0 RC 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-16-release-notes) replaces Beta 6.
- Homebrew package upgrades

### Stack update `v2024-08-26` (released on 2024-08-28)

- Homebrew package upgrades
- JDK 8 is not preinstalled anymore
- The old preinstalled Flutter version (3.7.12) has been removed. Flutter 3.22.0 remains preinstalled and is still the default.
- Android SDK cleanups:
  - Only the latest build-tools package (35) is preinstalled. Android Gradle Plugin automatically downloads any missing build-tools packages during configuration if the project requires a different version.
  - Removed NDK 24.0.8215888 as it's no longer the LTS release. The current LTS version (26.3.11579264) is still preinstalled.

### Stack update `v2024-08-21`

- [Xcode 16.0 Beta 6](https://developer.apple.com/documentation/xcode-release-notes/xcode-16-release-notes) replaces Beta 5.
- Homebrew package upgrades

### Stack update `v2024-08-13`

- Homebrew package upgrades

### Stack update `v2024-08-07`

- [Xcode 16.0 Beta 5](https://developer.apple.com/documentation/xcode-release-notes/xcode-16-release-notes) replaces Beta 4.
- Homebrew package upgrades

### Stack update `v2024-07-24`

- [Xcode 16.0 Beta 4](https://developer.apple.com/documentation/xcode-release-notes/xcode-16-release-notes) replaces Beta 3.
- Gradle, Maven and Ant are no longer installed system-wide. We recommend pinning an exact version of the build tool and using the Gradle Wrapper and Maven Wrapper features.
- Tuist has been updated to `4.20.0`
- Homebrew package upgrades
- Ruby upgrade: `3.3.1` -> `3.3.4`

### Stack update `v2024-07-09`

- [Xcode 16.0 Beta 3](https://developer.apple.com/documentation/xcode-release-notes/xcode-16-release-notes) replaces Beta 2.
- To better align with modern Android Gradle Plugin versions, JDK 17 is now the default Java version. JDK 11 remains installed.
- The preinstalled Flutter version has been upgraded to `3.22.0`
- The current LTS Android NDK (`r26`) is now installed. The old preinstalled NDK (`r24`) will be removed in the next update. You can use the [Install missing Android tools step](https://github.com/bitrise-steplib/steps-install-missing-android-tools) to install arbitrary NDK versions.
- [pipx](https://github.com/pypa/pipx), a tool to install Python executables is now installed and configured on stacks.
- Homebrew package upgrades
- Ionic CLI upgrade: 6.x → 7.x
- Cordova CLI upgrade: 11.x → 12.x
- Appcenter CLI upgrade: 2.x → 3.x
- OpenUPM CLI upgrade: 1.x → 3.x

### Stack update `v2024-06-26`

- [Xcode 16.0 Beta 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-16-release-notes) replaces Beta 1.
- Homebrew package upgrades
- Default Ruby version change: `3.2` -> `3.3` (`3.2` remains installed)
- Node.js 21 has been removed as it reached its end of life

### Stack update `v2024-06-10`

- Initial release of the stack with [Xcode 16.0 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-16-release-notes).


