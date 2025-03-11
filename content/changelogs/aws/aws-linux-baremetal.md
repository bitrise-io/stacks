---
title: Linux bare metal AMI changelog
summary: Changelog of stack updates
type: basic_page
---

Check out the [stack report page]({{% ref "/stack_reports/aws/aws-linux-baremetal.md" %}}) for a snapshot of what is currently installed.

{{< hint info >}}
Learn more [how to get notified of updates]({{% ref "/tips/Get notified" %}}).
{{< /hint >}}

## Updates

### Stack update `2025w10`

- **Bitrise Tooling Update** (Bitrise CLI, DEN Agent)

#### AMIs by Region

- **us-east-1:** ami-0d45c5a31ba8478c3
- **us-east-2:** ami-0b918029e0706081e
- **us-west-2:** ami-0f1ff09a846b98b0f
- **eu-central-1:** ami-0db875b8e10f24c34
- **ap-southeast-1:** ami-0ff663c9163f3e9f2
- **ap-southeast-2:** ami-08ca77869e71a9024

#### Tooling Versions

- **Ruby**
  - **Available Versions:**
    - 3.1.6
    - 3.2.5
    - **3.3.5** (latest, marked as default)
  - **Version Aliases:**
    - `3` ➜ 3.3.5
    - `3.1` ➜ 3.1.6
    - `3.2` ➜ 3.2.5
    - `3.3` ➜ 3.3.5

- **Go**
  - **Available Versions:**
    - **1.21** (marked as default)
    - 1.21.13
    - 1.22.7
  - **Version Aliases:**
    - `1` ➜ 1.22.7
    - `1.21` ➜ 1.21.13
    - `1.22` ➜ 1.22.7

- **Node.js**
  - **Available Versions:**
    - **20.17.0** (marked as default)
    - 18.20.4
    - 21.7.3
  - **Version Aliases:**
    - `18` ➜ 18.20.4
    - `20` ➜ 20.17.0
    - `21` ➜ 21.7.3
    - `lts` ➜ 20

- **Java**
  - **Available Versions:**
    - **java-17-openjdk** (marked as default)
    - java-21-openjdk
    - java-11-openjdk
    - java-8-openjdk

- **Python**
  - **Available Versions:**
    - **3.12.6** (marked as default)
  - **Version Aliases:**
    - `3` ➜ 3.12.6
    - `3.12` ➜ 3.12.6

- **Kotlin**
  - **Available Version:**
    - Kotlin version **2.0.0-release-341**

### Stack update `2024w30`

- Bitrise Tooling Update (Bitrise CLI, DEN Agent)
- JDK 17 is the new default version (JDK 11 remains installed)
- Android Related Updates: emulator 34.2.16, NDK: 26.1.10909125, Platform Tools: 35.0.1 