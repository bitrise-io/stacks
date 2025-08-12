---
title: Xcode 16.4 changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-16.4.x.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2025-08-11` (released v2025-08-12)

- Added: iOS 18.6 simulator runtime (iOS 18.5 remains installed, but you should try 18.6 if you experience stability issues)
- [pre-commit](https://github.com/pre-commit/pre-commit) CLI is now preinstalled
- [licenseplist](https://formulae.brew.sh/formula/licenseplist) CLI is now preinstalled
- [crowdin](https://www.npmjs.com/package/@crowdin/cli) CLI is now preinstalled

### Stack update `v2025-07-07` (released 2025-07-14)

- From now on, you can expect the simulator device `Bitrise iOS default` to be paired with an Apple Watch device

### Stack update `v2025-05-29` (released 2025-05-29)

Initial stack release
