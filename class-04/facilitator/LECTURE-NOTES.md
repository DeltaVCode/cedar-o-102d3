# Lecture Notes: Installing Ubuntu Linux OS 

Use this document to add more details, flavor, hints, tricks, ideas to make lecture better. This should tie into the "Why, What, How" sections of the facilitator's README.

Consider the [README](README.md) in conjunction with the [DEMO](DEMO.md) as the single source of truth for a given class, while this document is more of the living, breathing, set of notes from all instructors as to what is historically working well.

## Topic 1: Operating Systems

- What is an operating system (OS)?
  - Primary software that manages hardware and software
  - Examples: Linux, MacOS, Windows, Android, iOS
- What does the OS do?
  - Interface between applications and hardware
  - Disk management
  - Process management/scheduling
  - Kill process/end task
  - Application management
  - Memory management
  - Device management
  - Access control/protection
  - Types of OS
    - Mobile device OS
    - Workstation OS
    - Server OS
    - Embedded OS
    - Firmware
    - Hypervisor (Type 1)

- Which OS should I learn?
  - For endpoints, Windows maintains the market share at 77% as of May 2020
    - Market prevalence means wide software support
    - High compatibility with Microsoft apps
    - Wide adoption in enterprise business environments
    - Wide support for gaming apps and drivers
    - Built-in support for Active Directory integration for client-server configurations
  - For lean home servers like our lab kit, Ubuntu is a beginner-friendly solution with its accessible Desktop GUI
  - Key vocabulary
    - Distribution/distro
      - Mostly applies to Linux. Examples: Ubuntu, Red Hat, Kali
    - Version
      - Windows 8 vs Windows 10
    - Edition
      - Windows 10 Home vs Windows 10 Pro
- Operating Systems VS Baseline
  - OS does not age well
  - Baseline lets you restore performance and working state  
- Lab plan
  - Remote into your lab kit PC; private cloud
- How to view system information
  - DXDIAG
  - Start + Pause
  - Install CPU-Z tool
- Disk Partitioning
  - In Windows GUI, Disk Management
  - From command line, diskpart
  - What is a partition?
    - Virtual allocation of storage space in the form of an assigned drive letter
    - Without a partition, your OS can't read the drive
- File systems used by Windows OS
  - EXT4
    - Default Linux files system. Number denotes generation; 4 is latest EXT iteration.
  - NTFS 
    - Windows default for OS and internal drives
  - FAT32
    - Save this for USB flash drives
  - exFAT - Extended File Allocation Table
    - Save this for USB flash drives, attempt at improving FAT32


- What units of memory do I need to know?
  - Bit
  - Byte
  - Kilo Byte
  - Mega Byte
  - Giga Byte
  - Tera Byte

- How do these convert?
  - 1 Bit = Binary Digit
  - 8 Bits = 1 Byte
  - 1024 Bytes = 1 KB (Kilo Byte)
  - 1024 KB = 1 MB (Mega Byte)
  - 1024 MB = 1 GB (Giga Byte)
  - 1024 GB = 1 TB (Terra Byte)

## Demo: Configuring Ubuntu

- Show the Ubuntu installation process




