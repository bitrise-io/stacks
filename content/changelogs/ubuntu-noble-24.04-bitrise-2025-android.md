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

### Stack update `v2025-09-30` (released 2025-10-01)

- Android emulator upgrade: `35.5.10` -> `36.1.9`
- [bundletool](https://github.com/google/bundletool) is now in `$PATH`, no need to use `java /path/to/bundletool.jar` anymore
- [crowdin CLI](https://crowdin.github.io/crowdin-cli/) is now preinstalled
- [ripgrep](https://github.com/BurntSushi/ripgrep) (`rg`) is preinstalled and available to other CLI tools and scripts
- [pre-commit](https://github.com/pre-commit/pre-commit) is now preinstalled

### Stack update `v2025-06-18`

Initial release of this new Bitrise stack based on Ubuntu 24.04.

A summary of changes compared to the Ubuntu 22.04 is [available here]({{% ref "/announcements/Ubuntu Noble 2025.md" %}}).
