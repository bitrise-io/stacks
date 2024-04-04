---
title: Ubuntu 20.04 for Android & Docker
summary: Docker with pre-installed Android tooling, based on Ubuntu 20.04.
platform: Linux
architecture: x86_64
weight: 999
---

{{< hint info >}}
There is a newer Ubuntu stack available: [Ubuntu 22](./linux-docker-android-22.04.md)

This stack (Ubuntu 20) is soon going to be marked as deprecated ([timeline](../announcements/Upcoming%20stack%20deprecations.md)), we encourage everyone to switch their workflows to the [Ubuntu 22 stack](./linux-docker-android-22.04.md). You can find a summary of changes and migration guide [here](../announcements/Ubuntu%2022.md).
{{< /hint >}}

## Languages and runtimes

{{< languages filepath="data/linux-docker-android-20.04/languages.json" >}}

## CLI tools

### Android development

{{< generic filepath="data/linux-docker-android-20.04/android.json">}}
{{< android-sdk filepath="data/linux-docker-android-20.04/android-sdk.txt">}}

### Generic tools

{{< generic filepath="data/linux-docker-android-20.04/tools.json" >}}

### Global NPM packages

{{< generic filepath="data/linux-docker-android-20.04/npm.json">}}

### Bitrise-specific

{{< generic filepath="data/linux-docker-android-20.04/bitrise.json" >}}

## OS

{{< generic filepath="data/linux-docker-android-20.04/os.json" >}}

## APT packages

{{< apt filepath="data/linux-docker-android-20.04/apt.txt" >}}
