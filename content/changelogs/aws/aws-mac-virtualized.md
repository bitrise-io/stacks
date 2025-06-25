---
title: macOS virtualized AMI changelog
summary: Changelog of stack updates
type: basic_page
---

This AMI listing has multiple actively updated versions:

- [macOS Sequoia with Xcode 16.3-16.4](../../stack_reports/aws/aws-mac-virtualized-sequoia16.md)
- [macOS Sonoma with Xcode 16.0-16.2](../../stack_reports/aws/aws-mac-virtualized-sonoma16.md)
- [macOS Sonoma with Xcode 15.3-15.4](../../stack_reports/aws/aws-mac-virtualized-sonoma15.md)
- [macOS Ventura with Xcode 15.0-15.2](../../stack_reports/aws/aws-mac-virtualized-ventura15.md)

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### AMI version `2025W23-sequoia16`

Initial version of the [macOS Sequoia-based stack](../../stack_reports/aws/aws-mac-virtualized-sequoia16.md) with the following Xcode versions:
- Xcode 16.4
- Xcode 16.3

#### AMIs by Region

- **us-east-1:** ami-0dbb5266c7baa512c
- **us-east-2:** ami-03b1882bfb80c1d95
- **us-west-2:** ami-0abb26131bf4d267c
- **ca-central-1:** ami-09b7876b1a2b2c488
- **eu-central-1:** ami-00fc7ce96a50a5b65
- **eu-west-1:** ami-03fc9848a5c65e98a
- **ap-southeast-1:** ami-030539c021bce597a
- **ap-southeast-2:** ami-09b77d46f2a38ac67

### AMI version `2025W16-sequoia16`

Initial version of the [macOS Sequoia-based stack](../../stack_reports/aws/aws-mac-virtualized-sequoia16.md) with the following Xcode versions:
- Xcode 16.3

#### AMIs by Region

- **us-east-1:** ami-0c8dd95a7dc4f47ea
- **us-east-2:** ami-07ad190b11a82ab79
- **us-west-2:** ami-06135a8d2e88b61ef
- **ca-central-1:** ami-0b739ab5a3c265725
- **eu-central-1:** ami-020747a087a34f2ad
- **eu-west-1:** ami-0c6dc68c85e983424
- **ap-southeast-1:** ami-0d763bc99b31fe9e5
- **ap-southeast-2:** ami-0094bd74a33c29db2

### AMI version `2025W14-sonoma16`

This is an update of the previous version (`2024W47-sonoma16`) with the following Xcode versions:
- Xcode 16.0
- Xcode 16.1
- Xcode 16.2

For more details, see [the changelog of the Xcode 16.x stack](../../osx-xcode-16.0.x.md).

#### AMIs by Region

- **us-east-1:** ami-0b650fe9860ca1779
- **us-east-2:** ami-05ed8d3660ccc8e72
- **us-west-2:** ami-09ba3dc5ac40daede
- **ca-central-1:** ami-0010e1f9cfe218e8f
- **eu-central-1:** ami-062fa6f421372c458
- **eu-west-1:** ami-0aad2c31d395844e6
- **ap-southeast-1:** ami-0fcabe355b6735c7b
- **ap-southeast-2:** ami-0e90ba71b1b25fce7

### AMI version `2024W47-sonoma16`

Added the initial version stable stack [macOS Sonoma with Xcode 16.0-16.1](../../stack_reports/aws/aws-mac-virtualized-sonoma16.md) with the following Xcode versions:
- Xcode 16.0
- Xcode 16.1

### AMI version `2024W47-sonoma15`

Updated stable stack [macOS Sonoma with Xcode 15.3-15.4](../../stack_reports/aws/aws-mac-virtualized-sonoma15) with the following Xcode versions:
- Xcode 15.3
- Xcode 15.4

### AMI version `2024W47-ventura15`

Updated stable stack [macOS Sonoma with Xcode 15.0-15.2](../../stack_reports/aws/aws-mac-virtualized-sonoma15) with the following Xcode versions:
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
