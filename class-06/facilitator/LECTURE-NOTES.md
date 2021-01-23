# Lecture Notes: SOHO Networking 

Use this document to add more details, flavor, hints, tricks, ideas to make lecture better. This should tie into the "Why, What, How" sections of the facilitator's README.

Consider the [README](README.md) in conjunction with the [DEMO](DEMO.md) as the single source of truth for a given class, while this document is more of the living, breathing, set of notes from all instructors as to what is historically working well.

## Review

## Topic 1: Ethernet

Discuss - Why are networks used?
On the diagram we drew, identify the components and where basic network concepts would appear on this diagram.
Moving information in a (hopefully) secure fashion from computer to computer, or computer to internet (and vice versa)
Why might we diagram a network?

WHITEBOARD DO: Draw an example network
- Internet
- Modem
- Router
- Switch
- Wi-fi devices
- Cabled PC

WHITEBOARD DO: Define for students and whiteboard for them
- IP Address - Every computer on the LAN must have a unique IP
- DNS - Domain Name System servers translate “google.com” > a real usable IP in the background
- DHCP Server - Assigns IPs automatically
- Subnet Mask
- Gateway

Run `ipconfig /all` or `ip a` and identify all the essential components of your machine’s network configuration
- MAC address
- IP address
- DNS server address
- Subnet Mask
- Gateway address

## Topic 2: Ethernet Crimping

- Discuss: What is Ethernet cabling? Why might organizations use this?
  - What is an RJ-45 Jack?
  - What does crimping mean?

- Hands on class exercise: How to crimp a Cat5/5e/6 ethernet cable?
  - Demonstrate how to crimp a network cable, have students follow along to crimp and continuity test their first cable
  - Connect the cable from WRT54G SoHo router to student computer to prep for lab
  - Crimp ethernet cable and test its continuity

- Hands on class exercise: How to use a punchdown tool
  - Ethernet RJ45 crimping using B-Standard
  - Keystone jack punchdown using B-Standard
  - Explain how multiple keystone jacks form a patch panel

## Topic 3: Routers

> David’s story - Faulty router: For one of the clients I supported, the router would constantly go down for no apparent reason (at least once a week). Along with it would go an entire network of computers, and a LOT of user complaints. Rebooting it always fixed the immediate outage. When I finally replaced the router, I noticed it was heavily customized and you could not simply install a replacement and walk away. Router configurations can be very specific to the networks they service. After a few hours of copy-pasting, the network was back to its original, operational self again.

Demo: Router Deployment

- Given a SOHO router, deploy a wireless network
  - Plug into an existing network to create a subnet
    - Avoids disrupting the overall home network
  - Plug in a computer to the router and follow instructions for setup
    - Use built-in startup wizard at first
    - On Wi-Fi, configure a DHCP pool of 192.168.64.1-192.168.64.200
    - Connect a Wi-Fi device. What IP does it receive?
    - Is your Wi-Fi separated from your cabled network?
  - Connect a device to the wireless network
  - Lookup your device’s IP configuration
    - Windows: ipconfig
  - Inspect the menus in your router portal
    - Can you see devices?
    - Inspec
- Document your experience
  - WAN IP
  - Wi-Fi configuration
  - SSID
  - Password
  - Encryption method
  - DHCP pool configuration
  - Reserved IPs
  - Gateway
  - Subnet mask
  - Ethernet configuration
  - DHCP pool configuration
  - Reserved IPs
  - Gateway
  - Subnet mask

