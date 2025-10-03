# Virtual Machine Creation and Installing Windows in VM

## Project Overview

### Project Goal

&nbsp;&nbsp;&nbsp;&nbsp;The goal of this project is to successfully establish a fully functional Virtual Machine (VM) on a Linux host system and install Windows 10 as the guest operating system.

### Objectives Included:

&nbsp;&nbsp;&nbsp;&nbsp;* Successfully install and configure virtual machine software (Oracle VirtualBox) on Ubuntu 20.04.3 LTS.

&nbsp;&nbsp;&nbsp;&nbsp;* Properly create and configure a new virtual machine for Windows 10, including allocation of storage, memory, and network resources.

&nbsp;&nbsp;&nbsp;&nbsp;* Learn how to configure the Linux kernel and related system files to allow full permissions for NTFS formatted drives for storage and VM use.

&nbsp;&nbsp;&nbsp;&nbsp;* Understand user management in Linux to allow proper access to VirtualBox features, such as USB pass-through and external drive mounting.

&nbsp;&nbsp;&nbsp;&nbsp;* Understand user management in Linux to allow proper access to VirtualBox features, such as USB pass-through and external drive mounting.

## Project Outcome

&nbsp;&nbsp;&nbsp;&nbsp;* Successfully installed Oracle VirtualBox on Ubuntu 24.04.3 LTS.

&nbsp;&nbsp;&nbsp;&nbsp;* Created a Windows 10 virtual machine stored on an external Seagate 2TB NTFS hard drive.

&nbsp;&nbsp;&nbsp;&nbsp;* Configured Linux system files to provide full read/write permissions to the NTFS external drive.

&nbsp;&nbsp;&nbsp;&nbsp;* Resolved system conflicts between VirtualBox and the built-in KVM virtualization module.

&nbsp;&nbsp;&nbsp;&nbsp;* Gained a deeper understanding of Linux kernel configuration, file systems, and virtualization best practices.

## Key Skills Demonstrated

&nbsp;&nbsp;&nbsp;&nbsp;* Linux system administration and terminal proficiency.

&nbsp;&nbsp;&nbsp;&nbsp;* User and group management in Linux to allow proper VirtualBox permissions.

&nbsp;&nbsp;&nbsp;&nbsp;* Troubleshooting system conflicts between different virtualization technologies.

&nbsp;&nbsp;&nbsp;&nbsp;* Editing and configuring system files like `/etc/fstab` for permanent drive mounting and permission management.

&nbsp;&nbsp;&nbsp;&nbsp;* Creating and configuring virtual machines, including ISO installation, virtual disk creation, and external drive usage.

## Technologies Used

### Hardware

&nbsp;&nbsp;&nbsp;&nbsp;* Alienware m15 r3 laptop

&nbsp;&nbsp;&nbsp;&nbsp;* Encrypted 2TB Seagate HDD formatted in NTFS for storing VMs.

&nbsp;&nbsp;&nbsp;&nbsp;* SandDisk Ultra USB 3.0 64GB configured with Ventoy for ISO booting.

### Software

&nbsp;&nbsp;&nbsp;&nbsp;* Ubuntu 24.04.3 LTS - Host operating system.

&nbsp;&nbsp;&nbsp;&nbsp;* Windows 10 - Guest operating system for virtual machine.

&nbsp;&nbsp;&nbsp;&nbsp;* BIOS/UEFI - Used for base system configuration and enabling virtualization.

&nbsp;&nbsp;&nbsp;&nbsp;* Oracle VirtualBox - Virtual machine software.

&nbsp;&nbsp;&nbsp;&nbsp;* Users and Groups - Linux application for managing user accounts and permissions.

### Tools

&nbsp;&nbsp;&nbsp;&nbsp;* Built-in Ubuntu Disks utility for managing drives.

&nbsp;&nbsp;&nbsp;&nbsp;* Linux terminal for commands and file editing.

&nbsp;&nbsp;&nbsp;&nbsp;* Users and Groups application for group management and permissions.

### URLs

&nbsp;&nbsp;&nbsp;&nbsp;* [Oracle VirtualBox Download for Linux](https://www.virtualbox.org/wiki/Linux_Downloads)


## Linux Terminal Commands (with Descriptions)

<table style="width:100%;">
    <tr>
        <td style="width:50%;">
            <code>sudo gpg --dearmor --yes --output /usr/share/keyrings/oracle-virtualbox-2016.gpg oracle_vbox_2016.asc</code>
        </td>
        <td style="width:50%;">
            Imports the GPG key for verifying the VirtualBox installer file.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            <code>lsmod | grep kvm</code>
        </td>
        <td style="width:50%;">
            Checks if any instances of the Kernel Virtual Machine (KVM) are active.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            <code>sudo nano /etc/modprobe.d/blacklist-kvm.conf</code>
        </td>
        <td style="width:50%;">
            Opens the KVM blacklist file to prevent KVM modules from loading at boot.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            <code>blacklist kvm, blacklist kvm_intel, blacklist kvm_amd</code>
        </td>
        <td style="width:50%;">
            Lines added to disable KVM modules.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            <code>sudo cp /etc/fstab /etc/fstab.bak</code>
        </td>
        <td style="width:50%;">
            Creates a backup of the fstab file before making modifications.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            <code>sudo blkid</code>
        </td>
        <td style="width:50%;">
            Lists all block devices and their attributes, including UUIDs.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            <code>mkdir windowsdrivetwotb</code>
        </td>
        <td style="width:50%;">
            Creates a directory to mount the external Seagate NTFS drive.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            <code>sudo nano /etc/fstab</code>
        </td>
        <td style="width:50%;">
            Opens the fstab file to configure automatic mounting of drives.
        </td>
    </tr>
    <tr>
        <td style="width:50%;">
            <code>UUID=C27EBA6C001C5412 /home/nohvas/windowsdrivefivetb ntfs-3g defaults,nofail,uid=1000,gid=1000,dmask=000,fmask=111 0 0</code>
        </td>
        <td style="width:50%;">
            Configuration added to fstab for full NTFS drive access.
        </td>
    </tr>
</table>

## Step-by-Step Walk-through (with Commands)

1. **Enable Virtualization in BIOS/UEFI (if applicable):**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Restart the computer and press the configured BIOS/UEFI key repeatedly during startup.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Navigate to advanced settings and enable the Intel Virtualization Technology (VMX). For AMD processors, enable AMDV. Save changes and restart the computer.

2. **Prepare External Hard Drive:**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Connect the Seagate HDD to the computer.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Backup fstab:

```
    bash

    sudo cp /etc/fstab /etc/fstab.bak
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Find the UUID:

```
    bash

    sudo blkid
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Create mount directory 

```
    bash

    mkdir windowsdrivetwotb
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Edit fstab for permanent mounting with full permissions:

```
    bash

    sudo nano /etc/fstab
```
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Add:

```
    ini

    UUID=C27EBA6C001C5412 /home/nohvas/windowsdrivefivetb ntfs-3g defaults,nofail,uid=1000,gid=1000,dmask=000,fmask=111 0 0
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Test mount:

```
    bash

    sudo mount -a
```

3. **Install Oracle VirtualBox:**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Download the proper VirtualBox installer for Ubuntu from the official website.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Installs and verifies the installation of Oracle Virtual Box

```
    bash

    wget -O- https://www.virtualbox.org/download/oracle_vbox_2016.asc | sudo gpg --yes --output /usr/share/keyrings/oracle-virtualbox-2016.gpg --dearmor

```

4. **Deactivate KVM to Avoid Conflicts:**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Check if KVM is running:

```
    bash

    lsmod | grep kvm
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Blacklist KVM modules:

```
    bash

    sudo nano /etc/modprobe.d/blacklist-kvm.conf
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;Add:

```
    bash

    blacklist kvm
    blacklist kvm_intel
    blacklist kvm_amd
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Regenerate initramfs:

```
    bash

    sudo update-initramfs -u
```

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Reboot the system.

5. **Configure VirtualBox User Permissions:**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Open "Users and Groups" from Ubuntu App Center.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Navigate to "Manage Groups", select "vboxusers", add your account, and log out/in.



6. **Create the Windows 10 VM:**

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Open VirtualBox, create a new machine, name it, and select external Seagate drive as the VM location.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Choose Windows 10 ISO from Ventoy USB drive.

&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;* Allocate 50GB for the virtual hard disk and configure RAM and CPU as needed.

## Problem & Solution

**Problem:** VirtualBox wouldn't run on Ubuntu.

**Solution:** KVM, the built-in virtualization for Linux, was running. Disabled KVM by blacklisting modules and regenerating initramfs to allow VirtualBox to operate.

&nbsp;

**Problem:** NTFS hard drive would not mount correctly.

**Solution:** Edited `/etc/fstab` to permanently mount the drive with full read/write permissions.

&nbsp;

**Problem:** VirtualBox could not access USB devices or external drives.

**Solution:** Added user to "vboxusers" group using "Users and Groups" application to allow proper USB and drive access.

## Verification & Testing

&nbsp;&nbsp;&nbsp;&nbsp;* Verified VirtualBox runs correctly and can access external drives.

&nbsp;&nbsp;&nbsp;&nbsp;* Successfully installed Windows 10 on the VM stored on the Seagate 2TB NTFS drive.

&nbsp;&nbsp;&nbsp;&nbsp;* Confirmed full read/write permissions on external drive from both Ubuntu and VirtualBox.

&nbsp;&nbsp;&nbsp;&nbsp; Ran test programs within Windows 10 VM to ensure system stability.

## Lessons Learned/Best Practices

&nbsp;&nbsp;&nbsp;&nbsp;* Always check for conflicts in virtualization modules when installing VirtualBox on Linux.

&nbsp;&nbsp;&nbsp;&nbsp;* Backup important system files like `/etc/fstab` before making modifications.

&nbsp;&nbsp;&nbsp;&nbsp;* Use dedicated tools like "Users and Groups" to simplify permissions management in Linux.

&nbsp;&nbsp;&nbsp;&nbsp;* Test mounting external drives and permissions before using them for critical VM damage.

&nbsp;&nbsp;&nbsp;&nbsp;* Properly plan VM storage location and allocation to optimize performance.
