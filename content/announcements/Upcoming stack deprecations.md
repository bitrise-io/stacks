---
title: Upcoming stack deprecations
type: basic_page

# DO update this date when adding a new stack deprecation
# DON'T update when archiving one or making other minor changes
date: 2024-10-19
---

Stacks are not kept forever, older stacks are eventually marked for removal. You can read more about this in our [stack deprecation and removal policy](https://devcenter.bitrise.io/en/infrastructure/build-stacks/stack-deprecation-and-removal-policy.html).

This page is an up-to-date overview of upcoming stack deprecations.

## Upcoming stack deprecations

The following table shows the currently deprecated stacks that are marked for removal.

While the stack is marked as deprecated, you can still run builds on it, but it's recommended to migrate your workflows to a more modern stack. On the day of removal, remaining users will be migrated to the stack shown in the _Automatic migration to_ column. If you encounter any difficulties during migration or require support, our dedicated [customer support team](https://support.bitrise.io) would be happy to assist.

| Stack ID                             | Deprecated from | Removed after | Automatic migration to           |
| ------------------------------------ | --------------- | ------------- | -------------------------------- |
| **linux-docker-android-20.04**       | 2024-08-01      | 2025-04-02    | linux-docker-android-22.04       |
| **osx-xcode-13.3.x**                 | 2024-09-17      | 2024-10-01    | osx-xcode-14.3.x-ventura         |
| **osx-xcode-13.4.x**                 | 2024-09-17      | 2024-10-01    | osx-xcode-14.3.x-ventura         |

*Exact date to be announced

## Archive

| Stack ID                             | Deprecated from | Removed       | Automatic migration to           |
| ------------------------------------ | --------------- | ------------- | -------------------------------- |
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
