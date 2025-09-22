# Creating a Tech Swiss Army Knife

## Project Overview

### Project Goal

&nbsp;&nbsp;&nbsp;&nbsp;To make a single tool that can be used in order to install nearly all commonly used operating systems, as well as a robust toolkit for system repair, data recovery and virus detection and removal.

### Project Outcome

&nbsp;&nbsp;&nbsp;&nbsp;* Successfully configured the USB to hold multiple ISOs and tools for repair, recovery, and benchmarking.

&nbsp;&nbsp;&nbsp;&nbsp;* Made a robust multitool that includes many repair and recovery tools and multiple OSs.

&nbsp;&nbsp;&nbsp;&nbsp;* Correctly configured my file management system to be able to extract compressed .rar, and .7z files.

## Technologies Used

### Hardware

&nbsp;&nbsp;&nbsp;&nbsp;* Alienware m15 r3 laptop.

&nbsp;&nbsp;&nbsp;&nbsp;* Unencrypted SanDisk Ultra USB 3.0 64GB.

### Software

&nbsp;&nbsp;&nbsp;&nbsp;* **General Software:**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Ubuntu 24.04.3 LTS - My home OS.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Ventoy software - Makes it possible to have multiple ISOs and recovery tools.

&nbsp;&nbsp;&nbsp;&nbsp;* **ISOs:**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Windows 10 - Windows OS.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Windows 11 - Windows OS.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Ubuntu 24.04.3 LTS - Linux OS.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Linux Mint Cinnamon - Linux OS.

&nbsp;&nbsp;&nbsp;&nbsp;* **Recovery Tools:**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Rescuezilla - Used for disk imaging and cloning.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* SystemRescue - Used for Linux based system repair, recovering data, and fixing data partitions.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Hiren's Boot CD - Used for Windows OS repair, recovering data, partitioning drives, and removing malware.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* GParted - Used for Linux with advanced partition management and disk formatting.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Clonezilla - Powerful command-line desk imaging and cloning utility for backups, deployment, and recovery.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Ultimate Boot CD (UBCD) - A bootable toolkit used for diagnosing hardware, repairing systems, recovering and cloning data, benchmarking performance, and running legacy DOS utilities.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* MediCat - Windows based toolkit with system repair, malware removal, data recovery, data partitioning, password resetting, and portable diagnostic tools.

### Tools

&nbsp;&nbsp;&nbsp;&nbsp;* Linux Terminal.

&nbsp;&nbsp;&nbsp;&nbsp;* Ubuntu disks application.

&nbsp;&nbsp;&nbsp;&nbsp;* File Manager and installed file manager function.

## Configuration Snippets

### Linux Terminal Commands

<table style="width:100%;">
    <tr>
        <td style="width:50%;">
            sudo apt install exfat-fuse exfatprogs
        </td>
        <td style="width:50%;">
            Allows formatting disks to exFAT on Linux
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            cd Downloads
        </td>
        <td style="width:50%;">
            Navigates to the "Downloads" folder on my home drive
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            tar -xvf ventoy-1.1.07-linux.tar.gz
        </td>
        <td style="width:50%;">
            Extracts the files from the compressed Ventoy download archive.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            cd ventoy-1.1.07
        </td>
        <td style="width:50%;">
            Navigates to the Ventoy version folder.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            sudo ./Ventoy2Disk.sh -i /dev/sdx
        </td>
        <td style="width:50%;">
            Installs Ventoy onto my USB and configures it for ISO copying.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            sudo dpkg -i opera-stable_122.0.5643.17_amd64.deb
        </td>
        <td style="width:50%;">
            Installs the Opera web browser via the downloaded installation link.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            sudo apt install qbittorrent
        </td>
        <td style="width:50%;">
            Installs the qbittorrent application for Linux.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            lsblk
        </td>
        <td style="width:50%;">
            Used to view block storage on drives.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            sudo apt update
        </td>
        <td style="width:50%;">
            Updates the package list.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            7z --version
        </td>
        <td style="width:50%;">
            Verifies if the 7z package list install.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            sudo apt install p7zip-rar
        </td>
        <td style="width:50%;">
            Installs the files necessary to extract data from compressed files.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            sudo apt install file-roller unrar p7zip-full p7zip-rar
        </td>
        <td style="width:50%;">
            Adds GUI support to the files manager for extracting files.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">

        </td>
    </tr>
</table>

## URLs

&nbsp;&nbsp;&nbsp;&nbsp;* [Ventoy download](https://www.ventoy.net/en/download.html)

&nbsp;&nbsp;&nbsp;&nbsp;* [Windows 10 download](https://www.microsoft.com/en-us/software-download/windows10ISO)

&nbsp;&nbsp;&nbsp;&nbsp;* [Windows 11 download](https://www.microsoft.com/en-us/software-download/windows11)

&nbsp;&nbsp;&nbsp;&nbsp;* [Ubuntu 24.04.3 LTS download](https://ubuntu.com/download/desktop)

&nbsp;&nbsp;&nbsp;&nbsp;* [Linux Mint Cinnamon download](https://linuxmint.com/edition.php?id=322)

&nbsp;&nbsp;&nbsp;&nbsp;* [RescueZilla backup/recovery tool](https://rescuezilla.com/download)

&nbsp;&nbsp;&nbsp;&nbsp;* [SystemRescue rescue/recovery tool](https://sourceforge.net/projects/systemrescuecd/)

&nbsp;&nbsp;&nbsp;&nbsp;* 


Welcome to my portfolio!
This is where you'll find all of my projects that I have done to show you what I can do and I hope you also see my drive and passion throughout! To see them, click the the projects link above.