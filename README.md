# Linux-Home-Lab

## The Beginning 
Hey there! Welcome to my GitHub repository documenting my journey of learning and exploring Linux as a beginner. As someone new to the world of Linux, I've created this repository to share my experiences, insights, and resources I've found useful along the way. Whether you're also just starting out or you're a seasoned Linux user looking to reminisce about your own beginnings, I hope you find something valuable here. Feel free to explore


## Why Linux?

Linux is the backbone of much of the IT infrastructure worldwide. Whether it's servers, networking equipment, or even mobile devices, Linux is everywhere. Understanding Linux gives me a solid foundation to work with a wide range of systems and environments.

Moreover, Linux is known for its stability, security, and scalability. These are critical aspects of IT that I want to master early on in my career. By learning Linux, I'm equipping myself with the skills needed to maintain robust and secure systems, which is invaluable in today's tech landscape.

Another reason for choosing Linux is its open-source nature. The vast community behind Linux means there's a wealth of resources available for learning and troubleshooting. Plus, being part of the open-source community allows me to contribute to projects, collaborate with others, and continuously improve my skills.



## Linux Distribution of choice
So I've decided to dive into **Rocky Linux version 9** for my Linux learning journey, and here's why.

![image](https://github.com/Danigan1/Linux-Home-Lab/assets/107498392/43880a43-4f6e-41e4-992e-8825619fd0c3)

First and foremost, Rocky Linux is a community-driven, enterprise-grade Linux distribution designed to be a seamless replacement for CentOS. It's built to be rock-solid (pun intended) and stable, which is exactly what I need as I dive into learning Linux. Having that stability means I can focus on learning without worrying about frequent changes or instability.

Another big reason for choosing Rocky Linux is its strong ties to the open-source community and its close relationship with Red Hat Enterprise Linux (RHEL). Since it's a downstream rebuild of RHEL, I'll essentially be working with a free, community-supported version of RHEL. This is incredibly valuable because RHEL is widely used in enterprise environments, so learning on Rocky Linux means I'll be gaining skills that are directly transferable to real-world scenarios and job opportunities.

## Downloads

**Rocky linux 64 Bit ISO**

- https://rockylinux.org/download

**Virtual box**

- https://www.virtualbox.org/wiki/Downloads

**Download the version of VirtualBox that matches your host operating system (e.g., Windows, macOS, or Linux)*

<br>

## Installation

<img width="1792" alt="Screenshot 2024-02-18 at 4 07 26 PM" src="https://github.com/Danigan1/Linux-Home-Lab/assets/107498392/6f2e30b7-832f-4920-b8e3-9d5a1ed0c55b">


- **Download Rocky Linux ISO:** First, I downloaded the Rocky Linux ISO file from the official website 

- **Install VirtualBox:** If I didn't have VirtualBox installed already, I went to the VirtualBox website and downloaded the appropriate version for my operating system. Then, I followed the installation instructions.

- **Open VirtualBox:** I launched VirtualBox after installation.

- **Create a New Virtual Machine:** In VirtualBox, I clicked on "New" to create a new virtual machine.

- **Name and Operating System:** I entered a name for the virtual machine (e.g., "Rocky Linux"), selected "Linux" as the type, and chose "Red Hat (64-bit)" as the version since Rocky Linux is based on Red Hat.

- **Memory Size:** I allocated the amount of RAM I wanted to assign to the virtual machine. A minimum of 1 GB is recommended, but I allocated more based on my system's resources.

- **Hard Disk:** I selected "Create a virtual hard disk now" and chose the default options for the hard disk file type and storage on physical hard disk.

- **Hard Disk File Type:** I selected the default option, VDI (VirtualBox Disk Image).

- **Storage on Physical Hard Disk:** I chose "Dynamically allocated" to allow the virtual hard disk file to grow as needed.

- **File Location and Size:** I specified the location and size for the virtual hard disk file. The default size is usually sufficient, but I adjusted it as needed based on my requirements.

- **Finish and Settings:** After creating the virtual machine, I clicked "Create" to finish. Then, I selected the virtual machine from the list and clicked on "Settings."

- **Storage:** In the settings menu, I went to the "Storage" tab, clicked on the empty optical drive, and selected "Choose a disk file." I navigated to the location where I downloaded the Rocky Linux ISO file and selected it.

- **Network:** I ensured that the network adapter was enabled and set to "NAT" or "Bridged" mode, depending on my networking preferences.

- **Start the Virtual Machine:** Finally, I clicked "OK" to close the settings menu and started the virtual machine by clicking the "Start" button.

- **Install Rocky Linux:** The virtual machine booted from the Rocky Linux ISO, and I followed the on-screen prompts to install Rocky Linux just like I would on a physical machine. I selected the installation language, keyboard layout, partitioning options, user account setup, and other configuration settings as needed.

- **Reboot:** Once the installation was complete, I rebooted the virtual machine and logged in to my newly installed Rocky Linux system.


# Drivers Installation needed

So, after finishing setting up Rocky Linux on my virtual machine, I noticed that there were a few areas where I needed to enhance functionality to ensure smooth operation. Specifically, I needed to install some drivers to enable features like shared clipboard, drag and drop between the host machine and the Linux guest machine, eliminating any mouse offset issues, and setting up shared folders for seamless file sharing.

Getting these drivers installed was crucial to improving the overall workflow and efficiency of my virtual machine setup. It took a bit of time and effort to set everything up just right, but once I got those drivers in place, everything ran much more smoothly between the host and guest machines.

Overall, it was definitely worth the effort to enhance the functionality of my Rocky Linux virtual machine and make it a more seamless part of my workflow.

**what I did:**

- updated the system
- installed additional ways to fetch additional software
- Then I updated the system again
- Installed tools required to compile drivers (the drivers were there but were there in source code. They had to be turned into executable stuff that we can install)
- installed drivers

### Configuration Recap
<br>

 **1.) Update your system**
<br>

`sudo dnf update`

If new updates were installed (in particular regarding the kernel) → **Restart your virtual machine** 🔛

**2.) Install additional packages**
<br>
`sudo dnf install epel-release`

**3.) Update your system again**
<br>
`sudo dnf update`

**4.) Install additional tools**
<br>
`sudo dnf install gcc kernel-devel kernel-headers make bzip2 perl`

**5.) Install the Guest Additions**
<br>
In VirtualBox menu bar: `Devices > Insert Guest Additions CD Image…`

Execute `VBoxLinuxAdditions.run`

**Restart your virtual machine** 🔛

<br>


## Bash CLI introduction


The first thing I most do is confirm I am actually using the bash shell since there are many shells out there.




https://github.com/Danigan1/Linux-Home-Lab/assets/107498392/cd3bb0f0-6fdf-4cf6-99bc-a0d3ae117b20

<br>

this showscases that we are **indeed** running the bash shell with a specified version



**key tip: folders are also known as directories*
### key commands

`echo` - allows you to output text in the terminal
<br>

**example:** `echo 'bash is amazing'`

<br>

command = `echo`

arguement= everything after

option =  `-n`

<br>


`-n` - surpresses the line break that echo outputs by default. 

`\n` - is supposed to **represet** a line break

`-e` - will notice that there is a **"backslash escape"** such as **\n, \t, \b** and act on it   

**backslash esapes:** special combinations of characters that begin with a backslash \ followed by another character

<br>

`pwd` - showcase the current directory you are on

`cd` - change directories by going forward or backward

**example:** 
<br>
`cd Desktop` = go into a directory that is within your current directoy
<br>

`cd ..` = go to previous directory
<br>

`cd /` = absolute path
<br>
`cd ~` = move me into **(user)** home directory

<br>


`ls` - list the "contents" of your current directory

`ls -a` - lists any *hidden* files and folders **as well** as regular files/folder

`ls -t` - sorts the list of files and folders by **modification time**, with recently modified first.

`ls -r` - reverse option that reveres what is already in place

<br>

### Absolute path vs relative path

Absolute path 

- starts with a / (root)
- defines the **complete** path to a file/folder
- it works everywhere no matter our current working directory
<img width="1792" alt="Screenshot 2024-02-19 at 2 11 56 PM" src="https://github.com/Danigan1/Linux-Home-Lab/assets/107498392/d7aae97e-6a68-4871-a546-eae70506cab3">

<br>
<br>
Relative path

-  A relative path specifies the location of a file or directory relative to the current working directory. **It does not start from the root directory**. Instead, it describes the location of the file or directory in relation to where you currently are in the file system.
  
- shorter and more convenient to use
  
**example:**

if a start in Documents directory

/home/dmbaabu/Documents

Lets say I want to nagivate to Pictures directory

i can do `cd ../Pictures`


<img width="1792" alt="Screenshot 2024-02-19 at 2 07 47 PM" src="https://github.com/Danigan1/Linux-Home-Lab/assets/107498392/dcaf353f-dc52-4a88-83a4-d7223ce9e8bf">


## Executing mulitple commands one after the other

This can be done by using the semicolon `;`

and inputing multiple commands

**Example:** I changed to the `root` directory then changed again to the `Desktop` directory and created a text file named `this.txt` with the word **hi** in it

<img width="1792" alt="Screenshot 2024-02-20 at 1 38 08 PM" src="https://github.com/Danigan1/Linux-Home-Lab/assets/107498392/dad30ffd-f212-4cf1-abd1-f0dc507aec75">


