---
title: Xcode 15.4 with edge updates changelog
summary: Changelog of stack updates
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-15.4.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2024-05-28` (released on 2024-05-30)

- Homebrew package upgrades
- As WWDC 2024 comes with the debut of Xcode 16 Beta, Bitrise Edge stacks will be updated with the new version as soon as it is available. *After this release, Xcode 15.x Edge stacks will be discontinued.* You are recommended to switch your workflows either to the Xcode 15.x Stable stacks or to the new Xcode 16.0 Edge stack. Remaining Xcode 15.x Edge stack users will be migrated to the corresponding Xcode 15.x Stable stacks.

### Stack update `v2024-05-21`

- Homebrew package upgrades
- Ruby `3.0.6` has been removed as it reached [end-of-life](https://endoflife.date/ruby)
- Node.js 22 is now pre-installed (`22.1.0` at the moment)
- Tool upgrades
    - Ruby `3.1.4` → `3.1.5`
    - Ruby `3.2.3` → `3.2.4`
    - Ruby `3.3.0` → `3.3.1`
    - Go `1.21.8` → `1.21.10`
    - Go `1.22.1` → `1.22.3`
    - Node.js `20.11.1` → `20.13.1`
    - Node.js `21.6.2` → `21.7.3`

### Stack update `v2024-05-08`

- [Xcode 15.4 Release Candidate](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_4-release-notes) is preinstalled, replacing 15.4 Beta.
- Homebrew package upgrades

### Stack update `v2024-04-17`

- Initial release of the stack with [Xcode 15.4 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-15_4-release-notes).


