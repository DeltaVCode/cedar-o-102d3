# Lecture Notes: Startup Sequence and BIOS

Use this document to add more details, flavor, hints, tricks, ideas to make lecture better. This should tie into the "Why, What, How" sections of the facilitator's README.

Consider the [README](README.md) in conjunction with the [DEMO](DEMO.md) as the single source of truth for a given class, while this document is more of the living, breathing, set of notes from all instructors as to what is historically working well.

## Topic 1: Startup Sequence and BIOS

### Key Concepts

- Malware
  - A malicious program or script designed to execute an attacker’s agenda.
- Virus
  - A malware that replicates itself.
- Boot Sector
  - A reserved sector of a disk or storage device that contains the necessary data or code used to complete the boot process of a disk or a computer.
- Boot Sector Virus
  - A virus that installs itself into the boot sector part of computer memory.

### Levels of abstraction in computing

- Physical (start 102 here - where you are now)
- Electronic transmission of binary signals
- Components in an electronics board
- Connecting hardware components
- **Basic input-output system (BIOS)**
- Operating system (OS)
- Virtualization (finish 102)
- Server
- Network
- Cloud

### Video: Prowler Boot Sector Virus

- SAY: Most of us think of Windows or MacOS graphical user interface (GUI) when it comes to operating a computer. Let’s challenge that by taking a look at a type of virus called “Prowler” that lurks in in a part of the computer called “boot sector.”
- [Video](https://youtu.be/fSL4J0zhMcY)
- Discuss
  - SAY:
    - Prowler 
      - What is different or unique about this virus? (DO: Go around the room)
      - This virus infects the master boot record. This is a part of memory that is accessed before the OS launches. Therefore, every time you start your computer, this virus will run before launching the OS like normal.
    - Key takeaway - If a virus infects a lower level system than your OS, you will need to be prepared to deal with it at this level.

### Startup Sequence

- Why might we need to know the computer startup sequence?
  - Troubleshooting a computer that is not correctly booting
  - Repairing a corrupt master boot record (MBR)
    - MBR holds partition and file system info
    - Boot loader for OS
  - Isolated a problem in the startup sequence
  - Accessing BIOS
  - Booting to the correct OS
  - Configuring dual-boot
  - Understanding what’s happening behind the scenes

### Read-only Memory (ROM)

> Be sure to compare to RAM. Same function (storing memory) but different purposes and capabilities.

Flash BIOS is less secure because it can be changed from an external source.


- What is ROM?
  - ROM stands for “read-only memory.” 
  - Hard-coded into the motherboard and cannot be altered or deleted
  - Newer devices use flash memory instead of ROM. An example of ROM is the boot sequence of a computer.
- BIOS originally stored in ROM
  - Newer BIOS use flash memory, less secure

### Startup Sequence

- What Happens When a Computer Powers On?
  - The CPU initializes, then fetches instructions from the BIOS, which is stored in the ROM in older systems (newer systems use flash BIOS). It puts these instructions into RAM for immediate use.
  - Refresh - What is RAM?
    - RAM stands for “random access memory.” RAM is a modular hardware component that is installed onto the motherboard. RAM is like a cache of memory that the computer can use to temporarily store memory it’s currently working with for more efficient processing. Examples of RAM-intensive processes include hosting a virtual machine and opening a very large spreadsheet file.
  - The BIOS starts the monitor and keyboard, and does some basic checks to make sure the computer is working properly. For example, it will look for the RAM.
  - The BIOS then starts the boot sequence. It will look for the operating system.
  - If you don’t change any of the settings, the BIOS will fetch the operating system from the hard drive and load it into the RAM.
  - The BIOS then transfers control to the operating system.”
- Watch [Future Learn: The Startup Sequence](https://www.futurelearn.com/courses/computer-systems/0/steps/53497)

### BIOS

- SAY: Next let’s take a look at the basic input/output system (BIOS). This is a low level computer system that you’ll likely never see if you’re just an everyday computer user getting work done. However, as an ops professional you’ll want to familiarize with BIOS from the perspective of computer support and configuration.

- What is the BIOS?
  - Basic Input-Output System (BIOS)
    - Low level system; first thing to load on powerup
    - Initializes hardware before handing off to OS
    - Boot modes
      - UEFI
      - Legacy
    - Boot order/priority

  - SAY: BIOS is a low level computer system and is the first system to load on power up. You won’t even see BIOS unless you press a special prompt to access it. The bootup screen will show you (briefly) what to press in order to access BIOS. Usually it is keystroke DEL or F2, F10, something like that.

  - BIOS initializes all the computer hardware before handing control over to the operating system. Therefore, it is critical that your BIOS knows where your OS is and boots into it for you. This is configured in the Boot Sequence or Boot Priority menu of BIOS.

  - There are two modes you’ll see in bootup: UEFI (most modern) and Legacy. Oftentimes compatibility issues during bootup can be resolved by toggling between UEFI and Legacy boot modes.

### CMOS

- Complementary metal-oxide-semiconductor (CMOS)
  - CMOS holds BIOS configuration
    - Type of disk drives installed
    - System clock date & time
    - Boot sequence
  - Reset CMOS memory by removing the CMOS battery to “clear” the CMOS, then reinserting it.

- SAY: Some of the BIOS configuration settings are stored in the complementary metal-oxide-semiconductor (CMOS) chip. The CMOS chip retains memory by drawing power from the CMOS battery embedded into the motherboard. This is usually a round, flat CR2032 Lithium battery.
- Therefore by removing the CMOS battery you should be able to clear the BIOS time & date configuration because CMOS is volatile memory. Motherboards vary between models, so there may be additional steps required to do so. Another method is manipulating the CMOS jumper.

### Configure BIOS

- Why might we alter BIOS settings?
  - Update firmware
  - Change boot order
  - Enable/disable a motherboard feature
  - Adjust a power, CPU, or RAM configuration setting
  - Clear the CMOS
- What scenarios would prompt us to interact with BIOS?
  - Motherboard malfunction requiring firmware update
  - Booting into the wrong device
  - Feature not configured on motherboard
  - Overclocking
  - Resetting the CMOS to default settings

### Demo: BIOS

- SAY: Next I’ll prepare you for today’s lab by showing you an example of BIOS and where all the important settings and information can be found. During the lab, you’ll use your lab PC, so your BIOS menus will differ from what you see here.

- DO: Navigate to a Lenovo BIOS Simulator (select IdeaCentre 310-15ASR (90G5)) and indicate where the below can be found. The simulator may not have all these.
  - Motherboard model
  - Processor specs
  - Total installed RAM
  - CPU Fan Speed
  - Processor Temperature
  - BIOS firmware version
  - Integrated Graphics Config
  - Menu to disable USB interfaces
  - Boot priority menu
  - Admin password menu
  - System Date & Time
  - Event Log
- If time allows, also show students the Phoenix BIOS Simulator for more exposure. Can’t do much on this one though; pressing ENTER just reloads the whole emulator.
Demonstrate on your exposed lab PC (disconnect power, check static discharge, etc.)
  - Show students where the CMOS battery is
  - Remind them what the CMOS battery does (retain BIOS configuration memory such as time & date, etc.)
  - Carefully remove the CMOS battery. You may need to grab your precision screwdriver to wedge it off. There are two black plastic clamps holding it in place.
  - Return the CMOS battery.

> Flashing BIOS means to update the firmware. If this goes awry, you can "brick" the device (render inoperable).

## Lab Time





