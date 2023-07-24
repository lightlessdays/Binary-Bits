---
title: "What is BIOS?"
datePublished: Fri May 05 2023 09:31:28 GMT+0000 (Coordinated Universal Time)
cuid: clhacwphw001209mhc18xfavv
slug: what-is-bios
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683279052315/49736e57-c31d-4878-ab18-f146b8a48bd8.png
tags: operating-system

---

When you start your computer, the very first thing(code) that runs on that system is BIOS. A piece of code or we can say a small piece of code contained in a chip(microprocessor) on your motherboard.

So, What is BIOS? The name itself suggests the meaning of the word, BIOS stands for Basic Input/Output System. While starting your computer you have no idea what is happening inside your computer or the functioning of your computer. The first thing BIOS does is, BIOS identifies your computer’s hardware, configure the BIOS setup for you, test all the workings for you, and connect it to the Operating System for your further instructions.

A BIOS (Basic Input/Output System) Short for ROM is a boot firmware program that a computer uses to successfully start operating. The BIOS is located on a chip inside of the computer and is designed in a way that protects it from disk failure.

When you turn on a PC, the BIOS first conduct a basic hardware check, called a Power-On Self Test (POST), to determine whether all of the attachments are present and working. Then it loads the operating system into your computer’s random access memory or RAM. The BIOS also manages data flow between the computer’s operating system and attached devices such as the hard disk, video card, keyboard, mouse, and printer. The BIOS stores the date, the time, and your system configuration information in a battery-powered, non-volatile memory chip, called a CMOS (Complementary Metal Oxide Semiconductor) after its manufacturing process.

## Functions of BIOS

1. **BIOS Power on Self Test (POST):** It is a built-in diagnostic program. This self-test ensures that the computer has all of the necessary parts and functionality needed to successfully start itself, such as the use of memory, a keyboard and other parts. Then additional tests are done during booting. If errors are detected during the test, the BIOS instruct the computer to give a code that reveals the problem. Error codes are typically a series of beeps heard shortly after startup.
    
    The BIOS also works to give the computer basic information about how to interact with some critical components, such as drives and memory that it will need to load the operating system. Once the basic instructions have been loaded and the self-test has been passed, the computer can proceed with loading the operating system from one of the attached drives. Computer users can often make certain adjustments to the BIOS through a configuration screen on the computer. The setup screen is typically accessed with a special key sequence during the first moments of startup. This setup screen often allows users to change the order in which drives are accessed during startup and control the functionality of several critical devices. Features vary among individual BIOS versions. We can also use flash-memory cards to hold BIOS information. This allows users to update the BIOS version on computers after a vendor releases an update. This system was designed to solve problems with the original BIOS or to add new functionality. Users can periodically check for updated BIOS versions, as some vendors release a dozen or more updates throughout a product’s lifetime. Motherboard (System) BIOS, Video adapter firmware (BIOS), Drive controller firmware (BIOS), Modem Card firmware (BIOS), Network adapter board BIOS, SCSI adapter BIOS. The motherboard BIOS provides routines to support motherboard features. BIOS ROM chips for major sub-systems of computers such as video and drive control must also be included.
    
    BIOS can be placed in between the computer and external devices as its name tells it is used for reading the keystroke, displaying values on screen, Reading and writing to and from floppy and hard disks etc. The keyboard is assigned port number 60, which is known as BIOS. BIOS read this port and data from the keyboard goes to the computer.
    
2. **Bootstrap Loader**: To boot the operating system. The BIOS contains a program known as bootstrap loader whose responsibility is to search and start the operating system boot program. Then the boot program of the operating system controls the computer system and boots the operating system.
    
3. **BIOS Setup Utility Program:** A non-volatile memory (NVRAM) is used to store information about the computer system. During the installation of a system, the user runs the BIOS setup program and enters the correct parameters. The settings of memory, disk types and other settings are stored in NVRAM and not in the BIOS chip itself. To construct NVRAM, the material required is CMOS (Complementary metal oxide semiconductor). These CMOS chips are very efficient storage devices as they store and maintain data on very low values of current. The system’s configurations, therefore, are also termed CMOS settings, which we can set using the BIOS setup program. The BIOS reads the parameters from CMOS RAM as and when required. CMOS settings can be maintained by battery backup either by using a capacitor or by a battery built into the NVRAM chip. This chip also has a system clock. If there is no battery, the setting remains for a short period and we need to reset the system. With it, there is a loss of the BIOS password which protects the BIOS set-up program.
    

## Booting the Computer

Whenever you turn on your computer, the first thing you see is the BIOS software doing its thing. On many machines, the BIOS displays text describing things like the amount of memory installed in your computer, the type of hard disk and so on. It turns out that, during this boot sequence, the BIOS is doing a remarkable amount of work to get your computer ready to run. This section briefly describes some of those activities for a typical PC.

After checking the CMOS Setup and loading the interrupt handlers, the BIOS determines whether the video card is operational. Most video cards have a miniature BIOS of their own that initializes the memory and graphics processor on the card. If they do not, there is usually video driver information on another ROM on the motherboard that the BIOS can load.

Next, the BIOS checks to see if this is a **cold boot** or a **reboot**. It does this by checking the value at memory address 0000:0472. A value of 1234h indicates a reboot, and the BIOS skips the rest of the POST. Anything else is considered a cold boot.

If it is a cold boot, the BIOS verifies RAM by performing a read/write test of each memory address. It checks the PS/2 ports or USB ports for a keyboard and a mouse. It looks for a **peripheral component interconnect** (PCI) bus and, if it finds one, checks all the PCI cards. If the BIOS finds any errors during the POST, it will notify you by a series of beeps or a text message displayed on the screen. An error at this point is almost always a hardware problem.

The BIOS then displays some details about your system. This typically includes information about:

* The processor
    
* The floppy drive and hard drive
    
* Memory
    
* BIOS revision and date
    
* Display
    

Any special drivers, such as the ones for **small computer system interface** (SCSI) adapters, are loaded from the adapter, and the BIOS displays the information. The BIOS then looks at the sequence of storage devices identified as **boot** devices in the CMOS Setup. "Boot" is short for "bootstrap," as in the old phrase, "Lift yourself by your bootstraps." Boot refers to the process of launching the operating system. The BIOS will try to initiate the boot sequence from the first device. If the BIOS does not find a device, it will try the next device in the list. If it does not find the proper files on a device, the startup process will halt. If you have ever left a disk when you restarted your computer, you have probably seen this message.

The BIOS has tried to boot the computer off of the disk left in the drive. Since it did not find the correct system files, it could not continue. Of course, this is an easy fix. Simply pop out the disk and press a key to continue.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1683278770633/0311df0b-31b5-45d3-8dfb-869d6d823b51.jpeg align="center")

## Configuring the BIOS

To enter the CMOS Setup, you must press a certain key or combination of keys during the initial startup sequence. Most systems use "Esc," "Del," "F1," "F2," "Ctrl-Esc" or "Ctrl-Alt-Esc" to enter setup. There is usually a line of text at the bottom of the display that tells you "Press \_\_\_ to Enter Setup."

Once you have entered the setup, you will see a set of text screens with several options. Some of these are standard, while others vary according to the BIOS manufacturer. Common options include:

System Time/Date - Set the system time and date Boot Sequence - The order that BIOS will try to load the operating system Plug and Play - A standard for auto-detecting connected devices; should be set to "Yes" if your computer and operating system both support it Mouse/Keyboard - "Enable Num Lock," "Enable the Keyboard," "Auto-Detect Mouse"... Drive Configuration - Configure hard drives, CD-ROM and floppy drives Memory - Direct the BIOS to shadow to a specific memory address Security - Set a password for accessing the computer Power Management - Select whether to use power management, as well as set the amount of time for standby and suspend Exit - Save your changes, discard your changes or restore default settings Be very careful when making changes to the setup. Incorrect settings may keep your computer from booting. When you are finished with your changes, you should choose "Save Changes" and exit. The BIOS will then restart your computer so that the new settings take effect.

The BIOS uses CMOS technology to save any changes made to the computer's settings. With this technology, a small lithium or Ni-Cad battery can supply enough power to keep the data for years. Some of the newer chips have a 10-year, tiny lithium battery built right into the CMOS chip!

![](https://img-9gag-fun.9cache.com/photo/a9qnQA0_460s.jpg align="center")

## Types of BIOS

There are two main types of BIOS:

* **Legacy BIOS:** Legacy BIOS is used in older motherboards to turn on the computer, and it controls how the CPU and different computer components talk to each other. Unfortunately, the Legacy BIOS has limitations. For example, it can’t handle or recognize data drives larger than 2.1 TB.
    
* **UEFI:** The acronym stands for Unified Extensible Firmware Interface. Unlike the Legacy BIOS, the UEFI can accommodate 2.2 TB or larger drives. In addition, UEFI handles drives with the aid of the Master Boot Record rather than GPT technology, the latter being a more modern GUID Partition Table.
    

UEFI is the newest of the two boot software offerings, released in 2002. Compared to BIOS, UEFI has greater scalability, higher performance, better programmability, and higher security. In addition, UEFI doesn't require a separate bootloading program to load the operating system. UEFI also has a better user interface and overall faster speeds

IT tech giants such as Intel, AMD, AMI, Apple, Dell, HP, IBM, Lenovo, and Microsoft have phased out BIOS or are in the process of doing so in favor of UEFI. So it looks like BIOS is slowly going away.

![Boot Sequence/Order/Priority Configuration of UEFI BIOS – DESKDECODE.COM](https://i0.wp.com/www.deskdecode.com/wp-content/uploads/2021/10/UEFI-vs-BIOS-MEME.jpg?resize=746%2C438&ssl=1 align="center")

## Upgrading BIOS

To upgrade BIOS, follow the steps mentioned:

* Check your current BIOS version.
    
* Enter the UEFI BIOS on the Boot menu.
    
* Boot into the UEFI control panel(when possible)
    
* Check for the latest BIOS update which is available from your motherboard’s support page.
    
* On a USB file drive, transfer the updated and downloaded file.
    
* Use the same UEFI utility as your new firmware which is stored on your flash drive.
    
* Once the update is complete, restart your system.
    

Thanks for reading :)