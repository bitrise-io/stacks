---
title: Xcode 26.5 changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-26.5.x.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2026-10-23` (released 2026-10-26)

- Update Homebrew `ca-certificates` (`2026-05-14` -> `2026-10-20`) to untrust the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/)
  - `curl` itself didn't need an update: it uses the certificates from Homebrew's `ca-certificates`, so it rejects the compromised CAs now
  - The same applies to OpenSSL and other tools that use Homebrew's OpenSSL trust store
  - `curl` itself didn't need an update: it uses the certificates from Homebrew's `ca-certificates`, so it rejects the compromised CAs now
  - The same applies to OpenSSL and other tools that use Homebrew's OpenSSL trust store

### Stack update `v2026-09-25` (released 2026-09-30)

- New preinstalled CLI tools: `1Password CLI`, `Sentry CLI`

### Stack update `v2026-08-13` released on `2026-08-17`

- Fix: Register the simulator app with launch services.

### Stack update `v2026-08-11`

- OS update 26.6.1 to address [Screen Sharing](https://support.apple.com/en-us/148170) vulnerability
- Bitrise CLI upgrade: `2.40.7` → `2.42.2`
- Bitrise guest agent upgrade: `2.2.0` → `2.10.1`
- Homebrew package upgrades

### Stack update `v2026-06-26`

- New preinstalled CLI tools: `ffmpeg`, `tmux`, `uv`
- Android SDK component `platforms;android-37.0` is now preinstalled

### Stack update `v2026-05-11`

Initial stack release with [Xcode 26.5](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_5-release-notes) (build `17F42`) on macOS 26.2 (25C56)
