# Lab: Installing Virtualbox with Linux Terminal 

## Overview

In order to effectively utilize Ubuntu Linux as a virtualization server, you'll need to get comfortable using the Linux terminal. While many operations can be performed using the desktop graphical user interface (GUI), basic Linux terminal skills are generally expected of Ops professionals.

## Objectives

On your Ubuntu Linux box:
- Establish internet connectivity to your lab kit PC
- Perform an APT package manager update
- Install Git
- Run the [setup script](https://github.com/lee5378/labsetup) and monitor to completion
- Open VirtualBox Manager

## Resources

- [Linux command line for beginner](https://ubuntu.com/tutorials/command-line-for-beginners#1-overview){:target="_blank"}
- [Linux Commands for Linux Beginners](https://www.howtouselinux.com/post/linux-commands-for-linux-beginners-cheat-sheet){:target="_blank"}
- [Advanced package tool for Linux](https://www.poftut.com/what-is-apt-advanced-package-tool-for-linux/){:target="_blank"}
- [How to Install Virtualbox on Ubuntu](https://itsfoss.com/install-virtualbox-ubuntu/){:target="_blank"}

## Tasks

### Part 1: Network Connectivity

First, check that your lab PC is connected to your home network via ethernet or Wi-Fi. Then, use the Ubuntu desktop GUI to update the Ubuntu OS to the latest version.
- On the back of the lab kit PC, on its I/O shield, you'll find the ethernet port. If you need an ethernet cable, open the Linksys Router and use the included cable. Plug the cable into the back of the PC and run it to your home router/modem.
- Alternatively, try the included wi-fi adapter (antenna with USB).

### Part 2: Running the Lab Setup Script

First let's load an automated setup script to stand up the required software. Run the following:
- `sudo apt update`
- `sudo apt install git -y`
- Create a dedicated Github folder to store downloaded repos using `mkdir ~/github`.
- Change to this new folder with `cd ~/github`.
- Download the automation script with `git clone https://github.com/lee5378/labsetup.git`.
- Navigate into the newly-downloaded repository with `cd labsetup`.
- Execute the installer script with `sudo bash labsetup.sh` then answer yes to all prompts.

By the end of this lab, you'll have a fully updated Ubuntu Linux OS with Virtualbox and internet connectivity.

## Strech Goals (Optional Objectives)

Have a macOS computer at home? Find the terminal application in macOS and try some of the operations from part 1 and 2. You might be surprised at how much macOS and Ubuntu have in common.

## Submission Instructions

1. Name the document according to your course code and assignment.
   - i.e. `c-rapids-ops-102n3: Reading 01` or `c-rapis-ops-102d3: Lab 04`.
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can view".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
