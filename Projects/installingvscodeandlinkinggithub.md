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
            Checks whether the <code>gnome-keyring</code> process is currently running
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            git add
        </td>
        <td style="width:50%;">
            Stage all changes for commit to the repository.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            git commit -m "Initial commit"
        </td>
        <td style="width:50%;">
            Commit staged changes with a message.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            git push origin main
        </td>
        <td style="width:50%;">
            Push commits from local repository to the GitHub repository.
        </td>
    </tr>
<table>



## Step-by-Step Walkthrouogh (with Commands)
1. Download Microsoft GPG key

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Downloaded <code>microsoft.asc</code> for package verification.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Verified the file in Downloads:

```
    bash

    cd Downloads
    ls
```

2. Install Microsoft repository package

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Downloaded and installed `packages-microsoft-prod.deb`:

```
    bash

    sudo dpkg -i packages-microsoft-prod.deb
    sudo apt-get update
    sudo apt-get install wget gpg
```

3. Download and install Visual Studio Code

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Installed VS Code from the Debian package:

```
    bash

    sudo apt install ./code_1_104.0-1757488003_amd64.deb
```

4. Install VS Code extensions

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Installed GitHub Pull Requeests and Issues, GitHub Codespaces, Markdown Preview Extension Pack

5. Verify Git installation

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Checked if Git was installed:

```
    bash

    git --version
```

6. Install Git and configure

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Iinstalled Git and configured username/email:

```
    bash

    sudo apt install git
    git config --global user.name "nmckinster1-hue"
    git config --global user.email "nmckinster1@gmail.com"
```

7. Attempt GitHub authentication in VS Code

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Checked Gnome Keyring:

```
    bash

    pa aux | grep gnome-keyring
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Set keyring password to match desktop login via "Passwords and Keyrings" utility for automatic authentication.

8. Verify GitHub repository connectivity

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Created Protfolio folder and linked to GitHub through VS Code.

## Problem & Solution

**Problem:** Could not link and authenticate Visual Studio Code with GitHub.

**Solution**:

&nbsp;&nbsp;&nbsp;&nbsp;* Verified Git installation (`git --version`).

&nbsp;&nbsp;&nbsp;&nbsp;* Installed Giit and configured username/email.

&nbsp;&nbsp;&nbsp;&nbsp;* Installed GitHub Pull Requeests and Issues extension.

&nbsp;&nbsp;&nbsp;&nbsp;* Confirmed email linked correctly in GitHub.

&nbsp;&nbsp;&nbsp;&nbsp;* Verified Gnome Keyring was running (`ps aux | grep gnome-keyring`).

&nbsp;&nbsp;&nbsp;&nbsp;* Set keyring password same as desktop login to allow VS Code to unlock automatically.

## Verification & Testing

&nbsp;&nbsp;&nbsp;&nbsp;* Created Portfolio folder on external hard drive and linked it to GitHub.

&nbsp;&nbsp;&nbsp;&nbsp;* Edited filees, committed changes, and synced to verify functionality.

&nbsp;&nbsp;&nbsp;&nbsp;* Repeated edits and commits to ensure data integrity.

## Lessons Learned/Best Practices

&nbsp;&nbsp;&nbsp;&nbsp;* Verify system dependencies before installation to prevent errors.

&nbsp;&nbsp;&nbsp;&nbsp;* Git and GitHub configuration require careful setupp.

&nbsp;&nbsp;&nbsp;&nbsp;* Markdown documentation provides reproducible workflows.

&nbsp;&nbsp;&nbsp;&nbsp;* Systematic testing and verification are essential.

&nbsp;&nbsp;&nbsp;&nbsp;* Extensions and integrations improve productivity and knowledge sharing.

&nbsp;&nbsp;&nbsp;&nbsp;* Authentication system (Gnome Keyring) must be configured to allow secure access.