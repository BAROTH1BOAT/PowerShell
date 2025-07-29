# Copilot Instructions for PowerShell Codebase

Welcome to the PowerShell codebase! This document provides guidance for AI coding agents to be productive in this project. It outlines the architecture, workflows, conventions, and key integration points specific to this repository.

---

## Project Overview

This repository focuses on managing and automating PowerShell scripts and configurations. It includes environment-specific changes, extensions, and workflows for integrating with tools like Visual Studio Code and GitHub Copilot.

### Key Components
1. **Environment Configuration**:
   - Files like `Environment changes - PowerShell` define terminal environment variables for extensions such as `vscode.git` and `GitHub.copilot-chat`.
   - Example: `GIT_ASKPASS` and `VSCODE_GIT_ASKPASS_*` variables enable Git authentication workflows.

2. **Extensions and Integrations**:
   - The repository integrates with Visual Studio Code extensions, such as:
     - `vscode.git`: Handles Git operations.
     - `GitHub.copilot-chat`: Adds debugging commands like `copilot-debug`.

3. **Scripts and Automation**:
   - PowerShell scripts automate tasks and manage configurations. Follow naming conventions and modularize scripts for reusability.

---

## Developer Workflows

### Building and Testing
- **Build Process**:
  - Ensure PowerShell scripts are syntactically correct using `pwsh`:
    ```bash
    pwsh -Command "Test-Script <script-name>.ps1"
    ```
- **Testing**:
  - Use Pester for unit testing PowerShell scripts:
    ```bash
    Invoke-Pester -Path <test-folder>
    ```

### Debugging
- Use the `copilot-debug` command (enabled by `GitHub.copilot-chat`) for debugging workflows:
  ```bash
  copilot-debug <script-name>.ps1
  ```