---
title: Xcode 27.0 changelog
summary: Changelog of stack updates
type: basic_page
---

## Updates

### Stack update `v2026-10-30` (released 2026-10-30)

- There is a new iOS 27.2 simulator runtime for iPhone Duo (build `24B91016s`) alongside the general-purpose iOS 27.2 simulator runtime (build `24B8117`). The `Bitrise iOS default` for iOS 27.2 remains the general-purpose simulator.
- New iOS 27.2 simulator device: iPad mini (A20 Pro)
- tvOS 27.2 simulator runtime installed
- New tvOS 27.2 simulator device: Apple TV 4K (4th generation)
- watchOS 27.2 simulator runtime installed
- visionOS 27.2 simulator runtime installed
- curl upgrade: `8.7.1` -> `8.22.0`
- Homebrew package upgrades

### Stack update `v2026-10-23` (released 2026-10-26)

- Next to [Apple's immediate certificate revocations](https://support.apple.com/en-us/149555), we untrust the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/) in Homebrew's trust store:
  - Homebrew `ca-certificates` upgrade: `2026-08-13` -> `2026-10-20`
  - `curl` itself didn't need an update: it uses the certificates from Homebrew's `ca-certificates`, so it rejects the compromised CAs now
  - The same applies to OpenSSL and other tools that use Homebrew's OpenSSL trust store

### Stack update `v2026-10-16` (released 2026-10-16)

- iOS 27.1 simulator runtime installed
- New iOS 27.1 simulator device: iPhone Duo
- Bitrise CLI upgrade: `2.43.4` -> `3.2.1`

### Stack update `v2026-09-15`

Initial stack release with [Xcode 27.0](https://developer.apple.com/documentation/xcode-release-notes/xcode-27-release-notes) (build `27A266a`) on macOS 26.6.2 (25G83)
