---
title: "New stack: macOS minimal"
type: basic_page
---

[macOS minimal](https://stacks.bitrise.io/stack_reports/osx-minimal/) (`osx-minimal`) is now available. It's a trimmed-down macOS stack created for teams that building and testing macOS apps.

This stack carries less than our Xcode stacks do. Most notably, it ships without simulator runtimes.

There is no such thing as a macOS simulator runtime (you test a macOS app on the OS the tests run on). The machine's own macOS version is the test target, so the simulator runtimes on the Xcode stacks do nothing for a macOS test suite.

We'll keep `osx-minimal` on the latest macOS release, including betas, so you can run your macOS test suites against current targets.

## What's different

Two of our usual guarantees don't apply here:

- **Disk space**: this stack is exempt from the 100 GB free space guarantee.
- **Update timing**: updates are best effort. The 24-hour SLO we target for Xcode updates doesn't cover this stack. We will aggressively release new versions as quickly as we can, but new macOS versions often introduce breaking changes to image creation automation making the Xcode version 24 hour SLO unfeasible for macOS updates. 

## Feedback

The stack is new and we want to hear how it works for you. Write to [letsconnect@bitrise.io](mailto:letsconnect@bitrise.io) or find us in [our community Slack](https://bitrise.slack.com).
