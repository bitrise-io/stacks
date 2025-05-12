---
title: Xcode 16 is coming with major stack changes
type: basic_page
params:
  archived: true
bookHidden: true
---

According to our [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html), the release of stable Xcode 16 means we'll be transitioning our current Edge stack (with Xcode 16 Beta) to a new Stable stack. There are some breaking changes compared to older Stable stacks, so we collected those below, grouped into categories per platform.

{{< hint info >}}
Existing Stable stacks (Xcode 14.x and 15.x) won't receive these changes, only the upcoming Xcode 16.0 stack.
{{< /hint >}}

### General changes

#### macOS upgrade

This stack is based on the latest version of macOS Sonoma (macOS 14). If migrating from the Xcode 15.2 stack or earlier, this means a major OS version upgrade for you (the Xcode 15.3 and 15.4 stacks are already based on Sonoma).

#### Tuist

Tuist is now installed via its [asdf-tuist](https://github.com/asdf-community/asdf-tuist) version manager plugin. This means you can install additional versions with `asdf install tuist 4.1.0` and set as the active version with a `.tool-versions` file or with `asdf global tuist 4.1.0`.

#### Homebrew `NO_DEPENDENTS_CHECK`

Similar to the `brew-install` step’s [new default behavior](https://github.com/bitrise-steplib/steps-brew-install/releases/tag/1.0.0), the env var `HOMEBREW_NO_INSTALLED_DEPENDENTS_CHECK=1` is also defined on stacks. This tweak helps the speed and reproducibility of `brew install` calls in scripts. See the [step release notes](https://github.com/bitrise-steplib/steps-brew-install/releases/tag/1.0.0) for more details.

#### Default Ruby version: 3.3

The default Ruby version is now `3.3` (an alias to the latest `3.3.x` version). The previous default, `3.2` remains preinstalled.

#### Ruby 3.0 removed

Ruby 3.0 has been removed as [it’s no longer officially supported](https://endoflife.date/ruby). You can manually reinstall it by running `asdf install ruby 3.0.7`.

#### Other tool upgrades

*   Homebrew package upgrades: on Stable stacks, Homebrew packages are not upgraded after the initial release of a stack. When switching from a previous stable stack, you’ll see newer package versions. Our Edge stacks are updated weekly with the latest package versions, so you can check [the Xcode 16.0 Edge stack report](https://stacks.bitrise.io/stack_reports/osx-xcode-16.0.x-edge/) any time to get a snapshot.

*   Ionic CLI 6.x → 7.x

*   Cordova CLI 11.x → 12.x

*   Appcenter CLI 2.x → 3.x

*   OpenUPM CLI 1.x → 3.x

*   The default Go version is `1.22`. The previous default, `1.21` remains preinstalled.

*   Go 1.23 is now preinstalled

*   Go 1.20 is no longer installed

#### Python 2

Python 2 is no longer installed. `pyenv`, a Python version manager is still installed, so you can reinstall Python 2 at your own risk.

Related: [pipx](https://github.com/pypa/pipx), a tool to install Python executables is now installed and configured on stacks.

### Android

#### JDK 17 is the new default version

To better align with modern Android Gradle Plugin versions, JDK 17 is now the default Java version on stacks.

JDK 11 remains preinstalled and you can use the [Set Java version](https://github.com/bitrise-steplib/bitrise-step-set-java-version) step to switch.

JDK 8 is no longer preinstalled.

#### Android command-line tools

The Android SDK’s `cmdline-tools` package has been upgraded to the latest stable version.

`cmdline-tools` was previously installed (incorrectly) to `$ANDROID_HOME/cmdline-tools/cmdline-tools`, this is now fixed (the tools are at `$ANDROID_HOME/cmdline-tools/latest/bin`).

#### Android NDK

The previously installed NDK version, `24.0.8215888` has been replaced with [the current LTS version](https://developer.android.com/ndk/downloads), `26.3.11579264`.

You can use the [install-missing-android-tools](https://github.com/bitrise-steplib/steps-install-missing-android-tools) step to install another NDK version.

Previously, the NDK package was incorrectly installed to the `$ANDROID_HOME/ndk-bundle` directory, this is no longer the case.

The env vars `ANDROID_NDK_HOME` and `ANDROID_NDK_VERSION` are no longer defined as [modern Android Gradle Plugin versions don’t rely on them](https://github.com/android/ndk-samples/wiki/Configure-NDK-Path).

#### System-wide Gradle and Maven

Gradle and Maven are no longer installed system-wide as most projects use the [Gradle Wrapper](https://docs.gradle.org/current/userguide/gradle_wrapper.html) and [Maven Wrapper](https://maven.apache.org/wrapper/) to execute a pinned version of the build tools.

### React Native

#### Node.js 20 is the new default version

Node 20 (LTS) replaces Node 18 (previous LTS) as the default version. Node 18 is no longer preinstalled, but you can manually install it by running `asdf install node 18.20.3`.

Node 22 (the upcoming LTS release) is also preinstalled.

#### Corepack

[Corepack](https://nodejs.org/api/corepack.html) is now enabled for all installed Node.js versions. This means that you no longer need to install Yarn or pnpm manually if your project uses these dependency managers. As long as the `package.json` contains a `packageManager` field with a package constraint like `yarn@3.8.3`, any script step invoking `yarn` (or `pnpm`) will trigger Corepack that automatically downloads and caches the required version manager.

### Flutter

#### Default Flutter version

The preinstalled Flutter version has been upgraded from `3.7.12` to `3.22.0`.

The [Flutter Install step](https://github.com/bitrise-steplib/bitrise-step-flutter-installer) can be used to prepare the exact version that your project depends on.
