---
title: macOS minimal
summary: macOS stack without Xcode, for builds that don't need Apple developer tooling
platform: macOS
flavor: stable
weight: 31
---

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
