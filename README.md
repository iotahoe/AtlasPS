# AtlasPS
A draft PowerShell library for calling the Apache Atlas v2 API.

This is a **work in progress** and should be treated as such. Use at your own risk!

## Cmdlets


---
layout: module
permalink: /module/AtlasPS/
---
# [AtlasPS](https://atlassianps.org/module/AtlasPS)

[![GitHub release](https://img.shields.io/github/release/AtlassianPS/AtlasPS.svg?style=for-the-badge)](https://github.com/AtlassianPS/AtlasPS/releases/latest)
[![Build Status](https://img.shields.io/vso/build/AtlassianPS/AtlasPS/11/master.svg?style=for-the-badge)](https://dev.azure.com/AtlassianPS/AtlasPS/_build/latest?definitionId=11)
[![PowerShell Gallery](https://img.shields.io/powershellgallery/dt/AtlasPS.svg?style=for-the-badge)](https://www.powershellgallery.com/packages/AtlasPS)
![License](https://img.shields.io/badge/license-MIT-blue.svg?style=for-the-badge)

AtlasPS is a Windows PowerShell module to interact with Apache Atlas via a REST API using a consistent PowerShell look and feel.

Join the conversation on TBD.

<!--more-->

---

## Instructions

### Installation

Install AtlasPS from the [PowerShell Gallery]! `Install-Module` requires PowerShellGet (included in PS v5)

```powershell
# One time only install:
Install-Module AtlasPS -Scope CurrentUser

# Check for updates occasionally:
Update-Module AtlasPS
```

### Usage

```powershell
# To use each session:
Import-Module AtlasPS
Set-JiraConfigServer 'https://YourCloud.atlassian.net'
New-JiraSession -Credential $cred
```

You can find the full documentation on our [homepage](https://xxx) and in the console.

```powershell
# Review the help at any time!
Get-Help about_AtlasPS
Get-Command -Module AtlasPS
Get-Help Get-JiraIssue -Full # or any other command
```

For more information on how to use AtlasPS, check out the [Documentation](https://xxx/AtlasPS).

### Contribute

Want to contribute to AtlasPS? Great!
We appreciate everyone who invests their time to make these modules the best they can be.

Check out our guidelines on [Contributing] to our modules and documentation.

## Tested on

|Configuration|Status|
|-------------|------|
|Windows Powershell v5.1|[![Build Status](https://img.shields.io/vso/build/AtlassianPS/AtlasPS/11/master.svg?style=for-the-badge)](https://dev.azure.com/AtlassianPS/AtlasPS/_build/latest?definitionId=11)|
|Powershell Core (latest) on Windows|[![Build Status](https://img.shields.io/vso/build/AtlassianPS/AtlasPS/11/master.svg?style=for-the-badge)](https://dev.azure.com/AtlassianPS/AtlasPS/_build/latest?definitionId=11)|
|Powershell Core (latest) on Ubuntu|[![Build Status](https://img.shields.io/vso/build/AtlassianPS/AtlasPS/11/master.svg?style=for-the-badge)](https://dev.azure.com/AtlassianPS/AtlasPS/_build/latest?definitionId=11)|
|Powershell Core (latest) on MacOS|[![Build Status](https://img.shields.io/vso/build/AtlassianPS/AtlasPS/11/master.svg?style=for-the-badge)](https://dev.azure.com/AtlassianPS/AtlasPS/_build/latest?definitionId=11)|

## Acknowledgements

* Thanks to [replicaJunction] for getting this module on it's feet
* Thanks to everyone ([Our Contributors](https://atlassianps.org/#people)) that helped with this module

## Useful links

* [Source Code]
* [Latest Release]
* [Submit an Issue]
* [Contributing]
* How you can help us: [List of Issues](https://github.com/AtlassianPS/AtlasPS/issues?q=is%3Aissue+is%3Aopen+label%3Aup-for-grabs)

## Disclaimer

Hopefully this is obvious, but:

> This is an open source project (under the [MIT license]), and all contributors are volunteers. All commands are executed at your own risk. Please have good backups before you start, because you can delete a lot of stuff if you're not careful.

<!-- reference-style links -->
  [JIRA]: https://www.atlassian.com/software/jira
  [PowerShell Gallery]: https://www.powershellgallery.com/
  [Source Code]: https://github.com/AtlassianPS/AtlasPS
  [Latest Release]: https://github.com/AtlassianPS/AtlasPS/releases/latest
  [Submit an Issue]: https://github.com/AtlassianPS/AtlasPS/issues/new
  [replicaJunction]: https://github.com/replicaJunction
  [MIT license]: https://github.com/AtlassianPS/AtlasPS/blob/master/LICENSE
  [Contributing]: http://atlassianps.org/docs/Contributing

<!-- [//]: # (Sweet online markdown editor at http://dillinger.io) -->
<!-- [//]: # ("GitHub Flavored Markdown" https://help.github.com/articles/github-flavored-markdown/) -->
