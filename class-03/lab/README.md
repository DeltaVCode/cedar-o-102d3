# Lab: Startup Sequences and BIOS

## Overview

Before a computer even launches into its OS (operating system), it performs a sequence of activities behind the scenes immediately after you press the power button. These activities include select a boot device based on a prescribed boot sequence. These low-level computing activities take place in the computer's BIOS. Settings such as motherboard or component voltage allocation, overclocking, boot sequence, system time, and more can be found in the BIOS menu system. Because virtualized computers can have multiple bootable drives and accept external media in the form of .iso disk images, it will be valuable for you to gain experience manipulating a physical computer's BIOS and boot sequence within it.

## Objectives

Today you will be performing the following operations on your lab computer's Basic Input/Output System (BIOS): 
- Document detailed system information using BIOS.
- Clear the CMOS using BIOS.
- Change boot sequence using BIOS.
- Secure BIOS with an administrator password.
- Access the event log in BIOS.

## Tasks

### Part 1: System Information

Create a new Google Doc for this lab per Submission Instructions below.
- Log into your lab computer’s BIOS. 
  > Changes made to BIOS do not apply until you select "Exit Saving Changes."
- Lookup and provide the following system spec information, and describe where you found this information for each item:
  - Motherboard 
  - CPU
  - Amount of RAM installed
  - BIOS firmware version
- Lookup the BIOS menu that allows you to disable USB ports. Include a photo.

### Part 2: Clearing the CMOS

In this part of the lab, you will attempt to clear the CMOS. Clearing the CMOS will revert BIOS back to its factory default settings. It may also take some time for the CMOS eletrically discharge. Take care to perform Part 2 before Part 3-4 in this lab assignment, to avoid inadvertently clearing your desired settings.
- Note the System Date and System Time on the Main menu. Shut down the computer.
- As always, don't touch PC internals until you've confirmed power cable is disconnected, PSU set to 0, and your body is free of static charge.
- Carefully remove the CR2032 battery from the motherboard. Wait five minutes.
- Reinsert the CR2032 battery. Plug in power, switch power to 1, and boot the PC. Go back into BIOS (F2).
- Include a photo of the warning message and altered time setting.
- Describe the process you used to clear the CMOS. Describe what all changed, and explain why it changed.
- Adjust System Date and Time to correct values.

### Part 3: Boot Sequence

Change boot order to prioritize USB over HDD. 
- What boot mode is your BIOS currently set to use, UEFI or Legacy? Include a photo.
- Configure USB flash drive to take priority over the hard drive. We'll need this to install Windows 10 via USB later.
- Include a photo of the boot order/priority menu. 
- Describe the steps you took and any issues you encountered.

> Typically, external media like DVD-ROM and USB will take precedence over the internal hard disk in order to facilitate smooth installation of operating systems using external media. When the installation process is complete and you're about to reboot into the HDD, you'll typically remove the external media at that stage so the boot sequence doesn't re-launch the installer off the external media.

### Part 4: Securing BIOS

If you're distributing physical computers to a workforce as company-administered property, consider securing the BIOS with an administrator password.
- Once configured, include a photo of the BIOS prompting you for a password.
- Describe the procedure you used to configure a password.
- Remove the password requirement.
- On the Security screen, make sure Intel Virtualization Technology is ENABLED and Intel VT for Directed I/O (VT-d) is ENABLED.

### Part 5: Event Log

Lookup the Event Log in BIOS. 
- Include a photo of the Event Log. 
- Describe what the purpose of this Event Log is.
- Recognize any entries?
  
## Stretch Goals (Optional Objectives): 

Pursue these optional objectives if you are an advanced user or have remaining lab time.

### Additional System Information

- Lookup and provide the CPU Fan Speed in RPM and the Processor Temperature in Celsius. Describe where you found this information.
- Lookup and provide the configuration setting of the Integrated Graphics Device. Explain what this means.
- Navigate to the SATA Drives menu and include a photo showing all devices attached via SATA.

### Flash the BIOS Firmware

If you're feeling confident thus far, check to see if there is a new version of your BIOS firmware and download it. Update the firmware via BIOS or whatever method is prescribed by the motherboard vendor.

- There are many ways to update BIOS. Choose one method and proceed.
- Include photos of all the steps you took. Describe any challenges or problems you encountered.

> Note that if a firmware upgrade goes wrong, such as a power interruption during the upgrade process, you run the risk of "bricking" the device (rendering the hardware permanently inoperable). This makes firmware upgrades inherently riskier than software application or OS upgrades.

## Submission Instructions

1. Name the document according to your course code and assignment.
   - i.e. `c-rapids-ops-102n3: Reading 01` or `c-rapids-ops-102d3: Lab 04`.
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can view".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
