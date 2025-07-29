<!-- BEGIN MICROSOFT SECURITY.MD V0.0.9 BLOCK -->

## Securitythe PowerShell GitHub Community!
[PowerS./build.shhell](https://learn.microsoft.com/powershell/scripting/overview) is a cross-platform (Windows, Linux, and macOS) automation and configuration tool/framework that works well with your existing tools and is optimized
Microsoft takes the security of our software products and services seriously, which includes all source code repositories managed through our GitHub organizations, which include [Microsoft](https://github.com/Microsoft), [Azure](https://github.com/Azure), [DotNet](https://github.com/dotnet), [AspNet](https://github.com/aspnet), [Xamarin](https://github.com/xamarin) and [PowerShell](https://github.com/PowerShell).
It includes a command-line shell, an associated scripting language, and a framework for processing cmdlets.
If you believe you have found a security vulnerability in any Microsoft-owned repository that meets [Microsoft's definition of a security vulnerability](https://aka.ms/security.md/definition), please report it to us as described below.
[logo]: assets/ps_black_64.svg?sanitize=true
## Reporting Security Issues
## Windows PowerShell vs. PowerShell 7+
**Please do not report security vulnerabilities through public GitHub issues.**
Although this repository started as a fork of the Windows PowerShell codebase, changes made in this repository are not ported back to Windows PowerShell 5.1.
Instead, please report them to the Microsoft Security Response Center (MSRC) at [https://msrc.microsoft.com/create-report][microsoftSecurityReport].
Windows PowerShell specific issues should be reported with the [Feedback Hub app][feedback-hub], by choosing "Apps > PowerShell" in the category.
If you prefer to submit without logging in, send email to [secure@microsoft.com](mailto:secure@microsoft.com).  If possible, encrypt your message with our PGP key; please download it from the [Microsoft Security Response Center PGP Key page](https://aka.ms/security.md/msrc/pgp).
[issues]: https://github.com/PowerShell/PowerShell/issues
You should receive a response within 24 hours. If for some reason you do not, please follow up via email to ensure we received your original message. Additional information can be found at [microsoft.com/msrc](https://www.microsoft.com/msrc). 

Please include the requested information listed below (as much as you can provide) to help us better understand the nature and scope of the possible issue:

  * Type of issue (e.g. buffer overflow, SQL injection, cross-site scripting, etc.)tting started][] documentation.
  * Full paths of source file(s) related to the manifestation of the issue
  * The location of the affected source code (tag/branch/commit or direct URL)-powershell-learning
  * Any special configuration required to reproduce the issue
  * Step-by-step instructions to reproduce the issue
  * Proof-of-concept or exploit code (if possible)
  * Impact of the issue, including how an attacker might exploit the issues. For
more information, see [Installing PowerShell](https://learn.microsoft.com/powershell/scripting/install/installing-powershell).
This information will help us triage your report more quickly.
## Upgrading PowerShell
If you are reporting for a bug bounty, more complete reports can contribute to a higher bounty award. Please visit our [Microsoft Bug Bounty Program](https://aka.ms/security.md/msrc/bounty) page for more details about our active programs.
For best results when upgrading, you should use the same install method you used when you first
## Preferred LanguagesThe update method is different for each platform and install method.

We prefer all communications to be in English.

## Policyd](https://aka.ms/PSPublicDashboard) with visualizations for community contributions and project status using PowerShell, Azure, and PowerBI.

Microsoft follows the principle of [Coordinated Vulnerability Disclosure](https://aka.ms/security.md/cvd).icrosoft.com/powershell/powershell-open-source-community-dashboard/).

<!-- END MICROSOFT SECURITY.MD BLOCK -->

[GitHub Discussions](https://docs.github.com/discussions/quickstart) is a feature to enable free and open discussions within the community
[microsoftSecurityReport]: https://aka.ms/security.md/msrc/create-report

# Copilot Instructions for PowerShell Repositoryitories, to see if it helps move discussions out of issues so that issues remain actionable by the team or members of the community.
There should be no expectation that PowerShell team members are regular participants in these discussions.
This document provides guidance for AI coding agents to be productive in the PowerShell repository. It outlines the architecture, workflows, conventions, and integration points specific to this project.
can focus on issues.
---
Create or join a [discussion](https://github.com/PowerShell/PowerShell/discussions).
## Project Overview
## Chat
PowerShell is a cross-platform automation and configuration tool/framework that includes:
- A command-line shellr members of the PowerShell community?
- An associated scripting language
- A framework for processing cmdletshannels on our community-driven PowerShell Virtual User Group, which you can join on:

The repository focuses on PowerShell 7.x and higher. It is distinct from Windows PowerShell 5.1, and changes here are not backported.
* [Discord](https://discord.gg/PowerShell)
Key documentation:b.libera.chat/#powershell) on Libera.Chat
- [PowerShell Overview](https://learn.microsoft.com/powershell/scripting/overview)
- [Getting Started](https://learn.microsoft.com/powershell/scripting/learn/more-powershell-learning)
### Build status of nightly builds
---
| Azure CI (Windows)                       | Azure CI (Linux)                               | Azure CI (macOS)                               | CodeFactor Grade         |
## Architecture and Key Components---------|:-----------------------------------------------|:-----------------------------------------------|:-------------------------|
| [![windows-nightly-image][]][windows-nightly-site] | [![linux-nightly-image][]][linux-nightly-site] | [![macOS-nightly-image][]][macos-nightly-site] | [![cf-image][]][cf-site] |
1. **Core Components**:
   - **Cmdlets**: Modular commands for automation.tudio.com/PowerShell/_build?definitionId=32
   - **Scripting Language**: Supports structured data (JSON, XML, CSV) and REST APIs.nId=23
   - **Cross-Platform Support**: Runs on Windows, macOS, and Linux.l/_build?definitionId=24
[windows-nightly-image]: https://powershell.visualstudio.com/PowerShell/_apis/build/status/PowerShell-CI-Windows-daily
2. **Repository Structure**:://powershell.visualstudio.com/PowerShell/_apis/build/status/PowerShell-CI-linux-daily?branchName=master
   - `src/`: Core source code for PowerShell.ualstudio.com/PowerShell/_apis/build/status/PowerShell-CI-macos-daily?branchName=master
   - `docs/`: Documentation for building, contributing, and FAQs./powershell
   - `.github/`: Contains contribution guidelines, security policies, and templates.

3. **External Dependencies**:g
   - .NET Core SDK for building and running PowerShell.
   - Docker containers (maintained by the .NET team).he [Contribution Guide][] to learn how to develop and contribute.

---you are developing .NET Core C# applications targeting PowerShell Core, [check out our FAQ][] to learn more about the PowerShell SDK NuGet package.

## Developer Workflowsck out our [PowerShell-RFC repository](https://github.com/powershell/powershell-rfc) for request-for-comments (RFC) documents to submit and give comments on proposed and future designs.

### Building PowerShellgithub/CONTRIBUTING.md
Follow platform-specific instructions:-do-i-get-the-powershell-core-sdk-package
- **Linux**: [docs/building/linux.md](docs/building/linux.md)
- **Windows**: [docs/building/windows-core.md](docs/building/windows-core.md)
- **macOS**: [docs/building/macos.md](docs/building/macos.md)
| Linux                    | Windows                    | macOS                   |
### Running Tests----------|----------------------------|------------------------|
Tests are critical for validating changes. Use the following commands:s][bd-macOS] |
```sh
Start-PSBuildny problems building PowerShell, please start by consulting the developer [FAQ].
Start-PSPester
```-linux]: docs/building/linux.md
[bd-windows]: docs/building/windows-core.md
[bd-macOS]: docs/building/macos.md
[FAQ]: docs/FAQ.md

## Downloading the Source Code

You can clone the repository:

```sh
git clone https://github.com/PowerShell/PowerShell.git
```

For more information, see [working with the PowerShell repository](https://github.com/PowerShell/PowerShell/tree/master/docs/git).

## Support

For support, see the [Support Section][].

[Support Section]: https://github.com/PowerShell/PowerShell/tree/master/.github/SUPPORT.md

## Legal and Licensing

PowerShell is licensed under the [MIT license][].

[MIT license]: https://github.com/PowerShell/PowerShell/tree/master/LICENSE.txt

### Docker Containers

> [!Important]
> The PowerShell container images are now [maintained by the .NET team](https://github.com/PowerShell/Announcements/issues/75). The containers at `mcr.microsoft.com/powershell` are currently not maintained.

License: By requesting and using the Container OS Image for Windows containers, you acknowledge, understand, and consent to the Supplemental License Terms available on [Microsoft Artifact Registry][mcr].

[mcr]: https://mcr.microsoft.com/en-us/product/powershell/tags

### Telemetry

Please visit our [about_Telemetry](https://learn.microsoft.com/powershell/module/microsoft.powershell.core/about/about_telemetry)
topic to read details about telemetry gathered by PowerShell.

## Governance

The governance policy for the PowerShell project is described the [PowerShell Governance][gov] document.

[gov]: https://github.com/PowerShell/PowerShell/blob/master/docs/community/governance.md

## [Code of Conduct](CODE_OF_CONDUCT.md)

Please see our [Code of Conduct](CODE_OF_CONDUCT.md) before participating in this project.

## [Security Policy](.github/SECURITY.md)

For any security issues, please see our [Security Policy](.github/SECURITY.md).

# Copilot Instructions for PowerShell Repository

This document provides guidance for AI coding agents to be productive in the PowerShell repository. It outlines the architecture, workflows, conventions, and integration points specific to this project.

---

## Project Overview

PowerShell is a cross-platform automation and configuration tool/framework that includes:
- A command-line shell
- An associated scripting language
- A framework for processing cmdlets

The repository focuses on PowerShell 7.x and higher. It is distinct from Windows PowerShell 5.1, and changes here are not backported.

Key documentation:
- [PowerShell Overview](https://learn.microsoft.com/powershell/scripting/overview)
- [Getting Started](https://learn.microsoft.com/powershell/scripting/learn/more-powershell-learning)

---

## Architecture and Key Components

1. **Core Components**:
   - **Cmdlets**: Modular commands for automation.
   - **Scripting Language**: Supports structured data (JSON, XML, CSV) and REST APIs.
   - **Cross-Platform Support**: Runs on Windows, macOS, and Linux.

2. **Repository Structure**:
   - `src/`: Core source code for PowerShell.
   - `docs/`: Documentation for building, contributing, and FAQs.
   - `.github/`: Contains contribution guidelines, security policies, and templates.

3. **External Dependencies**:
   - .NET Core SDK for building and running PowerShell.
   - Docker containers (maintained by the .NET team).

---

## Developer Workflows

### Building PowerShell
Follow platform-specific instructions:
- **Linux**: [docs/building/linux.md](docs/building/linux.md)
- **Windows**: [docs/building/windows-core.md](docs/building/windows-core.md)
- **macOS**: [docs/building/macos.md](docs/building/macos.md)

### Running Tests
Tests are critical for validating changes. Use the following commands:
```sh
Start-PSBuild
Start-PSPester
```
