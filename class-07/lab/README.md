# Lab: Network Connectivity 

## Overview

To use the Ubuntu PC as a true dedicated virtualization server, we'll need to next establish reliable network connectivity to it from our personal computer. To do this, we'll need to apply networking concepts such as IP addressing, ports, and MAC addressing. We'll also need to install some additional software on the Ubuntu box to facilitate these network protocols. After configuring and testing remote connectivity to your Ubuntu virtualization server, you'll no longer need to keep it around your desktop workspace and can relocate to a closet or garage with network access. Think of it as your "private cloud," but without the costs!

> The operations depicted in this lab are quite common in the world of networking and systems administration. Most servers are reserved or static IPs, and in this cloud-driven market we're seeing heavy usage of remote desktop solutions such as Microsoft RDP (Remote Desktop Protocol).

## Objectives

- On your home network's DHCP server, assign a reserved IP address to the Ubuntu PC network adapter's MAC.
- Establish SSH connectivity from your personal system to the Ubuntu PC.
- Establish GUI desktop remote connectivity from your personal system to the Ubuntu PC.
- Install and use a GUI SCP application.
- Perform a SCP file transfer via the GUI SCP application.

## Resources
- [DHCP Reservation](https://homenetworkadmin.com/dhcp-reservation/){:target="_blank"} 
- [Ubuntu RDP access from Windows 10](https://linuxconfig.org/ubuntu-20-04-remote-desktop-access-from-windows-10){:target="_blank"} 
- [Ubuntu VNC access from macOS](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-vnc-on-ubuntu-20-04){:target="_blank"} 

## Tasks

Today's tasks will vary depending on your home's network setup, as well as the OS of your personal system. Be extra careful when manipulating the configuration of your network appliances, as this can affect your overall internet connectivity. 

### Part 1: IP Address Reservation

First, you'll need to reserve a fixed IP address on your home DHCP server for the Ubuntu PC's network adapter. If you're new to administering DHCP on your home modem/router appliance, pump the brakes and take it slow! If you neglect to properly do this step, the IP address of your Ubuntu PC may change, thus affecting our ability to connect to it. 
- Identify the MAC address of the Ubuntu PC via terminal.
- Access your DHCP server's (router's) administrative interface and assign a reserved IP to the Ubuntu PC's network adapter MAC address.
- Reboot the Ubuntu PC if necessary, to obtain the reserved IP.

> Ask your instructor for help if you're uncertain at this stage of the lab. Everyone's home network is different, and this is a very perilous stage of the lab to make a mistake.

### Part 2: SSH Connectivity

SSH lets us access the command line of a remote computer by authenticating into it using a local user's password.
- Install an OpenSSH server on your Ubuntu PC using the APT package manager.
- Create any necessary firewall exceptions to ensure port 22 is open.
- Next, download and install [Git Bash](https://git-scm.com/downloads) on your personal computer. We'll be using this as our "shell" program to SSH into the lab computer.
- SSH into your Ubuntu box from your personal computer's Git Bash. Take a screenshot of yourself issuing commands to the lab computer from your personal computer via SSH. Be sure to try these commands:
  - `whoami`
  - `ls`
  - `pwd`
  - `ip a`
  - `sudo apt update`
  - `sudo reboot now`
  - `sudo shutdown now`

> Remember, your personal computer must be on the same LAN subnet as the Ubuntu computer. Their gateway and subnet mask should be identical. If not, check your home network.

### Part 3: XRDP (or VNC) Connectivity

Windows 10 users, follow this instruction set.

- Perform the [following steps](https://linuxconfig.org/ubuntu-20-04-remote-desktop-access-from-windows-10){:target="_blank"} to install an RDP server on your Ubuntu box.
  - Always remember to update the apt package manager with `sudo apt update` before installing any new packages.
  - Install the RDP server with `sudo apt install xrdp`.
  - Allow the RDP server to initialize on startup with `sudo systemctl enable --now xrdp`.
  - Create a firewall exception for port 3389 on this system with `sudo ufw allow from any to any port 3389 proto tcp`.
- Give the computer a reboot, then wander over to your host PC and remote in using RDP protocol. Be sure to keep the domain prefix off of the username, and manually specify the username. Do not save the RDP file.
- You'll need to use the `xorg` protocol and provide your Ubuntu username and password. 
- Grab a screenshot of your successful RDP session and include it in your submission.

Alternatively, macOS users should follow [this instruction set](https://www.digitalocean.com/community/tutorials/how-to-install-and-configure-vnc-on-ubuntu-20-04){:target="_blank"} to install a VNC server on the Ubuntu box.

Once you have established remote desktop connectivity, customize the interface to your liking by assigning common applications to favorites, such as Terminal and Files. Personalize this lab computer by adding a cool wallpaper and change the colors on your Terminal app while you're at it. Grab a screenshot of your customized homme lab desktop.

> Once you have established SSH and remote desktop connectivity to the Ubuntu PC from your host system, feel free to relocate the Ubuntu PC somewhere more discreet, like a closet or garage with network access. Keep the monitor and keyboard plugged into it for those occasional instances where it malfunctions.

### Part 4: Secure Copy Protocol (SCP)

Throughout your home lab journey, you'll have occasion to transfer files from your main personal computer to the lab system. Windows users can use WinSCP to perform this task.

Windows users can utilize [WinSCP](https://winscp.net/eng/index.php) to transfer a file from your personal computer to your lab computer. Take a screenshot of what you did and explain how it worked.

Alternatively, macOS users should try [SCP Client](https://apps.apple.com/us/app/scp-client/id1368363210) or an equivalent GUI SCP app to transfer a file from the personal computer to the lab computer. Take a screenshot of what you did and explain how it worked.

## Stretch Goals (Optional Objectives)

- Perform a SCP file transfer using only the command line/Git Bash.

## Submission Instructions

1. Name the document according to your course code and assignment.
   - i.e. `c-rapids-ops-102n3: Reading 01` or `c-rapis-ops-102d3: Lab 04`.
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can view".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
