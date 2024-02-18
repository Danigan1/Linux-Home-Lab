# Linux-Home-Lab

## The Beginning 
Hey there! Welcome to my GitHub repository documenting my journey of learning and exploring Linux as a beginner. As someone new to the world of Linux, I've created this repository to share my experiences, insights, and resources I've found useful along the way. Whether you're also just starting out or you're a seasoned Linux user looking to reminisce about your own beginnings, I hope you find something valuable here. Feel free to explore, leave feedback, or even join me in this exciting learning adventure!


## The Why

I've chosen to dive into learning Linux as a beginner for my journey into IT for several reasons. Firstly, Linux is the backbone of much of the IT infrastructure worldwide. Whether it's servers, networking equipment, or even mobile devices, Linux is everywhere. Understanding Linux gives me a solid foundation to work with a wide range of systems and environments.

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

what I did

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
