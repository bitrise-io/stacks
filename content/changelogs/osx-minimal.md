---
title: macOS minimal changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-minimal.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

Please note:

- **Disk space**: the minimal stack is exempt from the 100 GB free space guarantee.
- **Update timing**: updates are best effort. Our 24-hour SLO for Xcode updates doesn't extend to this stack. Update speed is still our priority for this stack, but new macOS versions often introduce breaking changes to image creation automation, making an aggressive SLO unfeasible.
- **Stack contents**: the minimal stack does not include the entire suite of pre-installed tools that would be found on other Xcode stacks, including simulator runtimes and Android tooling.

## Updates

### Stack update `v2026-08-26`

- Update macOS 27.0 to beta 7 (`26A5421a`)
- Homebrew package upgrades

### Stack update `v2026-08-25`

Update macOS 27.0 to beta 5 (`26A5406e`).

### Stack update `v2026-07-23`

Initial stack release on macOS 27.0 (`26A5388g`). This is a new stack which omits simulator runtimes.
