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

### Stack update `v2026-06-01`

Adds Android SDK 37 and removes Android SDK 34.
Standardizes all pre-installed Android emulator system images to [16kb page size](https://developer.android.com/guide/practices/page-sizes) emulators.

- Adds [uv](https://docs.astral.sh/uv/) `0.11.17`
- Fastlane upgrade: `2.233.0` -> `2.235.0`
- Google Cloud CLI upgrade: `565.0.0` -> `570.0.0`
- AWS CLI upgrade: `2.34.37` -> `2.34.56`
- Docker upgrade: `29.4.1` -> `29.5.2`
- Docker Compose upgrade: `5.1.3` -> `5.1.4`
- Firebase CLI upgrade: `15.15.0` -> `15.19.0`
- GitHub CLI upgrade: `2.91.0` -> `2.93.0`
- Node.js upgrade: `22.22.0` -> `22.22.3`
- NPM upgrade: `11.6.2` -> `11.13.0`
- Ubuntu package upgrades

### Stack update `v2026-05-29`

Initial release of this new Linux stack. The stack is based on [Ubuntu 26.04 LTS](https://documentation.ubuntu.com/release-notes/26.04/), with further customizations and changes by Bitrise.

Compared to the previous Linux stack, [Ubuntu Noble 24.04 - Bitrise 2025 Edition](/stack_reports/ubuntu-noble-24-04-bitrise-2025-edition), the following breaking changes could affect your builds:

#### `ubuntu` as the default user

Previously, builds were running as `root` by default. The root user and passwordless sudo is still available, but the default user is now `ubuntu`.

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
