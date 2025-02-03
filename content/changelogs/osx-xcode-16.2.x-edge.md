---
title: Xcode 16.2 with edge updates changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-16.2.x-edge.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2025-01-27`  (released 2025-02-03)

- Homebrew package upgrades

### Tool version changes:
#### Ruby
- **Updated:**
  - `3.2.5` → `3.2.6`
  - `3.3.5` → `3.3.7`

#### Golang
- **Updated:**
  - `1.23.3` → `1.23.5`
  - `1.22.7` → `1.22.11`

#### Node.js
- **Deleted:**
  - `20.17.0`
- **Updated:**
  - `22.9.0` → `22.13.0`

#### Python
- **Updated:**
  - `3.12.6` → `3.12.8`
- **Added:**
  - `3.13.1`
  

### Stack update `v2025-01-03`  (released 2025-01-07)

- Fixed: Remote access screen sharing is not working. From now you can use the Remote Access on the Edge stack.

- Homebrew package upgrades

### Stack update `v2024-12-06`

**Known issue**: Remote access screen sharing is not working (SSH access does work). We are working on a fix.

- - [Xcode 16.2 RC](https://developer.apple.com/documentation/xcode-release-notes/xcode-16_2-release-notes) replaces Beta 3.
- Homebrew package upgrades

### Stack update `v2024-11-21`

**Known issue**: Remote access screen sharing is not working (SSH access does work). We are working on a fix.

- [Xcode 16.2 Beta 3](https://developer.apple.com/documentation/xcode-release-notes/xcode-16_2-release-notes) replaces Beta 2.
- OS upgrade from `macOS 15.0 (24A335)` to `macOS 15.1 (24B83)`
- Go `1.21` has been removed (reached end-of-life)
- Default Go version has changed to `1.22`
- Go `1.23` is now also installed
- Homebrew package upgrades

### Stack update `v2024-11-05`

**Known issue**: Remote access screen sharing is not working (SSH access does work). We are working on a fix.

- Homebrew package upgrades
- [Xcode 16.2 Beta 2](https://developer.apple.com/documentation/xcode-release-notes/xcode-16_2-release-notes) replaces Beta 1.

### Stack update `v2024-10-28` (released 2024-10-29)

**Known issue**: Remote access screen sharing is not working (SSH access does work). We are working on a fix.

- This stack is now based on macOS Sequoia (15.0)
- Homebrew package upgrades

### Stack update `v2024-10-24`

- Initial release of the stack with [Xcode 16.2 Beta 1](https://developer.apple.com/documentation/xcode-release-notes/xcode-16_2-release-notes).


