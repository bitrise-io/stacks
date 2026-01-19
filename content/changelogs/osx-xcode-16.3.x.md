---
title: Xcode 16.3 changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-16.3.x.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2026-01-15` (released 2026-01-19)

- [Lix](https://lix.systems/) (Nix-like) is preinstalled and configured

### Stack update `v2025-09-15` (released 2025-09-22)

- [ripgrep](https://github.com/BurntSushi/ripgrep) (`rg`) is preinstalled and available to other tools

### Stack update `v2025-08-11` (released v2025-08-12)

- Added: iOS 18.6 simulator runtime (iOS 18.5 remains installed, but you should try 18.6 if you experience stability issues)
- [pre-commit](https://github.com/pre-commit/pre-commit) CLI is now preinstalled
- [licenseplist](https://formulae.brew.sh/formula/licenseplist) CLI is now preinstalled
- [crowdin](https://www.npmjs.com/package/@crowdin/cli) CLI is now preinstalled

### Stack update `v2025-07-07` (released 2025-07-14)

- From now on, you can expect the simulator device `Bitrise iOS default` to be paired with an Apple Watch device

### Stack update `v2025-05-29` (released 2025-05-29)

- yq [added](https://formulae.brew.sh/formula/yq) 

### Stack update `v2025-05-09` (released 2025-05-13)

macOS upgrade from `15.2` to `15.4.1`, in anticipation for Xcode 16.4, which requires macOS 15.3+.

### Stack update `v2025-04-01`

Initial stack release
