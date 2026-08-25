---
title: "New stack: macOS minimal"
type: basic_page
---

[macOS minimal](https://bitrise.io/stacks/stack_reports/osx-minimal/) (`osx-minimal`) is now available. It's a trimmed-down macOS stack created for teams that building and testing macOS apps.

This stack carries less than our Xcode stacks do. Most notably, it ships without simulator runtimes and android tooling.

Why is a minimal stack useful? It is particularly useful for testing macOS apps on the latest OS. There is no such thing as a macOS simulator runtime. Instead, tests execute directly against the OS of the VM where they are running.

The `osx-minimal` stack will provide the latest macOS release, including betas, so you can run your macOS test suites against the latest targets.

## What's different

Two of our usual guarantees don't apply here:

- **Disk space**: this stack is exempt from the 100 GB free space guarantee.
- **Update timing**: updates are best effort. Our 24-hour SLO for Xcode updates doesn't extend to this stack. Update speed is still our priority for this stack, but new macOS versions often introduce breaking changes to image creation automation, making an aggressive SLO unfeasible.

## Feedback

We want to hear how this new stack works for you. Write to [letsconnect@bitrise.io](mailto:letsconnect@bitrise.io) or find us in [our community Slack](https://bitrise.slack.com).
