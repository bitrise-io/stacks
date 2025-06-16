---
title: Ubuntu Noble (24) is available
type: basic_page
---

The [Ubuntu Noble - Bitrise 2025 stack](https://stacks.bitrise.io/stack_reports/ubuntu-noble-24.04-bitrise-2025/) is now available in public preview. This is another Linux stack recommended for Android workflows, but based on Ubuntu 24.04.

Besides the new OS version, the stack comes with various tool upgrades and we plan on updating these more frequently in the future following the principles of the newly made [Linux edge stack strategy](TODO).

{{< hint info >}}
Something missing? [Share your feedback here](https://github.com/bitrise-io/stacks/discussions/252)!
{{< /hint >}}

The changes are grouped into categories according to the related platforms:

## Android

### Preinstalled Android NDK upgrade

The preinstalled NDK has been upgraded to the current LTS version, `27.2.12479018`

### Kotlin CLI 2.1

The preinstalled Kotlin CLI is now version 2.1.

## React Native and Javascript

### Node 22 as default, Node 18 is no longer installed

The previous default Node version, Node 20 remains installed, but the new Bitrise stack makes Node 22 the default and additionally has Node 24. Node 18 and 21 are no longer preinstalled.

You can learn more about selecting tool versions and installing additional ones [here](https://stacks.bitrise.io/tips/tool-versions/).

## Flutter

### Preinstalled Flutter upgrade

The preinstalled Flutter SDK has been upgraded from `3.16.8` to `3.29.3`.

## Other tooling changes

### Ruby 3.4

Ruby 3.4 is now the default active version, while Ruby 3.3 and 3.2 are also installed.

### Python 3.13

Python 3.13 is the new preinstalled version replacing Python 3.12.

### Go 1.24

Go 1.24 is now the default active version, while Go 1.23 is also installed.

## Bazelisk

Bazelisk 1.26 is now preinstalled.
