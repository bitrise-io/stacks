---
title: macOS virtualized AMI changelog
summary: Changelog of stack updates
type: basic_page
---

This AMI listing has multiple actively updated versions:

- [macOS Sonoma with Xcode 16.0-16.1](../../stack_reports/aws/aws-mac-virtualized-sonoma16edge.md)
- [macOS Sonoma with Xcode 15.3-15.4](../../stack_reports/aws/aws-mac-virtualized-sonoma15.md)
- [macOS Ventura with Xcode 15.0-15.2](../../stack_reports/aws/aws-mac-virtualized-ventura15.md)

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### AMI version `2024W47-sonoma16`

Added the initial version stable stack [macOS Sonoma with Xcode 16.0-16.1](../../stack_reports/aws/aws-mac-virtualized-sonoma16.md) with the following Xcode versions:
- Xcode 16.0
- Xcode 16.1

### AMI version `2024W47-sonoma15`

Updated stable stack [macOS Sonoma with Xcode 15.3-15.4](../../stack_reports/aws/aws-mac-virtualized-sonoma15) with the following Xcode versions:
- Xcode 15.3
- Xcode 15.4

### AMI version `2024W47-ventura15`

Updatedn stable stack [macOS Sonoma with Xcode 15.0-15.2](../../stack_reports/aws/aws-mac-virtualized-sonoma15) with the following Xcode versions:
- Xcode 15.0
- Xcode 15.1
- Xcode 15.2

### AMI version `2024W37-sonoma16edge`

Added the edge stack [macOS Sonoma with Xcode 16.0-16.1](../../stack_reports/aws/aws-mac-virtualized-sonoma16edge.md) with the following Xcode versions:
- Xcode 16.0 RC
- Xcode 16.1 beta 1

### AMI version `2024W24-sonoma15` and `2024W24-ventura15`

- This AMI has been split into multiple active versions (two at the moment). From now on, each version contains only a single VM image. See what's included in these two versions [here](../../stack_reports/aws/aws-mac-virtualized-sonoma15.md) and [here](../../stack_reports/aws/aws-mac-virtualized-ventura15.md). This change results in smaller disk size per AMI version.
- Xcode 15.4 has been added to the `2024W24-sonoma15` version

### Stack update `v2024W14-1`

- Brew package updates
- Xcode 15.3 added

### Stack update `v2024W03`

- Brew package updates
- Xcode 15.2 added

### Stack update `v2023W47`

Initial version
