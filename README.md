# ZeroFailed.Deploy.PowerPlatform

[![Build Status](https://github.com/zerofailed/ZeroFailed.Deploy.PowerPlatform/actions/workflows/build.yml/badge.svg)](https://github.com/zerofailed/ZeroFailed.Deploy.PowerPlatform/actions/workflows/build.yml)
[![License](https://img.shields.io/github/license/zerofailed/ZeroFailed.Deploy.PowerPlatform.svg)](https://github.com/zerofailed/ZeroFailed.Deploy.PowerPlatform/blob/main/LICENSE)

A [ZeroFailed](https://github.com/zerofailed/ZeroFailed) extension that provides deployment features for Microsoft Power Platform environments and Dataverse solutions.

> **Status:** under development. The extension has no features yet, and no version has been released.

## Overview

| Component Type | Included | Notes |
| -------------- | -------- | ----- |
| Tasks          | planned  | |
| Functions      | planned  | |
| Processes      | no       | Designed to be compatible with the default process provided by the [ZeroFailed.Deploy.Common](https://github.com/zerofailed/ZeroFailed.Deploy.Common) extension |

For more information about the different component types, please refer to the [ZeroFailed documentation](https://github.com/zerofailed/ZeroFailed/blob/main/README.md#extensions).

The planned feature groups are listed below. Each one will be documented on the [HELP page](./HELP.md) as it is added.

- **Environments:**
  - ensure a pay-as-you-go billing policy and the environments linked to it;
  - Managed Environment features;
  - auditing settings;
  - environment copies.
- **Security:**
  - ensure Entra security groups;
  - Dataverse teams linked to those groups;
  - application users;
  - security role privileges.
- **Solution deployment:**
  - import solutions, unmanaged or managed, with deployment settings;
  - publish customisations;
  - smoke tests.
- **Backup and restore:**
  - environment backups;
  - table data export and restore, preserving record IDs.

Every task can be re-run safely. Destructive operations support a what-if mode, and take a backup first.

The extension depends on [ZeroFailed.Deploy.Azure](https://github.com/zerofailed/ZeroFailed.Deploy.Azure), which brings in [ZeroFailed.Deploy.Common](https://github.com/zerofailed/ZeroFailed.Deploy.Common). Use it together with [ZeroFailed.Build.PowerPlatform](https://github.com/zerofailed/ZeroFailed.Build.PowerPlatform), which builds the solution artefacts this extension deploys.

## Pre-requisites

Using the features in this extension requires:

- PowerShell 7.4 or later
- The [Power Platform CLI](https://learn.microsoft.com/power-platform/developer/cli/introduction) (`pac`)
- The `Az.Accounts` PowerShell module

## Building this extension

```pwsh
./build.ps1
```

This runs the build and the Pester tests, using [ZeroFailed.Build.PowerShell](https://github.com/zerofailed/ZeroFailed.Build.PowerShell).
