---
title: Xcode 15.3 changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-15.3.x.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2025-07-21` (released 2025-07-22)

- The [pre-commit](https://github.com/pre-commit/pre-commit) CLI tool is now preinstalled
- The [licenseplist](https://formulae.brew.sh/formula/licenseplist) CLI tool is now preinstalled
- The [crowdin](https://www.npmjs.com/package/@crowdin/cli) CLI tool is now preinstalled

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

### Stack update `v2024-05-14`

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

No user-facing changes, this release is only caused by the new [Xcode 15.4 stack]({{ ref "/changelogs/osx-xcode-15.4.x.md" %}}).

### Stack update `v2024-05-07` (released on 2024-05-08)

- Homebrew package installs now use the [new JSON API introduced in Homebrew 4.0](https://brew.sh/2023/02/16/homebrew-4.0.0/). This should not make any difference in practice, but you can still revert to the old behavior by setting the `HOMEBREW_NO_INSTALL_FROM_API=1` env var.
- Related: the `brew-install` step has a [new major version](https://github.com/bitrise-steplib/steps-brew-install/releases/tag/1.0.0) that speeds up installs and make them more reproducible.

### Stack update `v2024-04-29` (released on 2024-05-01)

- Brew dependency mirror update

### Stack update `v2024-04-23` (released on 2024-04-26)

- Brew dependency mirror update
- google-cloud-sdk pre-installed

### Stack update `v2024-04-15` (released on 2024-04-18)

- Brew dependency mirror update

### Stack update `v2024-04-09` (released on 2024-04-11)

- Brew dependency mirror update

### Stack update `v2024-04-03` (released on 2024-04-04)

- Brew dependency mirror update. This also fixes [a recent Homebrew crash](https://github.com/Homebrew/homebrew-bundle/pull/1334) when running `brew bundle` or `brew services`.

### Stack update `v2024-03-18` (released on 2024-03-21)

- Brew dependency mirror update

### Stack update `v2024-03-12` (released on 2024-03-15)

- Brew dependency mirror update
- Ruby `3.3.0` added
- Ruby `3.2.2` is replaced by `3.2.3`
- Go `1.21.1` is replaced by `1.21.8`
- NodeJS `21.2.0` is replaced by `21.6.2`
- NodeJS `20.9.0` is replaced by `20.11.1`
- NodeJS `18.18.2` is replaced by `18.19.1`

To ensure your workflows remain efficient and utilize the most recent tool updates, we recommend using version aliases in your configurations. Version aliases help you automatically adopt new patch versions without the need for manual updates. For detailed information on how to use version aliases with your Bitrise stacks, please refer to our [Version Aliases Documentation](https://stacks.bitrise.io/tips/tool-versions/#version-aliases)

### Stack update `v2024-03-06`

Initial stack release.
