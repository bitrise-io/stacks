---
title: "New edge stack: Ubuntu Noble 24.04 Bitrise 2025 Edition"
type: basic_page
---

[Ubuntu Noble 24.04 - Bitrise 2025 Edition](https://stacks.bitrise.io/stack_reports/ubuntu-noble-24.04-bitrise-2025-android/) is now available as a new edge stack. This is another Linux stack, recommended for Android workflows and is based on Ubuntu 24.04.

Besides the new OS version, the stack comes with various tool upgrades and other, possibly breaking changes.

{{< hint info >}}
TODO
Something missing? [Share your feedback here](https://github.com/bitrise-io/stacks/discussions/252)!
{{< /hint >}}

## Android

### Android NDK upgrade

The preinstalled NDK packge has been upgraded to the current LTS version, `27.2.12479018`

### Emulator system images

There are some emulator system images preinstalled to reduce your build times. As a new Android OS version is released, the matching system image and platform package is added to the stack.

Our policy is to install:

- last 3 OS versions for emulator system images (Google API variant)
- last 3 platform packages

In practice, this means the following breaking changes this year:

- `system-images` and `platform` packages are now preinstalled for Android 36
- `system-images` and `platform` packages are no longer installed for Android 33

### Kotlin CLI 2.1

The preinstalled Kotlin CLI is now at version 2.1.

## React Native and Javascript

### Node 22 as default, Node 18 is no longer installed

The previous default Node version, Node 20 remains installed, but the new Bitrise stack makes Node 22 the default and additionally has Node 24 (the upcoming LTS version). Node 18 and 21 are no longer preinstalled.

You can learn more about selecting tool versions and installing additional ones [here](https://stacks.bitrise.io/tips/tool-versions/).

## Flutter

### Preinstalled Flutter upgrade

The preinstalled Flutter SDK has been upgraded from `3.16.8` to `3.29.3`.

## Bazel

[Bazelisk](https://github.com/bazelbuild/bazelisk) is now installed. It also overrides `bazel` in `$PATH`, so any `bazel` execution is going to either respect your `.bazeliskrc`/`.bazelversion` file or download and execute the latest stable release of Bazel.

## Other tooling changes

### Ruby 3.4

Ruby 3.4 is now the default version, while Ruby 3.3 and 3.2 are also installed. Ruby 3.1 is no longer installed.

### Python 3.13

Python 3.13 is the new preinstalled version, replacing Python 3.12.

### Go 1.24

Go 1.24 is now the default active version, while Go 1.23 is also installed. Go 1.21 is no longer installed.
