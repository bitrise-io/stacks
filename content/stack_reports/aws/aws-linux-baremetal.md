---
title: Linux bare metal AMI
summary: "Bitrise on AWS: bare-metal Linux stack"
type: stack_reports_aws
aws_url: "https://aws.amazon.com/marketplace/pp/prodview-m66b4krh3qe2c"
platform: Linux
---

This version of the AMI contains the following software:

## Languages and runtimes

{{< languages filepath="data/aws-linux-baremetal/languages.json" >}}

## CLI tools

### Android development

{{< generic filepath="data/linux-docker-android-22.04/android.json">}}
{{< android-sdk filepath="data/linux-docker-android-22.04/android-sdk.txt">}}

### Android development

{{< generic filepath="data/aws-linux-baremetal/android.json">}}
{{< android-sdk filepath="data/aws-linux-baremetal/android-sdk.txt" >}}

### Generic tools

{{< generic filepath="data/aws-linux-baremetal/tools.json" >}}

### Global NPM packages

{{< generic filepath="data/aws-linux-baremetal/npm.json">}}

### Bitrise-specific

{{< generic filepath="data/aws-linux-baremetal/bitrise.json" >}}

## OS

{{< generic filepath="data/aws-linux-baremetal/os.json" >}}

## APT packages

{{< apt filepath="data/aws-linux-baremetal/apt.txt" >}}
