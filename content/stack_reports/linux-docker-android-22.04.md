---
title: Ubuntu 22.04 for Android & Docker
summary: Docker with pre-installed Android tooling, based on Ubuntu 22.04.
platform: Linux
flavor: stable
architecture: x86_64
weight: 999
---

## Languages and runtimes

{{< languages filepath="data/linux-docker-android-22.04/languages.json" >}}

## CLI tools

### Android development

{{< generic filepath="data/linux-docker-android-22.04/android.json">}}
{{< android-sdk filepath="data/linux-docker-android-22.04/android-sdk.txt">}}

### Generic tools

{{< generic filepath="data/linux-docker-android-22.04/tools.json" >}}

### Global NPM packages

{{< generic filepath="data/linux-docker-android-22.04/npm.json">}}

### Bitrise-specific

{{< generic filepath="data/linux-docker-android-22.04/bitrise.json" >}}

## OS

{{< generic filepath="data/linux-docker-android-22.04/os.json" >}}

## APT packages

{{< apt filepath="data/linux-docker-android-22.04/apt.txt" >}}
