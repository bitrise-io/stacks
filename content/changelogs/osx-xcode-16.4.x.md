---
title: Xcode 16.4 changelog
summary: Changelog of stack updates
type: basic_page
---

Bitrise stacks are updated continuously according to the [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html).

Check out the [stack report page]({{% ref "/stack_reports/osx-xcode-16.4.x.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `v2025-07-07` (released 2025-07-14)

- **Device Pair Configuration**: Starting with Xcode 16.3, there are no pre-configured device pairs. Since this is a common requirement for CI users, we now recreate at least one device pair automatically:
  - Apple Watch Series 10 (46mm) paired with iPhone simulator

### Stack update `v2025-05-29` (released 2025-05-29)

Initial stack release
