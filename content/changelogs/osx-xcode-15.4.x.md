---
title: Xcode 15.4 changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-15.4.x.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2025-05-30` (released 2025-06-04)

- The [yq](https://github.com/mikefarah/yq) CLI tool is now preinstalled

### Stack update `v2025-02-13` (released on 2025-02-17)

- [Sourcery](https://github.com/krzysztofzablocki/Sourcery) and [XcodeGen](https://github.com/yonaskolb/XcodeGen) are now preinstalled.
- Minor and patch tool version upgrades:
  - Ruby `3.2.5` -> `3.2.6` (note: `3.2.5` is kept installed for one more release)
  - Ruby `3.3.6` -> `3.3.7` (note: `3.3.6` is kept installed for one more release)
  - Node.js `18.20.4` -> `18.20.5`
  - Node.js `20.17.0` -> `20.18.1`
- Node.js `corepack` has been upgraded to `0.29.4` in order to fix [this issue](https://github.com/nodejs/corepack/issues/612)

### Stack update `v2024-11-21` (released on 2024-11-26)

- No user-facing changes

### Stack update `v2024-10-15` (released on 2024-10-17)

- Minor and patch version upgrades:
  - Ruby `3.1.5` -> `3.1.6`
  - Ruby `3.2.4` -> `3.2.5`
  - Ruby `3.3.4` -> `3.3.5`
  - Go `1.21.10` -> `1.21.13`
  - Node.js `18.20.2` -> `18.20.4`
  - Node.js `20.13.1` -> `20.17.0`

### Stack update `v2024-09-19` (released on 2024-09-23)

- `cmake` has been upgraded to `3.30.3`, fixing [this regression](https://gitlab.kitware.com/cmake/cmake/-/issues/26128)

### Stack update `v2024-08-22` (released on 2024-08-27)

- Tool upgrades
    - Ruby `3.3.1` → `3.3.4`

### Stack update `v2024-07-12` (released on 2024-07-15)

- Pre-installed [pipx](https://github.com/pypa/pipx) for running Python executables and CLI tools

### Stack update `v2024-06-12` (released on 2024-06-13)

- No user-facing changes

### Stack update `v2024-05-24` (released on 2024-05-27)

- Tool upgrades
    - Ruby `3.0.6` → `3.0.7`
    - Ruby `3.1.4` → `3.1.5`
    - Ruby `3.2.3` → `3.2.4`
    - Ruby `3.3.0` → `3.3.1`
    - Go `1.20.8` → `1.20.14`
    - Go `1.21.8` → `1.21.10`
    - Node.js `18.19.1` → `18.20.2`
    - Node.js `20.11.1` → `20.13.1`
    - Node.js `21.6.2` → `21.7.3`

### Stack update `v2024-05-14`

Initial stack release.
