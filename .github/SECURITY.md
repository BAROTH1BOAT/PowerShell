<!-- BEGIN MICROSOFT SECURITY.MD V0.0.9 BLOCK -->

## Security

Microsoft takes the security of our software products and services seriously, which includes all source code repositories managed through our GitHub organizations, which include [Microsoft](https://github.com/Microsoft), [Azure](https://github.com/Azure), [DotNet](https://github.com/dotnet), [AspNet](https://github.com/aspnet), [Xamarin](https://github.com/xamarin) and [PowerShell](https://github.com/PowerShell).

If you believe you have found a security vulnerability in any Microsoft-owned repository that meets [Microsoft's definition of a security vulnerability](https://aka.ms/security.md/definition), please report it to us as described below.

## Reporting Security Issues

**Please do not report security vulnerabilities through public GitHub issues.**

Instead, please report them to the Microsoft Security Response Center (MSRC) at [https://msrc.microsoft.com/create-report][microsoftSecurityReport].

If you prefer to submit without logging in, send email to [secure@microsoft.com](mailto:secure@microsoft.com).  If possible, encrypt your message with our PGP key; please download it from the [Microsoft Security Response Center PGP Key page](https://aka.ms/security.md/msrc/pgp).

You should receive a response within 24 hours. If for some reason you do not, please follow up via email to ensure we received your original message. Additional information can be found at [microsoft.com/msrc](https://www.microsoft.com/msrc). 

Please include the requested information listed below (as much as you can provide) to help us better understand the nature and scope of the possible issue:

  * Type of issue (e.g. buffer overflow, SQL injection, cross-site scripting, etc.)
  * Full paths of source file(s) related to the manifestation of the issue
  * The location of the affected source code (tag/branch/commit or direct URL)
  * Any special configuration required to reproduce the issue
  * Step-by-step instructions to reproduce the issue
  * Proof-of-concept or exploit code (if possible)
  * Impact of the issue, including how an attacker might exploit the issue

This information will help us triage your report more quickly.

If you are reporting for a bug bounty, more complete reports can contribute to a higher bounty award. Please visit our [Microsoft Bug Bounty Program](https://aka.ms/security.md/msrc/bounty) page for more details about our active programs.

## Preferred Languages

We prefer all communications to be in English.

## Policy

Microsoft follows the principle of [Coordinated Vulnerability Disclosure](https://aka.ms/security.md/cvd).

<!-- END MICROSOFT SECURITY.MD BLOCK -->


[microsoftSecurityReport]: https://aka.ms/security.md/msrc/create-report

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
