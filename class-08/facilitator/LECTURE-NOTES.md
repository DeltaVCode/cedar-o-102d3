# Lecture Notes: Virtualization of Windows OS

Use this document to add more details, flavor, hints, tricks, ideas to make lecture better. This should tie into the "Why, What, How" sections of the facilitator's README.

Consider the [README](README.md) in conjunction with the [DEMO](DEMO.md) as the single source of truth for a given class, while this document is more of the living, breathing, set of notes from all instructors as to what is historically working well.

**WHY**

- Why will we be using Virtualbox?
  - Free
  - Supports .ova import/export without licensing (VMware does not)
  - Work with different kinds of computers and multiple computers on a single host

**WHAT**

- What is a virtual machine (VM)?
  - Abstracting away the computer hardware
  - Only dealing with the OS, networking, etc.
  - A computer inside a computer
  - Multiple computers per host computer

- What is required to virtualize?
  - Intel VT-X or AMD-V capable chipset
  - Host OS that supports the chosen virtualization software 
  - Virtualization software

- What operating systems are we able to virtualize?
  - Linux distributions (GNU public license)
  - Windows non-activated installations from ISO or [evaluation editions](https://www.microsoft.com/en-us/evalcenter/)
  - Not macOS due to Apple's terms of use that forbid virtualizing on non-Apple hardware
  - Not systems to which we don't have legal license (piracy)

- What operating systems will we be virtualizing in the Ops sequence?
  - Ubuntu 20.10 Desktop
  - Ubuntu 20.10 Server
  - Kali Linux
  - Windows Server 2019
  - Windows 10
  - Windows 7
  - pfSense 
    - Not exactly an OS but a router/firewall appliance

**HOW**

- How can I get better performance from virtual machines?
  - Add more RAM is always a good first step
  - Add more CPU speed and cores
  - Consider how you're accessing it

- Ref [DEMO.md](DEMO.md)