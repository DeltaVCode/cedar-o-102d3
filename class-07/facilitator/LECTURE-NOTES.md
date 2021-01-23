# Lecture Notes: Network Connectivity 

Use this document to add more details, flavor, hints, tricks, ideas to make lecture better. This should tie into the "Why, What, How" sections of the facilitator's README.

Consider the [README](README.md) in conjunction with the [DEMO](DEMO.md) as the single source of truth for a given class, while this document is more of the living, breathing, set of notes from all instructors as to what is historically working well.

**WHY**

- Why remote into the lab kit PC?
  - Reduces clutter in your work area; who wants to deal with two of everything?
  - "Personal cloud" concept; only cost is initial purchase and cost of maintenance is a little electricity, VS cloud hosting service charges which are pay as you go
  - Keep lab work on a dedicated system
  - Disposable; if it breaks, reload; keep your personal data safe in case you need to wipe and start over. 
    - Set expectation to not a matter of if but when something goes sideways. Plan for the worst.
    - Reduces stress and level of impact on your stuff.

- Why reserve an IP address from the DHCP server?
  - The other day we talked about DHCP leases; IP addresses expire and then the computer may be assigned a new IP.
  - By reserving the IP, we will know the IP every time; do not allow IP to change 
  - Requires the MAC address to be known

**WHAT**

- What is a network port?
  - Ports are like doorways into your computer system.
  - Each port has a number.
  - So, ports are like doors with a number.
  - In both Windows and Linux, the ports can be opened or closed by the software firewall.
  - Open ports are required for the services that use them. Let's take a look at some examples we'll be using today.

- What methods can we use to interact remotely with our lab kit PC?
  - SSH (Secure Shell) via port 22
  - RDP (Microsoft Remote Desktop Protocol) via port 3389
  - VNC (Virtual Network Connection) via 5900, 5800
  - SCP (Secure Copy Protocol) via port 22

- What is SSH?
  - Secure Shell is a modern standard for remote terminal access.
  - SSH was created by [Tatu Ylonen](https://ylonen.org/) in 1995 as a successor to telnet (port 23) and FTP (port 21), which were heavily used at the time.
  - SSH uses password authentication to establish a terminal-only connection to a computer running the SSH service
  - Requires port 22 to be open on the "server"
  - Many applications such as WinSCP and VSCode can "piggyback" SSH by using it as a background means of transferring data

- What is Git Bash?
  - Windows command line prompt is underwhelming; Git Bash is recommended.
  - Git Bash is a terminal we can use on Windows. This is superior to the native terminal and a useful swiss army knife for intensive terminal work such as SSH activities. There are many alternatives to this, such as Cmder.
  - If you're a beginner to running alternative terminal apps on Windows, start here.

- What is RDP and what about XRDP?
  - The remote desktop protocol (RDP) is built into Microsoft Windows.
  - Not known for greatest security, but within a LAN like our home it's fine
  - Can be used by macOS if installed separately

- How about macOS users?
  - Can install RDP separately or use the alternative, VNC
  - Today's lab instructions will give macOS users some alternative options

- What is SCP?
  - Secure Copy Protocol (SCP) lets you transfer files fromm one computer to another
  - Normally, you'd use the command line to do so
  - Today we'll be using a graphical user interface (GUI) mostly for ease of use

- What is WinSCP?
  - GUI for SCP on Windows
  - Requires SSH to work

- What about macOS users?
  - See lab notes

**HOW**

- Ref. [DEMO.md](DEMO.md)
