---
title: "Removing Xcode 15.x stacks"
type: basic_page
---

The Xcode 15.x stacks (`osx-xcode-15.0.x` through `osx-xcode-15.4.x`) have been deprecated since October 1, 2025, and will be removed on September 16, 2026.

{{< hint info >}}
These stacks are marked as frozen and no longer receive updates. Your builds continue to run on them until the removal date. Read more about our [stack update policy here](https://docs.bitrise.io/en/bitrise-platform/infrastructure/build-stacks/stack-update-policy.html).
{{< /hint >}}

## Migration guide

We recommend migrating each workflow to a currently supported stack. The replacement is a newer major version in which tool versions are different, so expect this to involve more than changing the stack ID:

| Current stack | Migrate to |
| --- | --- |
| `osx-xcode-15.0.x` | [`osx-xcode-16.0.x`](../stack_reports/osx-xcode-16.0.x/) |
| `osx-xcode-15.1.x` | [`osx-xcode-16.0.x`](../stack_reports/osx-xcode-16.0.x/) |
| `osx-xcode-15.2.x` | [`osx-xcode-16.0.x`](../stack_reports/osx-xcode-16.0.x/) |
| `osx-xcode-15.3.x` | [`osx-xcode-16.0.x`](../stack_reports/osx-xcode-16.0.x/) |
| `osx-xcode-15.4.x` | [`osx-xcode-16.0.x`](../stack_reports/osx-xcode-16.0.x/) |

Ahead of the removal, any remaining projects with their `bitrise.yml` stored on bitrise.io will be migrated automatically to `osx-xcode-16.0.x`. If your `bitrise.yml` is committed to your git repository, please update the stack before September 16, 2026.

Since the automatic migration target is a newer major Xcode version, an auto-migrated build may compile and behave differently — it prevents a hard failure, but it isn't a guarantee your build still passes. Migrate and test deliberately rather than relying on it.
