# Demos: Virtualization of Ubuntu Linux OS

Use this document to describe the demo(s). Generally, this is going to take the format of either how to build the demo step by step, or less specifically, talking points surrounding the outcomes of the demo segment and code snippets to highlight.

## Demo: Install a VM with VirtualBox

### VirtualBox Deployment

> How to deploy your own virtual machine in VirtualBox (ref. [Walkthrough](https://askubuntu.com/questions/142549/how-to-install-ubuntu-on-virtualbox))

- Open VirtualBox and select New. A new window will come out.
- Choose your guest OS and architecture (32 vs. 64 bit, select Ubuntu)
- Set your Base Memory (RAM)
- Click next until it shows the VM storage size. Specify how much space you need depending on your available disk space and finish the wizard by clicking the create button.
- On VirtualBox's main window, select START and pick your MEDIA SOURCE. In your case, select the .iso on your desktop.
- Finish the installation as a normal install.
- Remove your installation .iso from the virtual optical disk drive before restarting the VM.
- Install Guest Additions.

### Configuring System Resources

Spend some time in class discussing the various settings. 
- RAM allocation
- Hard disk settings
- CPU allocation

> At this stage, you don't need to go super heavy on the networking settings. We'll focus on networking more later on, especially 301.
