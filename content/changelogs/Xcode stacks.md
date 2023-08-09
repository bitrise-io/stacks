---
title: Xcode stacks changelog
summary: Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html). This page is updated every time a new update is released to one of the [macOS-based Xcode stacks](/platform/macos).
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html). This page is updated every time a new update is released to one of the [macOS-based Xcode stacks](/platform/macos).

When a specific Xcode version is not mentioned, all actively updated Xcode stacks are affected.

{{< hint info >}}
Learn more [how to get notified of updates](../tips/Get%20notified.md).
{{< /hint >}}

## Updates

### Stack update `v2023-08-07`, `v2023-08-08`

- {{< chip text="edge" >}} {{< chip text="Xcode 15" >}} Xcode 15 Beta 6 is available, replacing Beta 5
- {{< chip text="stable" >}} {{< chip text="edge" >}} Deprecated Ruby 2.x versions have been removed according to the [deprecation timeline](https://discuss.bitrise.io/t/ruby-2-7-x-deprecation/22544)

### Stack update `v2023-08-02`
This update is for {{< chip text="edge" >}} stacks.

- Brew cache update & security fixes.
- Ruby version 3.1.0 has been removed as it's been broken for a while. Version 3.1.0 cannot be reliably installed on macOS because of [this bug](https://bugs.ruby-lang.org/issues/18912); the first fixed version of the 3.1 series is 3.1.3. This version is available preinstalled.

### Stack update `v2023-07-31`

This update is for {{< chip text="stable" >}} stacks.

- Brew cache update & security fixes.

### Stack update `v2023-07-26`

This update is for {{< chip text="edge" >}} stacks {{< chip text="Xcode 14.3" >}} and {{< chip text="Xcode 15" >}} only.

- [Xcode 15 Beta 5](https://developer.apple.com/documentation/xcode-release-notes/xcode-15-release-notes) is available, replacing Beta 4.
- Preinstalled Ruby gems such as `cocoapods` and `fastlane` are now installed for all available Ruby versions.

### Stack update `v2023-07-18`

- {{< chip text="edge" >}} {{< chip text="stable" >}}Tool version aliases: tools managed via ASDF got special alias versions for every `major` and `major.minor` version. These aliases always point to the latest installed patch version and can be selected like the regular versions. Examples:
  - `asdf global ruby 3.2`
  - `asdf global nodejs 19`
  - `asdf global golang 1.20`
- {{< chip text="edge" >}} Default tool versions are now set to `major.minor` aliases and the exact patch version might change in the future:
  - Ruby: `3.2`
  - Golang: `1.20`
  - Node.js: `20.4`

### Stack update `v2023-07-12`

- {{< chip text="edge" >}} [Xcode 15 Beta 4](https://developer.apple.com/documentation/xcode-release-notes/xcode-15-release-notes) is available, replacing Beta 3.
- {{< chip text="edge" >}} {{< chip text="stable" >}} Some iOS simulator devices are pre-warmed for better performance. For each iOS runtime, the device `Bitrise iOS default` is already booted once (then shut down) so that the next boot during testing is faster and uses less CPU.
- {{< chip text="stable" >}} [Tuist](https://tuist.io) has been updated to version 3.19.

### Stack update `v2023-07-06`

This update is for {{< chip text="edge" >}} stacks {{< chip text="Xcode 14.3" >}} and {{< chip text="Xcode 15" >}} only.

- [Xcode 15 Beta 3](https://developer.apple.com/documentation/xcode-release-notes/xcode-15-release-notes) is available, replacing Beta 2.
- Tuist has been updated to [version 3.20](https://github.com/tuist/tuist/releases/tag/3.20.0)
- The following simulator runtimes are now installed:
  - iOS 16.4
  - tvOS 16.4
  - watchOS 9.4

### Stack update `v2023-07-03`

- {{< chip text="stable" >}} {{< chip text="Xcode 14.0-14.3" >}} Default Ruby version has changed from 2.7.6 to 3.2.2 according to the [deprecation plan](https://discuss.bitrise.io/t/ruby-2-7-x-deprecation/22544).

### Stack update `v2023-06-22`

- {{< chip text="stable" >}} {{< chip text="edge" >}} Ruby versions are now managed via [asdf](https://asdf-vm.com/). During the transition period, both `rbenv` and `asdf` are installed and can be used, but we recommend migrating to `asdf`, which also manages Node.js and Go versions on the stacks.
- {{< chip text="edge" >}} Default Ruby version has changed from 2.7.6 to 3.2.2 according to the [deprecation plan](https://discuss.bitrise.io/t/ruby-2-7-x-deprecation/22544).
- {{< chip text="stable" >}} {{< chip text="edge" >}} Each installed iOS simulator runtime now has a device named `Bitrise iOS default`. This name is constant across all runtime versions, but the real device type changes based on the iOS version. You can use this device name in test steps and destination specifiers and be sure that it’s going to be available across all Xcode and runtime versions.
- {{< chip text="stable" >}} {{< chip text="edge" >}} The `cmake;3.10.2.4988404` Android SDK package is now preinstalled
- {{< chip text="stable" >}} {{< chip text="edge" >}} [OpenUPM CLI](https://openupm.com/) is now preinstalled
- {{< chip text="edge" >}} [swift-format](https://github.com/apple/swift-format) is now preinstalled


