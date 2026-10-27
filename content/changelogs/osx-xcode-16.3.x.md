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

### Notice `v2026-10-26`

{{< hint warning >}}
This stack is [frozen](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html) and doesn't receive updates, so it still trusts the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/). Tools on macOS check certificates against one of three trust stores, and each one is affected differently:

- **Homebrew trust store** (Homebrew's `ca-certificates` package): used by tools built against Homebrew's OpenSSL, such as `wget`. Run `brew upgrade ca-certificates` in the beginning of your builds to install the fixed package and untrust the compromised CAs.
- **macOS system trust store** (`/etc/ssl/cert.pem`): used by the curl that ships with macOS and the tools built on it, such as `git`. `brew upgrade ca-certificates` doesn't change this file. Apple will fix it in a macOS update, which this stack won't receive. Until then, follow [Apple's instructions](https://support.apple.com/en-us/149555) in the beginning of your builds to remove the compromised root CAs from the file.
- **Apple's Security framework** (the keychain): used by Xcode and other tools that rely on Apple's networking APIs. Apple's Security framework does perform updates to certificate configuration data, but the timing of these updates is not guaranteed to happen early in the build (for example, before the first steps download their dependencies).

The preinstalled versions of Java, Node.js, pip, fastlane and other tools that bundle their own root certificates stay affected regardless of the trust stores above. Migrate to a supported stack, such as [Xcode 26.0]({{% ref "/stack_reports/osx-xcode-26.0.x.md" %}}), to receive tool updates and security patches. See the [migration guide]({{% ref "/announcements/Deprecating Xcode 16.x stacks.md" %}}).
{{< /hint >}}

### Stack update `v2026-09-25` (released 2026-09-28)

- New preinstalled CLI tools: `1Password CLI`, `Sentry CLI`

### Stack update `v2026-08-13` (released 2026-08-17)

- macOS update `15.4.1` → `15.7.9` to address [Screen Sharing](https://support.apple.com/en-us/148170) vulnerability
- Bitrise CLI upgrade: `2.40.7` → `2.42.2`
- Bitrise guest agent upgrade: `2.2.0` → `2.10.1`
- OpenSSH upgrade: `9.9p1` → `9.9p2`

### Stack update `v2026-06-30` (released 2026-06-30)

- New preinstalled CLI tools: `ffmpeg`, `tmux`, `uv`
- Android SDK component `ndk;27.1.12297006` is now preinstalled, matching the current React Native default

### Stack update `v2026-02-20` (released 2026-03-03)

- The preinstalled Ruby versions are now built with `--enable-shared`. The `--disable-shared` option was required for compatibility with a past version of Xcode, but it is no longer necessary. Using `--enable-shared` allows Ruby gems with native extensions that depend on the shared Ruby library to work properly.

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
