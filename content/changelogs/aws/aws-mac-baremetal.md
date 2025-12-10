---
title: macOS bare metal AMI changelog
summary: Changelog of stack updates
type: basic_page
---

Check out the [stack report page]({{% ref "/stack_reports/aws/aws-mac-baremetal.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### AMI version `2.109.1-sequoia26`

Updated version of the [macOS Sequoia-based stack](../../stack_reports/aws/aws-mac-baremetal.md) with the following Xcode versions:
- Xcode 26.0.1

#### AMIs by Region
- **us-east-1**: ami-0a9a3a3822b74750f
- **us-east-2**: ami-0bb898c6b2c23f0e2
- **us-west-2**: ami-09e55d600b3aa6b16
- **ca-central-1**: ami-0e838b513636e50a4
- **eu-central-1**: ami-052ff7da43a646f64
- **eu-west-1**: ami-02bdbf184a35a1486
- **ap-southeast-1**: ami-086dd31a1beb2b525
- **ap-southeast-2**: ami-090247970bf37633f

### Stack update `v2.77.1-sonoma16`

- Initial AWS AMI version with Xcode 16.0 and 16.1
- macOS version: 14.7.1

### Stack update `v2.54.0-sonoma15`

- Xcode 15.3.0 added
- MacOS version updated to Sonoma.
- Upgrade preinstalled tools (Node.js, Go, Ruby)
- Upgrade Homebrew packages

### Stack update `v2.54.0-ventura15`

- Xcode 15.2.0 added
- Upgrade preinstalled tools (Node.js, Go, Ruby)
- Upgrade Homebrew packages

### Stack update `v2.35.1`

- Upgrade Xcode to 15.0.1
- Upgrade preinstalled tools (Node.js, Go, Ruby)
- Upgrade Homebrew packages

### Stack update `v2.24.2`

Initial AWS AMI version with Xcode 14.0.1, 14.1 and 14.2.
