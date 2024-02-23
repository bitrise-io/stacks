---
title: Upcoming stack changes for Xcode 14 and 15
type: basic_page
params:
  archived: true
bookHidden: true
---

According to our [stack update policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-update-policy.html) release of Xcode 15 GA means we'll be transitioning our current Edge stacks to the matching Stable stacks. This could present breaking changes for some workflows.

### Ruby

The default version doesn't change effectively (still `3.2.2`), but it's set as `3.2`. It's a special alias version that always points to the latest available patch version of Ruby 3.2.x. We recommend declaring one of the major.minor version aliases in workflows to ensure it remains functional even if the patch version is updated with the latest fixes.

- `3.1.0` and `3.1.3` replaced by `3.1.4`
- `3.2.1` replaced by `3.2.2`

An overview of Ruby versions across all Bitrise stacks is [available here]({{% ref "tools/ruby" %}}). We also offer [a guide for defining tool versions for reliable builds]({{% ref "tips/tool versions" %}}). 

### Node.js

The default version changes from `16.19.1` to `18`. It's a special alias version that always points to the latest available patch version of Node `18.x.y`. We recommend declaring one of the major version aliases in workflows to ensure it remains functional even if the patch version is updated with the latest fixes.

- Added: `20.x`
- Removed: `12.22.9` (no longer maintained, security support ended)
- Removed: `16.19.1` (no longer maintained, security support ended)
- Removed: `19.8.1` (superseded by Node 20, security support ended)

### Go

The default version changes from `1.20.2` to `1.21`. This is a special alias version that always points to the latest installed patch version of `1.21.x`. We recommend declaring one of the `major.minor` version aliases in workflows to ensure it remains functional even if the patch version is updated with the latest fixes.

- Added: `1.20`
- Added: `1.21`
- Removed: `1.18.10` (no longer supported)


### Apple simulator runtimes

Every Xcode stack contains a few additional (older) simulator runtimes preinstalled. This list is not changing for existing Xcode 14 stacks. For Xcode 15, these simulator runtimes are preinstalled:

- iOS 17.0
- iOS 16.4
- iOS 15.5
- watchOS 10.0
- watchOS 9.4
- tvOS 17.0
- visionOS 1.0

The [Xcode Test step](https://github.com/bitrise-steplib/steps-xcode-test) targets the latest iOS version by default. You can change its “Destination” input to one of the above.
