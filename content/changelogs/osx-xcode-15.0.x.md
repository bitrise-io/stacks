---
title: Xcode 15.0 changelog
summary: Changelog of stack updates
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-15.0.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2023-11-15`

- The default Node.js version is now Node 20, the active LTS release
- Node 18 is no longer installed
- Node 21, the latest version is now preinstalled
- Ruby 3.0.0 and 3.0.3 have been replaced with 3.0.6, the latest 3.0.x Ruby
- Brew package upgrades

### Stack update `v2023-11-06` (released on 2023-11-09)

- Brew dependency mirror update

### Stack update `v2023-10-26` (released on 2023-10-31)

- Brew dependency mirror update

### Stack update `v2023-10-19` (released 2023-10-20)
- [Xcode 15.0.1](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_0_1-release-notes), is available replacing 15.0 GA

### Stack update `v2023-10-11` (released 2023-10-17)

- Brew package upgrades, including cURL version 8.4.0 ([more info]({{% ref "/announcements/curl-CVE-2023-38545.md" %}}))

### Stack update `v2023-09-20`

- Removed Ruby 3.1.3 as [previously announced]({{% ref "/announcements/2023 September.md" %}}). Version 3.1.4 is still installed and we'll keep the latest 3.1.x version installed.
- Go 1.21 updated to the latest patch version (1.21.1)
- Go 1.20 updated to the latest patch version (1.20.8)
- Node 20 updated to the latest minor.patch version (20.6.1)
- Brew package updates


### Stack update `v2023-09-13` (released on 2023-09-18)

Initial release of the Xcode 15 stable stack. Xcode 15 GA is the same as the RC (build number `15A240d`)
