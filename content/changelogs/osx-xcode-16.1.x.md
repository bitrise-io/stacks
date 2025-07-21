---
title: Xcode 16.1 changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-16.1.x.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2025-07-18` (released 2025-07-21)

- The [pre-commit](https://github.com/pre-commit/pre-commit) CLI tool is now preinstalled
- The [licenseplist](https://formulae.brew.sh/formula/licenseplist) CLI tool is now preinstalled
- The [crowdin](https://www.npmjs.com/package/@crowdin/cli) CLI tool is now preinstalled

### Stack update `v2025-05-28` (released 2025-06-02)

- yq [added](https://formulae.brew.sh/formula/yq) 

### Stack update `v2025-02-13` (released on 2025-02-17)

- [Sourcery](https://github.com/krzysztofzablocki/Sourcery)is now preinstalled.
- Minor and patch tool version upgrades:
  - Ruby `3.2.5` -> `3.2.6` (note: `3.2.5` is kept installed for one more release)
  - Ruby `3.3.5` -> `3.3.7` (note: `3.3.5` is kept installed for one more release)
  - Node.js `20.17.0` -> `20.18.1`
  - Node.js `22.9.0` -> `22.13.0`
  - Go `1.22.7` -> `1.22.11`
  - Python `3.12.6` -> `3.12.8`
- Node.js `corepack` has been upgraded to `0.31.0` in order to fix [this issue](https://github.com/nodejs/corepack/issues/612)

### Stack update `v2024-12-11`

- [XcodeGen](https://github.com/yonaskolb/XcodeGen) CLI is now preinstalled

### Stack update `v2024-11-25` (released on 2024-11-26)

- No user-facing changes

### Stack update `v2024-10-29`

- Initial stack release
