---
title: Xcode 15.3 with edge updates changelog
summary: Changelog of stack updates
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-15.3.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

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

- [Xcode 15.3 Release Candidate 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_3-release-notes) is preinstalled, replacing Release Candidate.
- Brew packages updates

### Stack update `v2024-02-28`

- [Xcode 15.3 Release Candidate](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_3-release-notes) is preinstalled, replacing Beta 3.
- Brew packages updates

### Stack update `v2024-02-21` (released on 2024-02-23)

- Brew package updates

### Stack update `v2024-02-14`

- [Xcode 15.3 Beta 3](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_3-release-notes) is preinstalled, replacing Beta 2.
- Brew packages updates

### Stack update `v2024-02-07`

- This stack is now based on macOS Sonoma 14.1.2
- [Xcode 15.3 Beta 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_3-release-notes) is preinstalled, replacing Beta 1.
- Brew packages updates

### Stack update `v2024-01-26`

- Initial release of the stack
- [Xcode 15.3 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_3-release-notes) is preinstalled.


