---
title: Xcode 27.1 changelog
summary: Changelog of stack updates
type: basic_page
---

## Updates

### Stack update `v2026-10-30` (released 2026-10-30)

- There is a new iOS 27.2 simulator runtime for iPhone Duo (build `24B91016s`) alongside the general-purpose iPhone simulator runtime for iOS 27.2 (build `24B8117`). The `Bitrise iOS default` for iOS 27.2 remains the general-purpose simulator.
- New tvOS 27.2, watchOS 27.2, and visionOS 27.2 simulator runtimes
- New simulator devices: iPad mini (A20 Pro), Apple TV 4K (4th generation)
- The default `curl` has been changed to Homebrew `curl` (`8.7.1` -> `8.22.0`). If your workflow requires the system `curl`, call it by its full path: `/usr/bin/curl`
- Homebrew `7.0.10` -> `7.0.11`

### Stack update `v2026-10-23` (released 2026-10-26)

- Next to [Apple's immediate certificate revocations](https://support.apple.com/en-us/149555), we untrust the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/) in Homebrew's trust store:
  - Homebrew `ca-certificates` upgrade: `2026-08-13` -> `2026-10-20`
  - `curl` itself didn't need an update: it uses the certificates from Homebrew's `ca-certificates`, so it rejects the compromised CAs now
  - The same applies to OpenSSL and other tools that use Homebrew's OpenSSL trust store

### Stack update `v2026-10-16` (released 2026-10-16)

Initial stack release with [Xcode 27.1](https://developer.apple.com/documentation/xcode-release-notes/xcode-27_1-release-notes) (build `27A9275`) on macOS 26.6.2 (25G83)
