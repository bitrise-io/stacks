---
title: Ubuntu 24.04 for Android & Docker
summary: Docker with pre-installed Android tooling, based on Ubuntu 24.04.
platform: Linux
flavor: edge
architecture: x86_64
weight: 999
---

## Languages and runtimes

{{< languages filepath="data/ubuntu-noble-24.04-bitrise-2025/languages.json" >}}

## CLI tools

### Android development

{{< generic filepath="data/ubuntu-noble-24.04-bitrise-2025/android.json">}}
{{< android-sdk filepath="data/ubuntu-noble-24.04-bitrise-2025/android-sdk.txt">}}

### Generic tools

{{< generic filepath="data/ubuntu-noble-24.04-bitrise-2025/tools.json" >}}

### Global NPM packages

{{< generic filepath="data/ubuntu-noble-24.04-bitrise-2025/npm.json">}}

### Bitrise-specific

{{< generic filepath="data/ubuntu-noble-24.04-bitrise-2025/bitrise.json" >}}

## OS

{{< generic filepath="data/ubuntu-noble-24.04-bitrise-2025/os.json" >}}

## APT packages

{{< apt filepath="data/ubuntu-noble-24.04-bitrise-2025/apt.txt" >}}
