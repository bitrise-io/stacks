---
title: Xcode 26.1 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-26.1.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2026-02-03` (released 2026-02-04)

- Ruby versions that are pre-built on the stack are now built with `--enable-shared`. They were previously built with `--disable-shared`. The `--disable-shared` option was required for compatibility with a past version of Xcode, but it is no longer necessary. Using `--enable-shared` allows Ruby gems with native extensions that depend on the shared Ruby library to work properly.

### Stack update `v2026-01-12` (released 2026-01-13)

- Homebrew package upgrades

### Stack update `v2025-12-30` (released 2026-01-06)

- [Xcode 26.2](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_2-release-notes) (build `17C52`)
- macOS upgrade: `26.0 (25A354)` -> `26.2 (25C56)`
- Homebrew package upgrades

### Stack update `v2025-12-04`

- [Xcode 26.2 RC](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_2-release-notes) (build `17C48`)
- Homebrew package upgrades

### Stack update `v2025-11-19`

- [Xcode 26.2 Beta 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_2-release-notes) (build `17C5038g`)
- Homebrew package upgrades

### Stack update `v2025-11-05`

Initial stack release with [Xcode 26.2 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_2-release-notes) (build `17C5013i`)
