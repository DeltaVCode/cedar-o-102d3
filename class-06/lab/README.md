# Lab: SOHO Networking

Routers, hosts, and IP addressing form the basics of a SOHO (small or home office) network.

## Objectives

- Deploy a small office/home office (SOHO) router, the Linksys WRT54G, to broadcast a secure wireless network.

## Tasks

### Part 1: Ethernet Crimping

Create your own ethernet patch cable.
- Use the provided crimping tool and RJ45 jacks to achieve this.
- Verify success with the provided continuity tester.

### Part 2: SOHO Router Setup

- Power on your Linksys WRT54G Router near your computer workspace.
- Router will begin broadcasting a Wi-FI network called "linksys"
- Plug in a computer to the router via Ethernet cable or connect your computer to the Wi-Fi network "linksys" and open the router's configuration web portal at 192.168.1.1
- Login using default credentials, then change the password to the router configuration web portal to "codefellows2020###".
- Configure a Wi-Fi network broadcasting SSID "ops102".
- Select the most secure Security Mode. Require the password "codefellows2020###". 
  - Include a screenshot of the "Wireless Security" configuration. Describe what Security Mode you selected and justify why.
- If you have an ethernet jack with internet service nearby, plug router's WAN port into an existing network via Ethernet cable to transmit internet connectivity through router. This will create a lab-only sub-network. This step is not required to complete this lab.
- If you have not done so already, connect a Wi-Fi device to the "ops102" Wi-Fi network. 
- On the router configuration web portal, locate the DHCP Active IP Table, which lists all currently connected computers.
  - Include a screenshot of the DHCP Active IP Table. Describe what you see here and what it means.

## Stretch Goals (Optional Objectives)

- Include a screenshot of the Status > Router screen. Describe what each attribute here means to the best of your ability (e.g. Firmware Version is which firmware version this router is using).
- Deploy a wireless hotspot from your mobile phone
  - Describe the extent to which you can configure the wireless hotspot.
  - Describe how this differs from configuring a SOHO router.
  - Describe what security concerns may arise in using a wireless hotspot from your mobile phone.

## Submission Instructions

1. Name the document according to your course code and assignment.
   - i.e. `seattle-ops-102n1: Reading 01` or `seattle-ops-102d33: Lab 04`.
1. Add your name & date at the top of the Google Doc.
1. Share your Google Doc so that "Anyone with the link can view".
1. Paste the link to your Google Doc in the discussion field below and share an observation from your experience in this lab including how long this lab took to complete.
