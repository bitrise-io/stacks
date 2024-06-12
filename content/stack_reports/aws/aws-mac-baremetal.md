---
title: macOS bare metal AMI
summary: "Bitrise on AWS: bare-metal macOS stack for building with Xcode"
type: stack_reports_aws
aws_url: "https://aws.amazon.com/marketplace/pp/prodview-hxvc5dqabjhus?sr=0-3&applicationId=AWSMPContessa"
platform: macOS
---

This version of the AMI contains the following software:

## Languages and runtimes

{{< languages filepath="data/aws-mac-baremetal/languages.json" >}}

## Simulators

Available runtimes and devices:

{{< simulators filepath="data/aws-mac-baremetal/simctl.json" >}}

## CLI tools

### Apple development

{{< generic filepath="data/aws-mac-baremetal/apple.json">}}

### Android development

{{< generic filepath="data/aws-mac-baremetal/android.json">}}
{{< android-sdk filepath="data/aws-mac-baremetal/android-sdk.txt" >}}

### Generic tools

{{< generic filepath="data/aws-mac-baremetal/tools.json" >}}

### Global NPM packages

{{< generic filepath="data/aws-mac-baremetal/npm.json">}}

### Bitrise-specific

{{< generic filepath="data/aws-mac-baremetal/bitrise.json" >}}

### Homebrew

{{< brew filepath="data/aws-mac-baremetal/brew.txt">}}

## OS

{{< generic filepath="data/aws-mac-baremetal/os.json" >}}
