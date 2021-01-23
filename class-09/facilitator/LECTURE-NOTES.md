# Lecture Notes: Basic Windows Operations

Use this document to add more details, flavor, hints, tricks, ideas to make lecture better. This should tie into the "Why, What, How" sections of the facilitator's README.

Consider the [README](README.md) in conjunction with the [DEMO](DEMO.md) as the single source of truth for a given class, while this document is more of the living, breathing, set of notes from all instructors as to what is historically working well.

## Career Development
- Certifications
  - At this stage, you should consider CompTIA ITF+
  - After Ops 201, consider CompTIA A+
  - After Ops 301, consider CompTIA Network+
  - After Ops 401, consider CompTIA Security+
- Why home lab?
  - Discuss some home lab communities and why people do this
  - Examples Reddit's r/homelab, Discord for homelab

## Basic Windows Operations

How does Windows differ from Linux?
- Fundamentally different systems architectures
- A software made for Windows won't run on Linux, etc.

How do I get 1080p on this thing?
- Virtualbox Guest Additions

### View System Information

- DXDIAG
- This PC 

### Windows Command Line

Why would we use the Windows Command Prompt?
- Diagnostic tools/troubleshooting
- Automation

What is the Command Prompt?
- It's not DOS like many people will casually claim; cmd.exe is actually its own application
- Presents a terminal from which you may issue commands
- Does NOT support Powershell commands (more on that later)

What are some basic commands I should know?
- `systeminfo`
- `ipconfig /all`
- `ping`
- `tracert`

What is the "Run" menu?
- Directly execute programs by name
  - `regedit`
  - `msfconfig`
  - `dxdiag`

## Windows Control Panel

Why would we use the Control Panel?
- Uninstall a Program
- Add/Remove Features
- Network and Internet
- User management
- Security
- Power

What is the Control Panel?
- Area where systems administrator can configure the computer
