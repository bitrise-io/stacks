---
title: "Deprecating Xcode 16.x stacks"
type: basic_page
---

The Xcode 16.x stacks (`osx-xcode-16.0.x` through `osx-xcode-16.4.x`) will be deprecated on October 1, 2026, and will be removed on September 15, 2027.

{{< hint info >}}
Your builds continue to run on these stacks until the removal date. Read more about our [stack update policy here](https://docs.bitrise.io/en/bitrise-platform/infrastructure/build-stacks/stack-update-policy.html).
{{< /hint >}}

## Migration guide

We recommend migrating each workflow to a currently supported stack. The replacement is a newer major Xcode version in which tool versions are different, so expect this to involve more than changing the stack ID:

| Current stack | Current macOS | Migrate to | macOS after migration |
| --- | --- | --- | --- |
| `osx-xcode-16.0.x` | Sonoma 14.5 | [`osx-xcode-26.0.x`](../stack_reports/osx-xcode-26.0.x/) | Sequoia 15.7 |
| `osx-xcode-16.1.x` | Sonoma 14.5 | [`osx-xcode-26.0.x`](../stack_reports/osx-xcode-26.0.x/) | Sequoia 15.7 |
| `osx-xcode-16.2.x` | Sonoma 14.5 | [`osx-xcode-26.0.x`](../stack_reports/osx-xcode-26.0.x/) | Sequoia 15.7 |
| `osx-xcode-16.3.x` | Sequoia 15.7 | [`osx-xcode-26.0.x`](../stack_reports/osx-xcode-26.0.x/) | Sequoia 15.7 |
| `osx-xcode-16.4.x` | Sequoia 15.7 | [`osx-xcode-26.0.x`](../stack_reports/osx-xcode-26.0.x/) | Sequoia 15.7 |

Migrating from `osx-xcode-16.0.x`, `osx-xcode-16.1.x` or `osx-xcode-16.2.x` also upgrades macOS from Sonoma to Sequoia, so check that any scripts or tools that depend on the macOS version still work.

Ahead of the removal, any remaining projects with their `bitrise.yml` stored on bitrise.io will be migrated automatically to `osx-xcode-26.0.x`. If your `bitrise.yml` is committed to your git repository, please update the stack before September 15, 2027.

Since the automatic migration target is a newer major Xcode version, an auto-migrated build may fail. For example, your tests may target an older simulator that is not present on the newer stack. It is best to test your builds on the new stack well in advance of the removal date.

When migrating to `osx-xcode-26.0.x`, here are the major changes to be aware of:

### Simulators

| Platform | Preinstalled on `osx-xcode-26.0.x` | No longer preinstalled |
| --- | --- | --- |
| iOS | 17.5, 18.6, 26.0, 26.1, 26.2 | 15.5, 16.4, 18.0, 18.1, 18.2, 18.4, 18.5 |
| tvOS | 26.0, 26.1, 26.2 | 18.0, 18.1, 18.2, 18.4, 18.5 |
| watchOS | 11.5, 26.0, 26.1, 26.2 | 10.5, 11.0, 11.1, 11.2, 11.4 |
| visionOS | 26.0, 26.1, 26.2 | 2.0, 2.1, 2.3, 2.4, 2.5 |

Check the simulator destinations in your test steps before migrating.

### Ruby

Ruby 3.4 is now the default version, while Ruby 3.2 and 3.3 are also installed. Ruby 3.1 is no longer installed.

### Node.js

The previous default Node version, Node 20 is no longer installed. The new default is Node 22, while Node 24 is also installed.

### Go

Go 1.25 is now the default version, while Go 1.24 is also installed. Go 1.21 and 1.22 are no longer installed.

### Flutter

The preinstalled Flutter SDK has been upgraded from `3.22.0` to `3.32.0`.

### Python

Python 3.13 is the preinstalled version, replacing Python 3.12.

### Java

JDK 11, 17 and 21 are still installed, and JDK 17 remains the default.

You can learn more about selecting tool versions and installing additional ones [here](https://docs.bitrise.io/en/bitrise-ci/configure-builds/configuring-build-settings/configuring-tool-versions.html).
