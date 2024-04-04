---
title: Xcode 15.1 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-15.1.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2024-04-03` (released on 2024-04-04)

- Brew package upgrades. This also fixes [a recent Homebrew crash](https://github.com/Homebrew/homebrew-bundle/pull/1334) when running `brew bundle` or `brew services`.
- The on-disk [Cocoapods specs repo](https://github.com/CocoaPods/Specs.git) is no longer updated in every stack update. Since [Cocoapods 1.8](https://blog.cocoapods.org/CocoaPods-1.8.0-beta/), the new CDN mechanism is enabled by default for new projects. If a project `Podfile` still references `https://github.com/CocoaPods/Specs.git`, you should update it according to [the guide here](https://blog.cocoapods.org/CocoaPods-1.8.0-beta/) to avoid dependency install errors.

### Stack update `v2024-03-26` (released on v2024-03-27)

- Homebrew package installs now use the [new JSON API introduced in Homebrew 4.0](https://brew.sh/2023/02/16/homebrew-4.0.0/). This should not make any difference in practice, but you can still revert to the old behavior by setting the `HOMEBREW_NO_INSTALL_FROM_API=1` env var.
- Homebrew package updates

### Stack update `v2024-03-12` (released on 2024-03-14)

- Brew dependency mirror update
- Ruby `3.3.0` added
- Go `1.21.1` is replaced by `1.21.8`
- NodeJS `21.2.0` is replaced by `21.6.2`
- NodeJS `20.9.0` is replaced by `20.11.1`

To ensure your workflows remain efficient and utilize the most recent tool updates, we recommend using version aliases in your configurations. Version aliases help you automatically adopt new patch versions without the need for manual updates. For detailed information on how to use version aliases with your Bitrise stacks, please refer to our [Version Aliases Documentation](https://stacks.bitrise.io/tips/tool-versions/#version-aliases)

Please be advised that Ruby version 3.0.6 will reach end of life on March 31, 2024, and will be removed from our supported versions in the coming weeks. We encourage users to upgrade to a newer version of Ruby to ensure continued stability and support.

### Stack update `v2024-03-05`

- Brew packages updates

### Stack update `v2024-02-28`

- Brew packages updates

### Stack update `v2024-02-21` (released on 2024-02-23)

- Brew package updates

### Stack update `v2024-02-07`

- This stack is now based on macOS Sonoma 14.1.2
- Brew packages updates

### Stack update `v2024-01-15` (released on 2024-01-16)

- Brew dependency mirror update
-  Edge stacks will soon be transitioned to MacOS Sonoma

### Stack update `v2024-01-03` (released on 2024-01-10)

- Brew package updates

### Stack update `v2023-12-06` (released on 2023-12-06)

- - [Xcode 15.1 RC 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_1-release-notes) is available, replacing Beta 3
- visionOS is unavailable as it's no longer part of Xcode 15.1 RC 1
- Brew package updates

### Stack update `v2023-11-24` (released on 2023-11-29)

- Fixed duplicate iOS simulator devices for iOS 17.0
- Brew package updates

### Stack update `v2023-11-15`

- [Xcode 15.1 Beta 3](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_1-release-notes) is available, replacing Beta 2
- The default Node.js version is now Node 20, the active LTS release
- Node 18 is no longer installed
- Node 21, the latest version is now preinstalled
- Ruby 3.0.0 and 3.0.3 have been replaced with 3.0.6, the latest 3.0.x Ruby
- Brew package upgrades

### Stack update `v2023-11-06` (released on 2023-11-09)

- Brew package upgrades

### Stack update `v2023-10-27`

-  [Xcode 15.1 Beta 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_1-release-notes) is available, replacing Beta 1

### Stack update `v2023-10-12`

-  The brew provided cURL has been updated to version 8.4.0, more details: [cURL CVE-2023-38545](https://stacks.bitrise.io/announcements/curl-cve-2023-38545/)

### Stack update `v2023-10-04`

- Initial release of the stack
- [Xcode 15.1 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_1-release-notes) is preinstalled.


