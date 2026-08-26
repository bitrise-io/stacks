---
title: macOS minimal
summary: macOS stack without Xcode, for builds that don't need Apple developer tooling
platform: macOS
flavor: edge
weight: 31
---

Please note:

- **Disk space**: the minimal stack is exempt from the 100 GB free space guarantee.
- **Update timing**: updates are best effort. Our 24-hour SLO for Xcode updates doesn't extend to this stack. Update speed is still our priority for this stack, but new macOS versions often introduce breaking changes to image creation automation, making an aggressive SLO unfeasible.
- **Stack contents**: the minimal stack does not include the entire suite of pre-installed tools that would be found on other Xcode stacks, including simulator runtimes and Android tooling.


## Languages and runtimes

{{< languages filepath="data/osx-minimal/languages.json" >}}

## CLI tools

### Generic tools

{{< generic filepath="data/osx-minimal/tools.json" >}}

### Global NPM packages

{{< generic filepath="data/osx-minimal/npm.json">}}

### Bitrise-specific

{{< generic filepath="data/osx-minimal/bitrise.json" >}}

### Homebrew

{{< brew filepath="data/osx-minimal/brew.txt">}}

## OS

{{< generic filepath="data/osx-minimal/os.json" >}}
