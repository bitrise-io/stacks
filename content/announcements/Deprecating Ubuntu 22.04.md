---
title: "Deprecating Ubuntu 22.04"
type: basic_page
---

The [Ubuntu 22.04 stack](../stack_reports/linux-docker-android-22.04/) was deprecated on June 10, 2026, and will be removed on April 8, 2027.

{{< hint info >}}
This stack is marked as a frozen stack and will no longer receive updates. Your builds continue to run on this stack until the removal date. Read more about our [stack update policy here](https://devcenter.bitrise.io/en/infrastructure/build-stacks/linux-stack-update-policy.html).
{{< /hint >}}

## Migration guide

We recommend migrating your workflows to the [Ubuntu Noble 24.04 - Bitrise 2025 Edition stack](/stack_reports/ubuntu-noble-24.04-bitrise-2025-android/), which is the successor of this stack, and is the new stable stack. You can also migrate to our edge stack, [Ubuntu Resolute 26.04 - Bitrise 2026 Edition](../stack_reports/ubuntu-resolute-26.04-bitrise-2026-android/), which is the next generation of our Linux stacks, but it may have more breaking changes and less stability than the 24.04 stack.

When migrating to the new *stable* stack, here are the major changes to be aware of:

### Ruby

Ruby 3.4 is now the default version, while Ruby 3.3 and 4.0 are also installed. Ruby 3.1 and 3.2 are no longer installed.


### Node.js

The previous default Node version, Node 20 is no longer installed. The new default is Node 24, the current LTS version. Node 22 is also installed.

### Emulator system images

There are some emulator system images preinstalled to reduce your build times. As a new Android OS version is released, the matching system image and platform package is added to the stack.

Compared to the previous stable stack:

- `system-images` and `platform` version `33` are no longer installed
- `system-images` and `platform` version `36` are now preinstalled
- `system-images` and `platform` version `37.0` are now preinstalled

### Flutter

The preinstalled Flutter SDK has been upgraded from `3.16.8` to `3.38.7`.


### Go

Go 1.25 is now the default version, while Go 1.24 is also installed. Go 1.21 and 1.22 are no longer installed.

### Bazel

[Bazelisk](https://github.com/bazelbuild/bazelisk) is now installed. It also overrides `bazel` in `$PATH`, so any `bazel` execution will either respect your `.bazeliskrc`/`.bazelversion` file or download and execute the latest stable release of Bazel.

### Java

JDK 25 is now installed next to the existing versions.

You can learn more about selecting tool versions and installing additional ones [here](https://docs.bitrise.io/en/bitrise-ci/configure-builds/configuring-build-settings/configuring-tool-versions.html).


### Python

Python 3.13 is the preinstalled version, replacing Python 3.12. Python 3.14 is also installed.
