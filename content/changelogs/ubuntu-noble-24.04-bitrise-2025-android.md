---
title: Ubuntu Noble 24.04 - Bitrise 2025 Edition
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html). This page is updated every time a new update is released to one of the [Linux-based stacks](/platform/linux).

{{< hint info >}}
Learn more [how to get notified of updates](../tips/Get%20notified.md).
{{< /hint >}}

## Updates

### Stack update `v2026-01-22` (released 2026-01-23)

- Android NDK 27.1.12297006 added
- Fastlane upgrade: `2.230.0` -> `2.231.1`
- Ruby upgrades: `3.4.3` -> `3.4.8`, `3.3.8` -> `3.3.10`
- Ruby 4.0.1 added
- Ruby 3.2.8 removed
- Go upgrades: `1.24.3` -> `1.24.12`, added `1.25.6` (default)
- Go 1.23.9 removed
- Node.js upgrades: `22.15.0` -> `22.22.0`, `24.0.1` -> `24.13.0` (default)
- Node.js 20.19.1 removed
- NPM upgrade: `10.9.2` -> `11.6.2`
- Java: OpenJDK 25 added
- Kotlin upgrade: `2.1.21` -> `2.3.0`
- Firebase upgrade: `15.2.1` -> `15.3.1`
- Docker upgrade: `29.1.4` -> `29.1.5`
- Docker Compose upgrade: `5.0.1` -> `5.0.2`

### Stack update `v2026-01-14` (released 2026-01-15)

- [Lix](https://lix.systems/) (Nix-like) is preinstalled and configured
- `Python` additional preinstalled version: `3.14.2`
- Android emulator upgrade: `36.2.12` -> `36.3.10`

### Stack update `v2025-11-18` (released 2025-11-19)

No user-facing changes in this stack update.

### Stack update `v2025-11-13` (released 2025-11-17)

No user-facing changes in this stack update.

### Stack update `v2025-10-23` (released 2025-10-27)

- Android emulator upgrade: `36.1.9` -> `36.2.12`
- By popular demand, `build-tools;35.0.0` is also preinstalled for Android Gradle Plugin 8.x versions

### Stack update `v2025-09-30` (released 2025-10-01)

- Android emulator upgrade: `35.5.10` -> `36.1.9`
- [bundletool](https://github.com/google/bundletool) is now in `$PATH`, no need to use `java /path/to/bundletool.jar` anymore
- [crowdin CLI](https://crowdin.github.io/crowdin-cli/) is now preinstalled
- [ripgrep](https://github.com/BurntSushi/ripgrep) (`rg`) is preinstalled and available to other CLI tools and scripts
- [pre-commit](https://github.com/pre-commit/pre-commit) is now preinstalled

### Stack update `v2025-06-18`

Initial release of this new Bitrise stack based on Ubuntu 24.04.

A summary of changes compared to the Ubuntu 22.04 is [available here]({{% ref "/announcements/Ubuntu Noble 2025.md" %}}).
