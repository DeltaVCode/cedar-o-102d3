# Lab: Virtualization of Windows OS

## Overview

Now that Virtualbox is loaded onto your Ubuntu-based lab PC, you'll be able to create a "virtual machine" of any operating system, assuming you can get your hands on the corresponding .iso installer or a premade .ova Virtualbox file. There are legal and ethical considerations to make when seeking out such files. For example, Apple forbids the virtualization of its macOS on non-Apple hardware. For this class, your first VM will be Windows 10, the most common enterprise business desktop used today.

## Objectives

- Create a Windows 10 VM in Virtualbox using the .iso installation method.
- Backup the working Windows 10 VM using Virtualbox's save state and .ova export features.
- Determine a consistent disk storage solution for .ova files.

## Resources

- [Windows Media Creation Tool](https://www.microsoft.com/en-us/software-download/windows10){:target="_blank"}

> For our purposes in class, we will not be activating our installations of Windows. If you have access to activation keys for commercial systems we use in class, feel free to apply them at your discretion.

## Tasks

### Part 1: Windows 10 ISO

In order to create a VM of Windows 10, you'll need an ISO of the installer disc image. Your instructor will provide you either the ISO file or you may use the Windows Media Creation Tool to generate a ISO file yourself.

- Transfer it to your lab PC using SCP or whatever means are at your disposal.

> If the operating systems you're working with do not support Windows 10 Media Creation Tool, contact your instructor.

### Part 2: Configuring your VM

Now that your VM is created, you'll want to review its resource allocation. These resources are virtual representations of the physical components you cataloged in Class 1.

- Adjust various parameters to optimize performance of the VM.
  - Adjust RAM to 8 GB.
  - Adjust CPU the utilize all four cores.
  - Allocate the maximum possible video memory.
  - Include screenshots of parameter adjustments. 

- Set the network adapter to bridge mode.

### Part 3: Windows 10 Setup Wizard

Complete the setup wizard that runs the first time you launch the VM.
  - Do not create a Microsoft account as the wizard prompts you to. Instead, create a local user account.
  - When you have access to the Windows 10 desktop, this part is complete.

## Part 4: Virtualbox Save State and Export/Import

Virtualbox includes a "save state" feature. We can use this to establish a "baseline" image of your Windows 10 VM.

- Save a VM state.
  - Make a change to the VM. For example, create a file on the desktop.
  - Restore the VM to the state you saved.
  - Describe whether the VM state was restored as expected. How might this be useful later on?
- Export a .ova file of your Windows 10 VM. 
  - Put this file somewhere spacious and ideally separate from the SSD of the lab PC. For example, a home NAS file server is ideal for .ova storage.

## Stretch Goals (Optional Objectives)

Download the premade [Microsoft Windows 10 Edge Legacy .ova](https://developer.microsoft.com/en-us/microsoft-edge/tools/vms/){:target="_blank"}.
- Import the .ova into Virtualbox as a new VM.
- Document in your submission how this process differs from the .iso installatin process you performed. What are the pros/cons of each method?
- Feel free to delete this VM and store the .ova file. We won't be using this one in class.

## Submission Instructions

1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-102n1: Reading 01` or `seattle-ops-102d33: Lab 04`.
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can view".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
