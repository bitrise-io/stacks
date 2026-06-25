---
title: "Removing Xcode 26 edge stacks"
type: basic_page
---

The Xcode 26 edge stacks (`osx-xcode-26.0.x-edge` through `osx-xcode-26.5.x-edge`) will be deprecated on July 1, 2026, and will be removed on August 1, 2026.

{{< hint info >}}
Each Xcode 26 version has a matching stable stack. Read more about our [stack update policy here](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).
{{< /hint >}}

## Migration guide

We recommend migrating each workflow to the matching stable stack:

| Edge stack              | Migrate to         |
| ----------------------- | ------------------ |
| `osx-xcode-26.0.x-edge` | `osx-xcode-26.0.x` |
| `osx-xcode-26.1.x-edge` | `osx-xcode-26.1.x` |
| `osx-xcode-26.2.x-edge` | `osx-xcode-26.2.x` |
| `osx-xcode-26.3.x-edge` | `osx-xcode-26.3.x` |
| `osx-xcode-26.4.x-edge` | `osx-xcode-26.4.x` |
| `osx-xcode-26.5.x-edge` | `osx-xcode-26.5.x` |

Alternatively, to stay on the edge channel, target your builds at the new `osx-xcode-27.0.x-edge` stack.

On the day of removal, any remaining projects with their `bitrise.yml` stored on bitrise.io will be migrated automatically to the matching stable stack. If your `bitrise.yml` is committed to your git repository, please update the stack before July 31, 2026.
