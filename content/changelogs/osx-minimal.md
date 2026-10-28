---
title: macOS minimal changelog
summary: Changelog of stack updates
type: basic_page
---

Please note:

- **Disk space**: the minimal stack is exempt from the 100 GB free space guarantee.
- **Update timing**: updates are best effort. Our 24-hour SLO for Xcode updates doesn't extend to this stack. Update speed is still our priority for this stack, but new macOS versions often introduce breaking changes to image creation automation, making an aggressive SLO unfeasible.
- **Stack contents**: the minimal stack does not include the entire suite of pre-installed tools that would be found on other Xcode stacks, including simulator runtimes and Android tooling.

## Updates

### Stack update `v2026-10-27` (released 2026-10-28)

- macOS update `27.2 beta 2 (26B5091g)` -> `27.2 (26B123)`
- Homebrew `ca-certificates` upgrade: `2026-08-13` -> `2026-10-20`, as part of untrusting the [compromised eMudhra intermediate CAs](https://emudhra.we-have-a-problem.com/)
- Bitrise CLI upgrade: `2.45.0` -> `3.2.1`
- Bitrise guest agent upgrade: `2.10.1` -> `2.10.2`
- Git upgrade: `2.55.0` -> `2.56.0`
- Git LFS upgrade: `3.8.0` -> `3.8.1`
- GitHub CLI upgrade: `2.101.0` -> `2.103.3`
- yq upgrade: `4.53.6` -> `4.54.1`
- AWS CLI upgrade: `2.36.50` -> `2.38.6`
- Google Cloud CLI upgrade: `586.0.0` -> `590.0.1`
- 1Password CLI upgrade: `2.39.0` -> `2.41.1`
- CMake upgrade: `4.4.3` -> `4.4.4`
- OpenVPN upgrade: `2.7.7` -> `2.7.8`
- Fastlane upgrade: `2.240.1` -> `2.241.2`
- Kotlin upgrade: `2.4.20` -> `2.4.21`
- LicensePlist upgrade: `3.28.2` -> `3.28.3`
- Go upgrade: `1.26.7` -> `1.26.10`, `1.27.0` -> `1.27.3`
- Node.js upgrade: `22.23.2` -> `22.23.4`, `24.19.0` -> `24.22.1`, `26.7.0` -> `26.12.1`
- NPM upgrade: `11.17.0` -> `11.19.1`
- Java upgrades: OpenJDK 17, 21, 25 patch updates
- pre-commit upgrade: `4.6.2` -> `4.7.0`
- uv upgrade: `0.12.17` -> `0.13.6`
- `applesimutils` removed: its Homebrew tap is no longer maintained and doesn't work with recent Homebrew versions. Use `xcrun simctl` instead.
- `aria2` removed
- Homebrew package upgrades

### Stack update `v2026-09-22`

- Update macOS 27.0 to [27.2 beta 2](https://developer.apple.com/documentation/macos-release-notes/macos-27_2-release-notes) (`26B5091g`)
- Homebrew package upgrades

### Stack update `v2026-08-26`

- Update macOS 27.0 to beta 7 (`26A5421a`)
- Homebrew package upgrades

### Stack update `v2026-08-25`

Update macOS 27.0 to beta 5 (`26A5406e`).

### Stack update `v2026-07-23`

Initial stack release on macOS 27.0 (`26A5388g`). This is a new stack which omits simulator runtimes.
