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

### Notice `v2026-10-26`

{{< hint warning >}}
This stack is [frozen](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html) and doesn't receive updates, so it still trusts the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/). Tools on macOS check certificates against one of three trust stores, and each one is affected differently:

- **Homebrew trust store** (Homebrew's `ca-certificates` package): used by tools built against Homebrew's OpenSSL, such as `wget`. Run `brew upgrade ca-certificates` in the beginning of your builds to install the fixed package and untrust the compromised CAs.
- **macOS system trust store** (`/etc/ssl/cert.pem`): used by the curl that ships with macOS and the tools built on it, such as `git`. `brew upgrade ca-certificates` doesn't change this file. Apple will fix it in a macOS update, which this stack won't receive. Until then, follow [Apple's instructions](https://support.apple.com/en-us/149555) in the beginning of your builds to remove the compromised root CAs from the file.
- **Apple's Security framework** (the keychain): used by Xcode and other tools that rely on Apple's networking APIs. Apple's Security framework does perform updates to certificate configuration data, but the timing of these updates is not guaranteed to happen early in the build (for example, before the first steps download their dependencies).

The preinstalled versions of Java, Node.js, pip, fastlane and other tools that bundle their own root certificates stay affected regardless of the trust stores above. Migrate to a supported stack, such as [Xcode 26.0]({{% ref "/stack_reports/osx-xcode-26.0.x.md" %}}), to receive tool updates and security patches. See the [migration guide]({{% ref "/announcements/Deprecating Xcode 16.x stacks.md" %}}).
{{< /hint >}}

### Stack update `v2026-09-24` (released 2026-09-25)

- New preinstalled CLI tools: `1Password CLI`, `Sentry CLI`

### Stack update `v2026-06-30` (released 2026-07-03)

- New preinstalled CLI tools: `ffmpeg`, `tmux`, `uv`
- Android SDK component `ndk;27.1.12297006` is now preinstalled, matching the current React Native default
- Android SDK component `platforms;android-35` is now preinstalled

### Stack update `v2026-02-20` (released 2026-02-23)

- The preinstalled Ruby versions are now built with `--enable-shared`. The `--disable-shared` option was required for compatibility with a past version of Xcode, but it is no longer necessary. Using `--enable-shared` allows Ruby gems with native extensions that depend on the shared Ruby library to work properly.

### Stack update `v2026-01-15` (released 2026-01-19)

- [Lix](https://lix.systems/) (Nix-like) is preinstalled and configured

### Stack update `v2025-09-15` (released 2025-09-18)

- [ripgrep](https://github.com/BurntSushi/ripgrep) (`rg`) is preinstalled and available to other tools

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
