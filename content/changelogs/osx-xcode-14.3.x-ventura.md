---
title: Xcode 14.3 changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-14.3.x-ventura.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2024-02-13` (released on 2024-02-16)

- JDK 21 is now preinstalled
- Ruby 3.2 upgrade to 3.2.3 (it fixes some segmentation fault crashes)
- Brew dependency mirror update

### Stack update `v2024-02-05` (released on 2024-02-09)

- Brew dependency mirror update

### Stack update `v2024-01-23` (released on 2024-01-29)

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

### Stack update `v2023-09-07`

- macOS has been upgraded from 13.2 to 13.5
- The default Go version had been incorrectly reported as `1.20` in the stack report. This is now fixed, the report displays the correct default Go version, which is `1.18`. Note: this is [soon going to change to Go 1.21](https://bitrise.io/blog/post/xcode-15-is-coming-with-major-stack-updates)
- Resolved various iOS simulator performance problems
- Android SDK packages `platform-33` and `platform-34` are now preinstalled
- Brew packages have been upgraded

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
