# Installing VS Code and Linking GitHub


## Project Overview

### Project Goal

&nbsp;&nbsp;&nbsp;&nbsp;The goal of this projectt was to install and configure **Visual Studio Code on Ubuntu** to doocument labs and projects for my portfolio using Markdown.

#### Objectives Included:
&nbsp;&nbsp;&nbsp;&nbsp;* Learning to install and manage applications via the Linux terminal.

&nbsp;&nbsp;&nbsp;&nbsp;* Creating professional, well-formatted docuumentation to enhance a technical protfolio.

&nbsp;&nbsp;&nbsp;&nbsp;* Developing familiarity with Linux file systems and software management in preparation for IT support tasks.

&nbsp;&nbsp;&nbsp;&nbsp;* Practicing troubleshooting and problem-solving for real-world technical issues.


## Project Outcome

Successfully establishhed a fully functional documentation environment with version control. Demonstrated:

&nbsp;&nbsp;&nbsp;&nbsp;* Software installation and configuration via terminal.

&nbsp;&nbsp;&nbsp;&nbsp;* Git/GitHub setup, authentication, and repository management.

&nbsp;&nbsp;&nbsp;&nbsp;* Problem-solving and troubleshhooting of installation and authentication issues.

&nbsp;&nbsp;&nbsp;&nbsp;* Creation of professional Markdown documention to support workflow and knowledge sharing.


## Key Skill Demonstrated

&nbsp;&nbsp;&nbsp;&nbsp;* Linux system administration software installation, file navigation, and dependency troubleshooting

&nbsp;&nbsp;&nbsp;&nbsp;* Git/GitHub configuration, repository management, and version control.

&nbsp;&nbsp;&nbsp;&nbsp;* Troubleshooting authentication and dependency issues (Git and Gnome Keyring).

&nbsp;&nbsp;&nbsp;&nbsp;* Technical documentation using Markdown for reproducible workflows.

&nbsp;&nbsp;&nbsp;&nbsp;* Verification and testing to ensure system functionality and data integrity.

&nbsp;&nbsp;&nbsp;&nbsp;* Knowledge sharing and workflow standardization.


## Technologies Used

### Hardware

&nbsp;&nbsp;&nbsp;&nbsp;* Alienware m15 r3 laptop

&nbsp;&nbsp;&nbsp;&nbsp;* Encrypted 2TB Seagatee HDD formatted in ext4

### Software

&nbsp;&nbsp;&nbsp;&nbsp;* Ubuntu 24.04.3 LTS

&nbsp;&nbsp;&nbsp;&nbsp;* Visual Studio Code

&nbsp;&nbsp;&nbsp;&nbsp;* Git

&nbsp;&nbsp;&nbsp;&nbsp;* GitHub

&nbsp;&nbsp;&nbsp;&nbsp;* Gnome Keyring & Passwords/Keyrings utility

### Tools

&nbsp;&nbsp;&nbsp;&nbsp;* Linux terminal

&nbsp;&nbsp;&nbsp;&nbsp;* VS Code extension for Markdown and GitHub integration


## URLs

&nbsp;&nbsp;&nbsp;&nbsp;* [Visual Studio Code Download](https://code.visualstudio.com/download)

&nbsp;&nbsp;&nbsp;&nbsp;* [Microsoft GPG Key Download](https://packages.microsoft.com/keys/)

&nbsp;&nbsp;&nbsp;&nbsp;* [Microsoft Ubuntu Repository Config](https://packages.microsoft.com/config/ubuntu/24.04/)


## Visual Studo Code Extensions

&nbsp;&nbsp;&nbsp;&nbsp;* **GitHub Pull Requests and Issues** - Manage GitHub repositories directly in VS Code.

&nbsp;&nbsp;&nbsp;&nbsp;* **GitHub Codespaces** - Cloud-hosted development environments.

&nbsp;&nbsp;&nbsp;&nbsp;* **GitHub Copilot & Copilot Chat** - AI-assisted coding and inline chat.

&nbsp;&nbsp;&nbsp;&nbsp;* **Markdown Preview Extension Pack** - Markdown preview, formatting support, and special character handling.


## Linux Terminal Commands (with Descriptions)

<table style="width:100%;">
    <tr>
        <td style="width:50%;">
            <b>Command</b>
        </td>
        <td style="width:50%;">
            <b>Description</b>
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            cd Downloads
        </td>
        <td style="width:50%;">
            Navigate to the Downloads folder where installation files are saved.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            ls
        </td>
        <td>
            List all files in tthe current directory to confirm the installer is present.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            sudo apt-get-update
        </td>
        <td style="width:50%;">
            Update the local package list to ensure all repositories and software soureces are current.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            sudo apt-get install wget gpg
        </td>
        <td style="width:50%;">
            Install wget (file downloader) and gpg (for cryptographic key management).
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            sudo dpkg -i packages-microsoft-prod.deb
        </td>
        <td style="width:50%;">
            Install Microsoft repository package to enable VS Code installation.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            sudo apt install ./code_1.104.0-1757488003_amd64.deb
        </td>
        <td style="width:50%;">
            Install Visual Studio Code from the downloaded Debian package.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            git --version
        </td>
        <td style="width:50%;">
            Check if Git installed and display its version.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            sudo apt install git
        </td>
        <td style="width:50%;">
            Install Git if it is not already installed.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            git config --global user.name "nmckinster1-hue"
        </td>
        <td style="width:50%;">
            Configure Git with your username for commit identification.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            git config --global user.email "nmckinster1@gmail.com"
        </td>
        <td style="width:50%;">
            Configure Git with your email for commit identification.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            ps aux | grep gnome-keyring
        </td>
        <td style="width:50%;">
            Checks whether the <pre><code>gnome-keyring</pre></code> process is currently running
        </td>
    </tr>
<table>