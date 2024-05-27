---
title: Xcode 15.2 changelog
summary: Changelog of stack updates
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-15.2.x.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

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

### Stack update `v2024-03-04` (released on 2024-03-08)

- Brew dependency mirror update

### Stack update `v2024-02-21` (released on 2024-02-23)

- Brew dependency mirror update

### Stack update `v2024-02-13` (released on 2024-02-16)

- JDK 21 is now preinstalled
- Ruby 3.2 upgrade to 3.2.3 (it fixes some segmentation fault crashes)
- Brew dependency mirror update

### Stack update `v2024-02-05` (released on 2024-02-09)

- Brew dependency mirror update

### Stack update `v2024-01-23` (released on 2024-01-29)

- Brew dependency mirror update

### Stack update `v2024-01-15` (released on 2024-01-16)

- Brew dependency mirror update

### Stack update `v2024-01-09`

Initial stack release.
