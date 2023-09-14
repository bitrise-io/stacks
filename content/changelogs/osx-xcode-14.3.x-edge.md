---
title: Xcode 14.3 with edge updates changelog
summary: Changelog of stack updates
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-14.3.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2023-09-05`

- Added simulator versions: iOS 15.5, iOS 16.4, watchOS 9.4 and visionOS 1.0
- Go 1.21 pre-installed and set as default.

### Stack update `v2023-08-30`

- The default Node.js version has changed to 18 (from 20) as [this is the current LTS version](https://endoflife.date/nodejs). Node 20 remains installed as the most up-to-date version, but Node 18 is going to be the default version when Xcode 15 becomes stable.
- Fix brew cask related issues.

### Stack update `v2023-08-17`

- macOS has been upgraded from 13.4 to 13.5
- Ruby 3.1.3 has been temporarily removed because of build failures. Ruby 3.1.4 is still installed, we recommend using that version or the version alias `3.1`.
- Android SDK packages `platform-33` and `platform-34` are now preinstalled

### Stack update `v2023-08-08`

- Deprecated Ruby 2.x versions have been removed according to the [deprecation timeline](https://discuss.bitrise.io/t/ruby-2-7-x-deprecation/22544)

### Stack update `v2023-08-02`

- Brew cache update & security fixes.
- Ruby version 3.1.0 has been removed as it's been broken for a while. Version 3.1.0 cannot be reliably installed on macOS because of [this bug](https://bugs.ruby-lang.org/issues/18912); the first fixed version of the 3.1 series is 3.1.3. This version is available preinstalled.

### Stack update `v2023-07-26`

- Preinstalled Ruby gems such as `cocoapods` and `fastlane` are now installed for all available Ruby versions.

### Stack update `v2023-07-18`

- Tool version aliases: tools managed via ASDF got special alias versions for every `major` and `major.minor` version. These aliases always point to the latest installed patch version and can be selected like the regular versions. Examples:
  - `asdf global ruby 3.2`
  - `asdf global nodejs 19`
  - `asdf global golang 1.20`
- Default tool versions are now set to `major.minor` aliases and the exact patch version might change in the future:
  - Ruby: `3.2`
  - Golang: `1.20`
  - Node.js: `20.4`

### Stack update `v2023-07-06`

- Tuist has been updated to [version 3.20](https://github.com/tuist/tuist/releases/tag/3.20.0)

### Stack update `v2023-06-22`

- Ruby versions are now managed via [asdf](https://asdf-vm.com/). During the transition period, both `rbenv` and `asdf` are installed and can be used, but we recommend migrating to `asdf`, which also manages Node.js and Go versions on the stacks.
- Default Ruby version has changed from 2.7.6 to 3.2.2 according to the [deprecation plan](https://discuss.bitrise.io/t/ruby-2-7-x-deprecation/22544).
- Each installed iOS simulator runtime now has a device named `Bitrise iOS default`. This name is constant across all runtime versions, but the real device type changes based on the iOS version. You can use this device name in test steps and destination specifiers and be sure that it’s going to be available across all Xcode and runtime versions.
- The `cmake;3.10.2.4988404` Android SDK package is now preinstalled
- [OpenUPM CLI](https://openupm.com/) is now preinstalled
- [swift-format](https://github.com/apple/swift-format) is now preinstalled
