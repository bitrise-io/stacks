---
title: Ubuntu 22 public preview
type: basic_page
---

The [Ubuntu 22 stack](https://stacks.bitrise.io/stack_reports/linux-docker-android-22.04/) is now available in public preview. This is another Linux stack recommended for Android workflows, but based on Ubuntu 22.04 instead of Ubuntu 20.04.

Besides the new OS version, the new stack has a few major changes that we long wanted to make, but we didn't want to break workflows running on the Ubuntu 20 stack.

{{< hint info >}}
Something missing? [Share your feedback here](https://github.com/bitrise-io/stacks/discussions/252)!
{{< /hint >}}

The changes are grouped into categories according to the related platforms:

## Android

### JDK 17 by default

By popular demand, JDK 17 is the new default version, matching the requirements of recent Android Gradle Plugin versions.

Other popular LTS versions are still installed (JDK 8, 11, 21), and the Set Java version step can be used to select another default at runtime like before.

### Android SDK CLI tools

The following CLI tools are now available in `$PATH`: `emulator`, `zipalign`, `aapt2`, `apksigner`

### Preinstalled Android NDK upgrade

The preinstalled NDK has been upgraded to the current LTS version, `26.1.10909125`

### Preinstalled emulator system images and platform versions

There are some emulator system images and platform versions preinstalled to reduce your build times. As a new Android OS version is released, the matching system image and platform package is added to the stack.

From now on, expect these packages to be available preinstalled:

- last 3 OS versions for emulator system images (Google API variant)
- last 3 platform packages

### `$ANDROID_NDK_HOME` is no longer defined

This env var has been deprecated for years and [modern Android Gradle Plugin versions ignore its value](https://github.com/android/ndk-samples/wiki/Configure-NDK-Path)

### Gradle, Maven, Ant are no longer installed

These build tools are not installed system-wide anymore. We recommend using Gradle wrapper or Maven wrapper and pinning an exact version of your build tool.

### Kotlin CLI 2.0

The preinstalled Kotlin CLI is now version 2.0 Beta 3 and we’ll update it to the final 2.0 release once it’s available.

## React Native and Javascript

### Node 20 as default, Node 16 is no longer installed

The previous default Node version, Node 16 [has reached its end-of-life](https://endoflife.date/nodejs). This new Bitrise stack version makes Node 20 (current LTS version) the default, and Node 16 is no longer preinstalled.

You can learn more about selecting tool versions and installing additional ones [here](https://stacks.bitrise.io/tips/tool-versions/).

### Active Node version is automatically selected based on `.node-version` or `.nvmrc` files

If the current working directory (your repo root typically) contains one of these files, the build environment automatically tries to activate the version declared in such a file.

Make sure that if your repo declares a Node version this way, the declared version is preinstalled (or install it at runtime). You can learn more about selecting tool versions and installing additional ones [here](https://stacks.bitrise.io/tips/tool-versions/).

### Corepack

Yarn and PNPM are installed with [corepack](https://nodejs.org/api/corepack.html). These package managers are installed for each preinstalled Node version.

**Possible breaking change**: corepack prevents running `npm install -g yarn`. If you want to use a different version of Yarn or PNPM, use the `packageManager` field in your `package.json` to declare the desired version.

## Flutter

### Preinstalled Flutter upgrade

The preinstalled Flutter SDK has been upgraded from `3.3.10` to `3.16.1`.

It is also now managed with ASDF, so you can install additional versions if needed.

## Other tooling changes

### Ruby 3.3

Ruby 3.3 is now the default active version, while Ruby 3.2 and 3.1 are also installed.

### AWS CLI v2

AWS CLI version 2 is the preinstalled version instead of version 1.

### Python 3

Python 2 is no longer preinstalled, Python 3.12 is the new preinstalled version.

### Docker Compose

Docker Compose is installed as [a Docker plugin](https://docs.docker.com/compose/install/linux/) instead of [a standalone binary](https://docs.docker.com/compose/install/standalone/).

See [this Docker article](https://docs.docker.com/compose/migrate/) for changes and the migration guide.

### Some default tool versions are aliases now

Tools that are managed with ASDF (thus multiple versions can be installed side-by-side) have special alias versions now. For example, even though `nodejs 20.6.1` is installed on the stack, it’s also available as `node 20` and `node 20.6`. In fact, the global default version is the `node 20` alias now.

If you previously declared an exact number in a `.tool-versions` file, we recommend pinning one of the available aliases as the exact versions might change as security updates are released to the tools.

Affected tools and runtimes:

- Go
- Ruby
- Node.js
- Python
- Flutter

### Go install

Go is now managed with ASDF.

**Possible breaking change**: If you install a Go binary to `$PATH` in your workflow via `go install`, you'll need to run `asdf reshim golang` before calling the binary.

### No longer preinstalled

The following CLI binaries are no longer preinstalled:

- `cmake`
- `gcc`
- `clang`
- ImageMagick `convert`

You can still install them from the Debian repositories at runtime.

