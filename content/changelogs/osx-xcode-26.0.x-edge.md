---
title: Xcode 26.0 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-26.0.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2025-07-15`

- Homebrew package upgrades
- Android Emulator updated `35.5.10` --> `35.6.11`
- platform-tools updated `35.0.2` --> `36.0.0`

### Stack update `v2025-07-09`

- [Xcode 26.0 Beta 3](https://developer.apple.com/documentation/xcode-release-notes/xcode-26-release-notes) (build `17A5276g`)
- `bundletool` is now installed
- Homebrew package upgrades

### Stack update `v2025-06-25`

- [Xcode 26.0 Beta 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-26-release-notes) (build `17A5241o`)
- Metal Toolchain, the new unbundled Xcode component is now installed
- From now on, you can expect the simulator device `Bitrise iOS default` to be paired with an Apple Watch device
- The Android NDK package has been upgraded to the current LTS release, `27.2.12479018`
- Homebrew package upgrades

### Stack update `v2025-06-19`

- Fixed: The list of installed iOS simulator runtimes now follows the usual Bitrise policy. This release ships with iOS 18.5 and 17.5 as the 2 older runtimes, resolving the previous issue where 17.5 and 16.4 were installed.
- Homebrew package upgrades

### Stack update `v2025-06-11`

iOS 18.5 simulator runtime is now installed as expected.

### Stack update `v2025-06-10`

Initial stack release with [Xcode 26.0 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-26-release-notes) (build `17A5241e`)

Known issue: the list of installed iOS simulator runtimes doesn't follow [the usual Bitrise policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html). In this release, `17.5` and `16.4` are the 2 older runtimes installed. This is going to be fixed in the next release, which will ship with iOS `18.5` and `17.5` as the 2 older runtimes.

Other changes compared to the Xcode 16.x Edge stacks:

- Ruby
    - `3.4.x` is now preinstalled
    - `3.1.x` is no longer preinstalled (reached end-of-life)
    - The default version is now `3.4.x`
- Golang
    - `1.24.x` is now preinstalled
    - `1.22.x` is no longer preinstalled (reached end-of-life)
    - The default version is now `1.24.x`
- Node.js `24.x`, the upcoming LTS version is now preinstalled
- Flutter upgrade: `3.22.0` -> `3.32.0`
- Tuist upgrade: `4.20.0` -> `4.50.2`
- Python `3.12.x` is no longer installed. `3.13.x` remains installed.
- Fixed: The `asdf-golang` plugin's [set-env script](https://github.com/asdf-community/asdf-golang?tab=readme-ov-file#use) is now sourced in shells.

