---
title: Xcode 26.3 changelog
summary: Changelog of stack updates
type: basic_page
---

## Updates

### Stack update `v2026-10-23` (released 2026-10-26)

- Next to [Apple's immediate certificate revocations](https://support.apple.com/en-us/149555), we untrust the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/) in Homebrew's trust store:
  - Homebrew `ca-certificates` upgrade: `2026-05-14` -> `2026-10-20`
  - This covers OpenSSL and other tools that use Homebrew's OpenSSL trust store
- The default `curl` has been changed to Homebrew `curl`, which uses the trust store updated for the eMudhra compromise. We recommend this version of `curl`. If your workflow requires the system `curl`, call it by its full path: `/usr/bin/curl`
- Bitrise CLI upgrade: `3.0.0` → `3.2.1`

### Stack update `v2026-09-25` (released 2026-09-29)

- New preinstalled CLI tools: `1password-cli`, `sentry-cli`

### Stack update `v2026-08-13` (released 2026-08-19)

- macOS update `15.4.1` → `15.7.9` to address [Screen Sharing](https://support.apple.com/en-us/148170) vulnerability
- Bitrise CLI upgrade: `2.40.7` → `2.42.2`
- Bitrise guest agent upgrade: `2.2.0` → `2.10.1`

### Stack update `v2026-06-30` (released 2026-07-02)

- New preinstalled CLI tools: `ffmpeg`, `tmux`, `uv`
- Android SDK component `platforms;android-37.0` is now preinstalled

### Stack update `v2025-02-26` (released 2026-02-27)

Initial stack release with [Xcode 26.3](https://developer.apple.com/documentation/xcode-release-notes/xcode-26_3-release-notes) (build `17C529`)
