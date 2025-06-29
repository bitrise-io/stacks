---
title: Ubuntu Noble 24.04 - Bitrise 2025 Edition
summary: Docker with pre-installed Android tooling, based on Ubuntu 24.04.
platform: Linux
flavor: edge
architecture: x86_64
weight: 1000
---

## Languages and runtimes

{{< languages filepath="data/ubuntu-noble-24.04-bitrise-2025-android/languages.json" >}}

## CLI tools

### Android development

{{< generic filepath="data/ubuntu-noble-24.04-bitrise-2025-android/android.json">}}
{{< android-sdk filepath="data/ubuntu-noble-24.04-bitrise-2025-android/android-sdk.txt">}}

### Generic tools

{{< generic filepath="data/ubuntu-noble-24.04-bitrise-2025-android/tools.json" >}}

### Global NPM packages

{{< generic filepath="data/ubuntu-noble-24.04-bitrise-2025-android/npm.json">}}

### Bitrise-specific

{{< generic filepath="data/ubuntu-noble-24.04-bitrise-2025-android/bitrise.json" >}}

## OS

{{< generic filepath="data/ubuntu-noble-24.04-bitrise-2025-android/os.json" >}}

## APT packages

{{< apt filepath="data/ubuntu-noble-24.04-bitrise-2025-android/apt.txt" >}}
