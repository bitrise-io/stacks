---
title: Upcoming stack deprecations
type: basic_page
tags: []

# DO update this date when adding a new stack deprecation
# DON'T update when archiving one or making other minor changes because we
# want to avoid an RSS feed update for unimportant changes
date: 2026-01-23
---

Stacks are not kept forever, older stacks are eventually marked for removal. You can read more about this in our [stack deprecation and removal policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-deprecation-and-removal-policy.html).

This page is an up-to-date overview of upcoming stack deprecations.

## Upcoming stack deprecations

The following table shows the currently deprecated stacks that are marked for removal.

While the stack is marked as deprecated, you can still run builds on it, but it's recommended to migrate your workflows to a more modern stack. On the day of removal, remaining users will be migrated to the stack shown in the _Automatic migration to_ column. If you encounter any difficulties during migration or require support, our dedicated [customer support team](https://support.bitrise.io) would be happy to assist.

| Stack ID                             | Deprecated from | Removal date  | Automatic* migration to                 |
| ------------------------------------ | --------------- | ------------- | --------------------------------------- |
| **linux-docker-android-22.04**       | 2026-04-08      | 2027-04-08    | ubuntu-noble-2404-bitrise-2025-android  |
| **osx-xcode-15.0.x**                 | 2025-10-01      | 2026-09-16    | osx-xcode-16.0.x                        |
| **osx-xcode-15.1.x**                 | 2025-10-01      | 2026-09-16    | osx-xcode-16.0.x                        |
| **osx-xcode-15.2.x**                 | 2025-10-01      | 2026-09-16    | osx-xcode-16.0.x                        |
| **osx-xcode-15.3.x**                 | 2025-10-01      | 2026-09-16    | osx-xcode-16.0.x                        |
| **osx-xcode-15.4.x**                 | 2025-10-01      | 2026-09-16    | osx-xcode-16.0.x                        |

* Automatic migration: when a project's `bitrise.yml` is [stored on bitrise.io](https://docs.bitrise.io/en/bitrise-ci/configure-builds/configuration-yaml/managing-a-project-s-configuration-yaml-file.html), we migrate all remaining projects before removal to the specified stack. When `bitrise.yml` is committed to the git repo, this is not possible and migration is the responsibility of the user.

## Archive

| Stack ID                             | Deprecated from | Removed       | Automatic migration to           |
| ------------------------------------ | --------------- | ------------- | -------------------------------- |
| **osx-xcode-13.3.x**                 | 2024-09-17      | 2024-10-01    | osx-xcode-14.3.x-ventura         |
| **osx-xcode-13.4.x**                 | 2024-09-17      | 2024-10-01    | osx-xcode-14.3.x-ventura         |
| **osx-xcode-13.0.x**                 | 2024-02-21      | 2024-03-20    | osx-xcode-13.4.x                 |
| **osx-xcode-13.0.x-rosetta**         | 2024-02-21      | 2024-03-20    | osx-xcode-14.2.x-ventura-rosetta |
| **osx-xcode-13.1.x**                 | 2024-02-21      | 2024-03-20    | osx-xcode-13.4.x                 |
| **osx-xcode-13.2.x**                 | 2024-02-21      | 2024-03-20    | osx-xcode-13.4.x                 |
| **osx-xcode-13.2.x-rosetta**         | 2024-02-21      | 2024-03-20    | osx-xcode-14.2.x-ventura-rosetta |
| **osx-xcode-13.3.x-rosetta**         | 2024-02-21      | 2024-03-20    | osx-xcode-14.2.x-ventura-rosetta |
| **osx-xcode-13.4.x-rosetta**         | 2024-02-21      | 2024-03-20    | osx-xcode-14.2.x-ventura-rosetta |
| **osx-xcode-14.0.x-ventura**         | 2024-02-21      | 2024-03-20    | osx-xcode-14.3.x-ventura         |
| **osx-xcode-14.0.x-ventura-rosetta** | 2024-02-21      | 2024-03-20    | osx-xcode-14.2.x-ventura-rosetta |
| **osx-xcode-14.1.x-ventura-rosetta** | 2024-02-21      | 2024-03-20    | osx-xcode-14.2.x-ventura-rosetta |
| **linux-docker-android-20.04**       | 2024-08-01      | 2025-04-02    | linux-docker-android-22.04       |
| **osx-xcode-14.1.x-ventura**         | 2025-06-24      | 2025-10-01    | osx-xcode-15.0.x                 |
| **osx-xcode-14.2.x-ventura**         | 2025-06-24      | 2025-10-01    | osx-xcode-15.0.x                 |
| **osx-xcode-14.3.x-ventura**         | 2025-06-24      | 2025-10-01    | osx-xcode-15.0.x                 |
