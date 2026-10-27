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
