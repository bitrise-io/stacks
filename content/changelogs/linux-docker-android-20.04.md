---
title: Ubuntu 20.04 for Android & Docker
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html). This page is updated every time a new update is released to one of the [Linux-based stacks](/platform/linux).

{{< hint info >}}
Learn more [how to get notified of updates](../tips/Get%20notified.md).
{{< /hint >}}

## Updates

{{< hint info >}}
There is a newer Ubuntu stack available: [Ubuntu 22](./linux-docker-android-22.04.md)

This stack (Ubuntu 20) is soon going to be marked as deprecated ([timeline]({{< ref "/announcements/Upcoming stack deprecations.md" >}})), we encourage everyone to switch their workflows to the [Ubuntu 22 stack](./linux-docker-android-22.04.md). You can find a summary of changes and migration guide [here](../announcements/Ubuntu%2022.md).
{{< /hint >}}

### Stack update `v2024-05-29`

- Tool upgrades
    - Android emulator `34.1.19` -> `34.2.14`
    - Ruby `3.3.0` → `3.3.1`
    - Go `1.21.5` → `1.21.10`
    - Node.js `18.19.1` -> `18.20.2`
    - Node.js `20.11.1` → `20.13.1`
    - Node.js `21.6.2` → `21.7.3`
    - Python `3.11.8` → `3.11.9` 

### Stack update `v2024-03-18`

- Android emulator upgrade: `33.1.24` -> `34.1.19`
- Ruby `3.3.0` is now preinstalled
- Node.js minor and patch version upgrades (Node 18, 20, 21)

### Stack update `v2024-01-08`

- Android emulator has been upgraded to `33.1.24`
- Go has been upgraded to `1.21`
- Node.js minor version updates: `20.9` to `20.10`, `21.1` to `21.2`
- Other minor CLI tool upgrades 

### Stack update `v2023-11-06`

- Multiple Node.js versions are now preinstalled via [ASDF]({{% ref "/tips/Tool versions.md" %}}):
  - Node 16 (default, just like before)
  - Node 18 (LTS with security support)
  - Node 20 (active LTS)
  - Node 21 (latest)
- Note: version files like `.node-version` and `.npmrc` are not automatically applied to avoid a breaking change. The only version file that has an effect on the selected version is `.tool-versions`.

### Stack update `v2023-08-28`

- Android SDK packages for Android 14 (`platforms;android-34` and `system-images;android-34;google_apis;x86_64`) and preinstalled. The `system-images;android-26` package is no longer preinstalled.

### Stack update `v2023-08-11`

- Android emulator has been upgraded to 32.1.14
- Removed system-wide Ruby 2 install according to the [deprecation timeline](https://discuss.bitrise.io/t/ruby-2-7-x-deprecation/22544)

### Stack update `v2023-08-07`

- [ASDF](https://asdf-vm.com/) version aliases: tools managed via ASDF got special alias versions for every `major` and `major.minor` version. These aliases always point to the latest installed patch version and can be selected like the regular versions. Examples:

  * `asdf global ruby 3.2`
  * `asdf global python 3.11`

- Android command-line tools package upgraded to 9.0
- Gradle (system-wide) updated to 8.2.1
- Kotlin (system-wide) updated to 1.9.0


### Stack update `v2023-06-28`

- The default Ruby version has changed from 2.7.6 to 3.2.2. See [the previous deprecation notice](https://discuss.bitrise.io/t/ruby-2-7-x-deprecation/22544) for more details. Reverting back to the previous default version can be done (for a limited time) by activating the system-wide Ruby version with `asdf global ruby system`.

### Stack update `v2023-06-09`

- The latest Android build tools versions are now preinstalled (added `33.0.1` and `34.0.0`)


