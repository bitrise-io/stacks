---
title: Xcode 14.2 changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-14.2.x-ventura.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2024-05-07` (released on 2024-05-08)

- Homebrew package installs now use the [new JSON API introduced in Homebrew 4.0](https://brew.sh/2023/02/16/homebrew-4.0.0/). This should not make any difference in practice, but you can still revert to the old behavior by setting the `HOMEBREW_NO_INSTALL_FROM_API=1` env var.
- Related: the `brew-install` step has a [new major version](https://github.com/bitrise-steplib/steps-brew-install/releases/tag/1.0.0) that speeds up installs and make them more reproducible.

### Stack update `v2024-04-29` (released on 2024-05-01)

- Brew dependency mirror update

### Stack update `v2024-04-23` (released on 2024-04-26)

- Brew dependency mirror update
- google-cloud-sdk pre-installed

### Stack update `v2024-04-15` (released on 2024-04-18)

- Brew dependency mirror update

### Stack update `v2024-04-09` (released on 2024-04-11)

- Brew dependency mirror update

### Stack update `v2024-04-03` (released on 2024-04-04)

- Brew dependency mirror update. This also fixes [a recent Homebrew crash](https://github.com/Homebrew/homebrew-bundle/pull/1334) when running `brew bundle` or `brew services`.

### Stack update `v2024-03-18` (released on 2024-03-21)

- Brew dependency mirror update

### Stack update `v2024-03-12` (released on 2024-03-14)

- Brew dependency mirror update
- Ruby `3.3.0` added
- Ruby `3.2.2` is replaced by `3.2.3`
- Go `1.21.1` is replaced by `1.21.8`
- NodeJS `21.2.0` is replaced by `21.6.2`
- NodeJS `20.9.0` is replaced by `20.11.1`
- NodeJS `18.18.2` is replaced by `18.19.1`

To ensure your workflows remain efficient and utilize the most recent tool updates, we recommend using version aliases in your configurations. Version aliases help you automatically adopt new patch versions without the need for manual updates. For detailed information on how to use version aliases with your Bitrise stacks, please refer to our [Version Aliases Documentation](https://stacks.bitrise.io/tips/tool-versions/#version-aliases)

### Stack update `v2024-03-04` (released on 2024-03-08)

- Brew dependency mirror update

### Stack update `v2024-02-21` (released on 2024-02-23)

- Brew dependency mirror update

### Stack update `v2024-02-13` (released on 2024-02-16)

- JDK 21 is now preinstalled
- Ruby 3.2 upgrade to 3.2.3 (it fixes some segmentation fault crashes)
- Brew dependency mirror update

### Stack update `v2024-02-05` (released on 2024-02-09)

- Brew dependency mirror update

### Stack update `v2024-01-23` (released on 2024-01-26)

- Brew dependency mirror update

### Stack update `v2024-01-15` (released on 2024-01-16)

- Brew dependency mirror update

### Stack update `v2024-01-03` (released on 2024-01-10)

- Brew dependency mirror update

### Stack update `v2023-11-24` (released on 2023-11-27)

- Node 18 and 20 have been upgraded to the latest minor.patch versions
- Node 21 is now preinstalled
- Brew dependency mirror update

### Stack update `v2023-11-06` (released on 2023-11-09)

- Brew dependency mirror update

### Stack update `v2023-10-26` (released on 2023-10-31)

- Brew dependency mirror update

### Stack update `v2023-10-11` (released 2023-10-17)

[As previously announced]({{% ref "/announcements/2023 September.md" %}}), this update removes some end-of-life and unsupported tool version:

- Node 12 is no longer installed (end of life)
- Node 16 is no longer installed (end of life)
- Node 19 is no longer installed (end of life)
- Node 20 is now installed (20.6.1)
- Ruby `3.1.0` and `3.1.3` are replaced by `3.1.4`, `3.2.1` is replaced by `3.2.2`
- Default Ruby version is now `3.2` (instead of `3.2.2`), which is an alias pointing to the latest installed patch release (`3.2.2`)
- Go 1.18 is no longer installed (end of life)
- Go 1.20.2 upgraded to 1.20.8
- Go 1.21.1 is now preinstalled
- Brew package upgrades, including cURL version 8.4.0 ([more info]({{% ref "/announcements/curl-CVE-2023-38545.md" %}}))

For more information about tool versions, take a look at the [comparison tables]({{% ref "/tools" %}}) and [best practices declaring tool versions]({{% ref "/tips/Tool versions.md" %}}).

### Stack update `v2023-09-08`

- Brew dependency mirror update

### Stack update `v2023-08-28`

- Fix corrupted or missing files from simulator runtimes
- Fix brew cask related issues.

### Stack update `v2023-08-16`

- Brew cache updates
- Node v18 has been preinstalled along the existing versions. Reminder: Node [v16 is approaching End of Life](https://nodejs.org/en/blog/announcements/nodejs16-eol)

### Stack update `v2023-07-31`

- Brew cache update & security fixes.

### Stack update `v2023-07-18`

- Tool version aliases: tools managed via ASDF got special alias versions for every `major` and `major.minor` version. These aliases always point to the latest installed patch version and can be selected like the regular versions. Examples:
  - `asdf global ruby 3.2`
  - `asdf global nodejs 19`
  - `asdf global golang 1.20`

### Stack update `v2023-07-12`

- [Tuist](https://tuist.io) has been updated to version 3.19.

### Stack update `v2023-07-03`

- Default Ruby version has changed from 2.7.6 to 3.2.2 according to the [deprecation plan](https://discuss.bitrise.io/t/ruby-2-7-x-deprecation/22544).

### Stack update `v2023-06-22`

- Ruby versions are now managed via [asdf](https://asdf-vm.com/). During the transition period, both `rbenv` and `asdf` are installed and can be used, but we recommend migrating to `asdf`, which also manages Node.js and Go versions on the stacks.
- Default Ruby version has changed from 2.7.6 to 3.2.2 according to the [deprecation plan](https://discuss.bitrise.io/t/ruby-2-7-x-deprecation/22544).
- Each installed iOS simulator runtime now has a device named `Bitrise iOS default`. This name is constant across all runtime versions, but the real device type changes based on the iOS version. You can use this device name in test steps and destination specifiers and be sure that it’s going to be available across all Xcode and runtime versions.
- The `cmake;3.10.2.4988404` Android SDK package is now preinstalled
- [OpenUPM CLI](https://openupm.com/) is now preinstalled
