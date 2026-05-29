---
title: Ubuntu Resolute 26.04 - Bitrise 2026 Edition
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html). This page is updated every time a new stack version is released.

{{< hint info >}}
Learn more [how to get notified of updates](../tips/Get%20notified.md).
{{< /hint >}}

## Updates

### Stack update `TODO`

Initial release of this new Linux stack. The stack is based on [Ubuntu 26.04 LTS](https://documentation.ubuntu.com/release-notes/26.04/), with further customizations and changes by Bitrise.

Compared to the previous Linux stack, [Ubuntu Noble 24.04 - Bitrise 2025 Edition](/stack_reports/ubuntu-noble-24-04-bitrise-2025-edition), the following notable changes are worth a mention:

#### `ubuntu` as the default user

Previously, builds were running with the `root` user by default. The root user and passwordless sudo is still available, but the default user is now `ubuntu`.

This change could case issues in two scenarios:

1. If your custom scripts rely on the elevated user (such as running `apt-get install` without `sudo`), you need to update your scripts to use `sudo`.
2. Hardcoded paths in scripts that include the username (such as `/home/root/.gradle`). Replace hardcoded parts with env vars like `$HOME` or `$USER`.

#### Ubuntu core packages

Updated system libraries and tools might cause unexpected issues when compiling C/C++ projects. Notable package updates in Ubuntu 26.04:

| Package           | Noble (24.04 LTS)       | Resolute (26.04 LTS)        |
| ----------------- | ----------- | --------------- |
| glibc             | 2.39        | **2.43**        |
| curl              | 8.5         | **8.18.0**      |
| GCC               | 13          | **15**          |
| LLVM/Clang        | 20          | **21**          |
| OpenSSL           | 3.0         | **3.5**         |

For all details and changes, check out the [Ubuntu 26.04 release notes](https://documentation.ubuntu.com/release-notes/26.04/).
