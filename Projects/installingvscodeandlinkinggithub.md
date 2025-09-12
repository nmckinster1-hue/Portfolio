# Installing VS Code and Linking GitHub

## Project Overview

### Project Goal

&nbsp;&nbsp;&nbsp;&nbsp;The goal of this project was to install and configure Visual Studio Code on Ubuntu to document labs and projects for my portfolio using Markdown. Objectives included:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Learning to install and manage applications via the Linux terminal.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Creating professional, well-formatted documentation to enhance a technical portfolio.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Developing familiarity with Linux file systems and software management in preparation for IT support tasks.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Practicing troubleshooting and problem-solving for real-world technical issues.

### Project Outcome

&nbsp;&nbsp;&nbsp;&nbsp;Successfully established a fully function documentation environment with version control. Demonstrated:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Software installation and configuration via terminal.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Git/GitHub setup, authentication, and repository management.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Problem-solving and troubleshooting of installation and authentication issues.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Creation of professional Markdown documentation to support workflow and knowledge sharing.

## Key Skill Demonstrated
&nbsp;&nbsp;&nbsp;&nbsp;* Linux system administration software installation, file navigation, and dependency troubleshooting.

&nbsp;&nbsp;&nbsp;&nbsp;* Git/GitHub configuration, repository management, and version control.

&nbsp;&nbsp;&nbsp;&nbsp;* Troubleshooting installation and authentication issues.

&nbsp;&nbsp;&nbsp;&nbsp;* Technical documentation using Markdown for reproducible workflows.

&nbsp;&nbsp;&nbsp;&nbsp;* Verification and testing to ensure system functionality and data integrity.

&nbsp;&nbsp;&nbsp;&nbsp;* Knowledge sharing and workflow standardization.

## Technologies Used

### Hardware

&nbsp;&nbsp;&nbsp;&nbsp;* Alienware m15 r3 laptop

&nbsp;&nbsp;&nbsp;&nbsp;* Encrypted 2TB Seagate HDD formatted in ext4

### Software

&nbsp;&nbsp;&nbsp;&nbsp;* Ubuntu 24.04.3 LTS

&nbsp;&nbsp;&nbsp;&nbsp;* Visual Studio Code

&nbsp;&nbsp;&nbsp;&nbsp;* Git

&nbsp;&nbsp;&nbsp;&nbsp;* GitHub

### Tools

&nbsp;&nbsp;&nbsp;&nbsp;* Linux terminal

&nbsp;&nbsp;&nbsp;&nbsp;* VS Code extensions for Markdown and GitHub integration.

## Configuration Snippets

### Linux Terminal Commands

<div style="width: 100%;">
    <table style="width:100%;">
        <tr>
            <td style="width: 50%;">
                cd Downloads
            </td>
            <td style="width: 50%;">
                Navigate to the Downloads folder
            </td>
        </tr>
        <tr>
            <td style="width: 50%;">
                ls
            </td>
            <td style="width: 50%;">
                List files to confirm download
            </td>
        </tr>
        <tr>
            <td style="width: 50%;">
                sudo apt install ./code_1.103.2-175570974_amd.deb
            </td>
            <td style="width: 50%;">
                Installation of VS Code
            </td>
        </tr>
        <tr>
            <td style="width: 50%;">
                git --version
            </td>
            <td style="width: 50%;">
                Verify Git Installation
            </td>
        </tr>
        <tr>
            <td style="width: 50%;">
                sudo apt install git
            </td>
            <td style="width: 50%;">
                Install Git if not present
            </td>
        </tr>
        <tr>
            <td style="width: 50%;">
            git config --global user.name "nmckinster1-hue"
            </td>
            <td style="width: 50%;">
                Configures the author for Git
            </td>
        </tr>
        <tr>
            <td style="width: 50%;">
                git config --global user.email "nmckinster1@gmail.com"
            </td>
            <td style="width: 50%;">
                Configures the email to identify the author
            </td>
        </tr>
    </table>
</div>


### URLs

&nbsp;&nbsp;&nbsp;&nbsp;* [https://code.visualstudio.com/download](https://code.visualstudio.com/download)

### Visual Studio Code Extensions

&nbsp;&nbsp;&nbsp;&nbsp;* **GitHub Pull Requests and Issues:** Manages GitHub repositories directly in VS Code.

&nbsp;&nbsp;&nbsp;&nbsp;* **GitHub Codespaces:** Cloud-hosted development environments.

&nbsp;&nbsp;&nbsp;&nbsp;* **GitHub Copilot & Copilot Chat:** AI-assisted coding and inline chat.

&nbsp;&nbsp;&nbsp;&nbsp;* **Markdown Preview Extension Pack:** Markdown preview, formatting support, and special character handling.

## Step-by-Step Walkthrough

&nbsp;&nbsp;&nbsp;&nbsp;1. Navigated to the [VS Code download page](https://code.visualstudio.com/download) and downloaded the .deb package for Ubuntu.

&nbsp;&nbsp;&nbsp;&nbsp;2. Opened the Linux terminal using `Ctrl+Alt+T`.

&nbsp;&nbsp;&nbsp;&nbsp;3. Navigated to the Downloads folder with `cd Downloads` and verified the installer file with `ls`.

&nbsp;&nbsp;&nbsp;&nbsp;4. Installed Visual Studio Code with `sudo apt install ./code_1.103.2-1755709794_amd.deb`

&nbsp;&nbsp;&nbsp;&nbsp;5. Installed the required VS Code extensions for GitHub integration and Markdown support.

&nbsp;&nbsp;&nbsp;&nbsp;6. Tried to link and authenticate VS Code with GitHub but failed.

### Problem & Solution

<u>**Problem:**</u> I cam across a challenge where I couldn't link and authenticate Visual Studio Code and GitHub.

<u>**Solution:**</u>: In order to fix this I needed to find out why VS Code and GitHub cannot verify and authenticate properly, and fix whatever is wrong or add whatever is missing.

&nbsp;&nbsp;&nbsp;&nbsp;1. I checked to see if Git was installed on my computer using the command `git --version` to see what it would return. It returned `Command 'git' not found, but can be installed with: sudo apt install git`

&nbsp;&nbsp;&nbsp;&nbsp;2. Installed Git: `sudo apt install git`.

&nbsp;&nbsp;&nbsp;&nbsp;3. Configured Git with username and email:

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* `git config --global user.name "nmckinster1-hue"`.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* `git config --global user.email "nmckinster1@gmaill.com"`.

&nbsp;&nbsp;&nbsp;&nbsp;4. Installed the **GitHub Pull Requests and Issues** extension in VS Code.

&nbsp;&nbsp;&nbsp;&nbsp;5. Signed into GitHub and verified the correct email was linked in the account settings.

## Verification & Testing

1. Created a **Portfolio** folder on an external hard drive and linked it to a GitHub repository

2. Edited files, committed changes, and synced with GitHub to verify repository functionality.

3. Repeated edits and commits to ensure consistent syncing and data integrity

## Lessons Learned/Best Practices

1. Alwaays verify system dependencies before installation to prevent errors.

2. Git and GitHub configuration require careful setup to ensure proper authentication.

3. Markdown documentation provides a professional and reproducible workflow for technical work.

4. Systematic testing and verification are essential for confirming successful setup and troubleshooting.

5. Setting up tools with extensions and integrations improves productivity and supports knowledge sharing.