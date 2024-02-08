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

### Stack update `v2024-02-05` (released 2024-02-08)

- The `build-essential` meta-package (containing `gcc`, `libc-dev`, `make` and other packages) is now instaled. This fixes Ruby gem installs that depend on native code compilation.
- The `bzip` package and CLI command are now installed

### Stack update `v2024-01-24`

Initial release of this new stack based on Ubuntu 22.

A summary of changes compared to the Ubuntu 20.04 is [available here]({{% ref "/announcements/Ubuntu 22.md" %}}).

