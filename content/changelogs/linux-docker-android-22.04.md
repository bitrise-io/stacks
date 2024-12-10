---
title: Ubuntu 22.04 for Android & Docker
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html). This page is updated every time a new update is released to one of the [Linux-based stacks](/platform/linux).

{{< hint info >}}
Learn more [how to get notified of updates](../tips/Get%20notified.md).
{{< /hint >}}

## Updates

### Stack update `v2024-12-06` (released 2024-12-10)

- Ubuntu package upgrades
- Tooling version updates:
    - Ruby `3.1.5` → `3.1.6`
    - Ruby `3.2.4` → `3.2.5`
    - Ruby `3.3.4` → `3.3.5`

    - Go `1.21.10` → `1.21.13`
    - Go `1.22.3` → `1.22.7`

    - NodeJS `18.20.2` → `18.20.4`
    - NodeJS `20.13.1` → `20.17.0`

    - Python `3.12.2` → `3.12.6`


### Stack update `v2024-11-04`

- Android emulator upgrade: `35.1.20` -> `35.2.10`
- Ubuntu package upgrades

### Stack update `v2024-09-06`

- Tool upgrades:
    - Android emulator `34.2.15` -> `35.1.20`
    - Ruby `3.3.1` → `3.3.4`
- The Android 15 SDK components are now preinstalled (`platforms;android-35` and `system-images;android-35;google_apis;x86_64`).
- The Android 12 (version code 32) SDK components are no longer preinstalled as we keep only the last 3 versions preinstalled.
- The Google Cloud CLI `alpha` and `beta` components are now preinstalled, which lets you run [gcloud beta firebase](https://cloud.google.com/sdk/gcloud/reference/beta/firebase) subcommands.
- [pipx](https://github.com/pypa/pipx) is now installed, which lets you install and run Python executables without manually creating virtualenvs.
- Fix for running private steps in workflows via SSH git URLs. An SSH agent is now automatically started in the background (just like on macOS stacks) and the keys configured by the [Activate SSH key step](https://github.com/bitrise-steplib/steps-activate-ssh-key) are correctly used when downloading private steps.

### Stack update `v2024-06-06` (released 2024-07-11)

- Libraries required to compile Ruby from source are now preinstalled. Previously, some Ruby versions failed to build when running `asdf install ruby x.y.z`.
- Android emulator update: `34.2.14` -> `34.2.15`
- Various Ubuntu package upgrades


### Stack update `v2024-05-29`

- Tool upgrades
    - Android emulator `34.1.20` -> `34.2.14`
    - Ruby `3.1.4` → `3.1.5`
    - Ruby `3.2.3` → `3.2.4`
    - Ruby `3.3.0` → `3.3.1`
    - Go `1.21.6` → `1.21.10`
    - Go `1.22.0` → `1.22.3`
    - Node.js `18.19.1` -> `18.20.2`
    - Node.js `20.11.1` → `20.13.1`
    - Node.js `21.6.2` → `21.7.3`
    - Kotlin (system-wide) `2.0.0-Beta3` -> `2.0.0`

### Stack update `v2024-04-22`

- Android emulator upgrade: `34.1.19` -> `34.1.20`
- Fixed building OpenSSL-related dependencies (e.g. Ruby gems) from source by preinstalling the `libssl-dev` package
- Added an [Automated Test Device](https://developer.android.com/studio/test/gradle-managed-devices#gmd-atd) emulator system image (`system-images;android-34;aosp_atd;x86_64`)
- The Docker daemon is now configured to use `mirror.gcr.io` as a registry mirror ([more info](https://cloud.google.com/artifact-registry/docs/pull-cached-dockerhub-images))

### Stack update `v2024-03-18`

- Android emulator upgrade: `33.1.24` -> `34.1.19`
- Go `1.22` is now preinstalled, `1.20` is no longer installed
- Node.js minor and patch version upgrades (Node 18, 20, 21)

### Stack update `v2024-02-05` (released 2024-02-08)

- The `build-essential` meta-package (containing `gcc`, `libc-dev`, `make` and other packages) is now instaled. This fixes Ruby gem installs that depend on native code compilation.
- The `bzip` package and CLI command are now installed

### Stack update `v2024-01-24`

Initial release of this new stack based on Ubuntu 22.

A summary of changes compared to the Ubuntu 20.04 is [available here]({{% ref "/announcements/Ubuntu 22.md" %}}).

