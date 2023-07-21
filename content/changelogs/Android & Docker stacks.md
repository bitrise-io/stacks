---
title: Android & Docker stacks changelog
summary: This page is updated every time a new update is released to one of the [macOS-based Xcode stacks](/platform/linux).
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html). This page is updated every time a new update is released to one of the [Linux-based stacks](/platform/linux).

{{< hint info >}}
Learn more [how to get notified of updates](../tips/Get%20notified.md).
{{< /hint >}}

## Updates

### Stack update `v2023-06-28`

- The default Ruby version has changed from 2.7.6 to 3.2.2. See [the previous deprecation notice](https://discuss.bitrise.io/t/ruby-2-7-x-deprecation/22544) for more details. Reverting back to the previous default version can be done (for a limited time) by activating the system-wide Ruby version with `asdf global ruby system`.

### Stack update `v2023-06-09`

- The latest Android build tools versions are now preinstalled (added `33.0.1` and `34.0.0`)


