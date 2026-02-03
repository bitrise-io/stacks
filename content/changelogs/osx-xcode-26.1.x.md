---
title: Xcode 26.1 with changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-26.1.x.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2026-02-03` (released 2026-02-04)

- The Ruby 3.3.9 version that is pre-built on the stack is now built with `--enable-shared`. It was previously built with `--disable-shared`. The `--disable-shared` option was required for compatibility with a past version of Xcode, but it is no longer necessary. Using `--enable-shared` allows Ruby gems with native extensions that depend on the shared Ruby library to work properly. We plan to use `--enable-shared` for all Ruby versions on this stack in a future update.

### Stack update `v2026-01-14` (released 2026-01-15)

- No customer facing change. Internal tooling update

### Stack update `v2025-12-15`

- Lix (Nix-like) is preinstalled and configured

### Stack update `v2025-11-12`

[Xcode 26.1.1](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_1-release-notes) (build `17B100`)

### Stack update `v2025-11-04`

Initial stack release with [Xcode 26.1](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_1-release-notes) (build `17B55`)
