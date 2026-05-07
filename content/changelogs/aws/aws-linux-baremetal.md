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

### Stack update `2026w19`

- **Major Language Version Updates** (Ruby, Go, Node.js, Python, Flutter)
- **Android SDK & Tools Updates** (Build-Tools, Emulator, NDK, Platform-Tools)
- **Bitrise Tooling Update** (Bitrise CLI, stepman, envman)
- **Development Tools Updates** (Docker, Git, AWS CLI, Firebase, GitHub CLI)

#### AMIs by Region

- **us-east-1:** ami-05da568d9fd23422a
- **us-east-2:** ami-0ebf11b61729a627a
- **us-west-2:** ami-00bc71586d7a1f2b7
- **eu-west-1:** ami-09c4e8e64e87e617f
- **eu-west-2:** ami-01aff8b361cf9beca
- **eu-central-1:** ami-0feb7beae9efd5530
- **ca-central-1:** ami-0d9d3f9372efb0abb
- **ap-southeast-1:** ami-095df2e0540e68138
- **ap-southeast-2:** ami-02a6183221e069eb6

#### Tooling Versions

- **Ruby**
  - **Available Versions:**
    - 3.3.10
    - **3.4.8** (marked as default)
    - 4.0.1
  - **Version Aliases:**
    - `3` ➜ 3.4.8
    - `3.3` ➜ 3.3.10
    - `3.4` ➜ 3.4.8
    - `4` ➜ 4.0.1
    - `4.0` ➜ 4.0.1

- **Go**
  - **Available Versions:**
    - **1.25** (marked as default)
    - 1.24.12
    - 1.25.6
  - **Version Aliases:**
    - `1` ➜ 1.25.6
    - `1.24` ➜ 1.24.12
    - `1.25` ➜ 1.25.6

- **Node.js**
  - **Available Versions:**
    - **24.13.0** (marked as default)
    - 22.22.0
  - **Version Aliases:**
    - `22` ➜ 22.22.0
    - `22.22` ➜ 22.22.0
    - `24` ➜ 24.13.0
    - `24.13` ➜ 24.13.0
    - `lts` ➜ 24

- **Java**
  - **Available Versions:**
    - **java-17-openjdk** (marked as default)
    - java-21-openjdk
    - java-25-openjdk
    - java-11-openjdk

- **Python**
  - **Available Versions:**
    - **3.14.2** (marked as default)
  - **Version Aliases:**
    - `3` ➜ 3.14.2
    - `3.14` ➜ 3.14.2

- **Flutter**
  - **Available Versions:**
    - **3.16.8-stable** (marked as default)
  - **Version Aliases:**
    - `3` ➜ 3.16.8-stable
    - `3.16` ➜ 3.16.8-stable
    - `3.16.8` ➜ 3.16.8-stable

- **Kotlin**
  - **Available Version:**
    - Kotlin version **2.0.0-release-341**

- **Android SDK**
  - **Build-Tools:** 35.0.1
  - **Emulator:** 36.5.11
  - **NDK:**
    - 26.1.10909125
    - 27.1.12297006
  - **Platform-Tools:** 37.0.0

- **Android Development Tools**
  - **Fastlane:** 2.233.1
  - **Bundletool:** 1.15.6

- **Python Tools (pipx)**
  - **pre-commit:** 4.2.0
  - **yamllint:** 1.35.1


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