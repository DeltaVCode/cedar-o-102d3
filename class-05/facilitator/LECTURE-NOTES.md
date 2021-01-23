# Lecture Notes: Install Virtualbox using Linux Terminal 

Use this document to add more details, flavor, hints, tricks, ideas to make lecture better. This should tie into the "Why, What, How" sections of the facilitator's README.

Consider the [README](README.md) in conjunction with the [DEMO](DEMO.md) as the single source of truth for a given class, while this document is more of the living, breathing, set of notes from all instructors as to what is historically working well.

## Topic 1: Linux Terminal

**WHY**

Why do we need to know Linux terminal?
- Terminal commands are lower level than GUI
- Not all programs have GUI
- Essential for operating Linux

**WHAT**

What is the Linux terminal?
- Many versions exist. It's an app that you launch on Ubuntu Desktop.
- If Ubuntu Server, is the default way you use the computer.
- Low level interaction with a computer; GUI desktop is a higher level of abstraction and "hides" the commands

What is a script?
- This is a file that when executed runs multiple commands.

What is root?
- This is the superuser account of the computer with full clearance.
- The account you use will by default not be root, by design. Equivalent idea in Windows might be local user vs admin user.
- Older versions of Linux let you start out as root.

What is Github?
- Github is the web application that acts as a script repository
- Git is the installed software package that lets you interact with Github
- Industry standard place to store and share scripts/code.
- Many open source programs can be found on Github
- When you download a Github repository using Git, it's called "cloning" the repo

**HOW**

How do I operate the Linux terminal?
- First, observe the prompt. This is a persistent representation of where you are in the file system. You'll see `username@computername` in most terminals to indicate it is ready for your action. 
- If you see a blank screen, dots, falling code, or other animations, you're probably waiting for a process and can't type in new actions. `CTRL+C` breaks out of a running process.
- `pwd` and `ls` and `ls -al` will show you where you are currently located. Use this often.
- `cd [path]` will change directory
- `mkdir [path/dirname]` will create a directory
- `sudo [command]` will elevate your command to root after you type the password
- `[appname] -[modifier parameter] [target/action parameter]` is the general syntax for doing a thing with a program, e.g. `firefox google.com` opens Google with Firefox. There are exceptions; every program is different in what it expects of you.
- Modifier parameters alter how a program behaves. `ls -al` lists more details than `ls` alone. The minus sign is a common indicator it's a modifier.
- Some programs run without any parameters.

How do I clone a repository from Git and execute a script?
- `sudo apt install git -y`
- `sudo bash [script]` will execute a script as root