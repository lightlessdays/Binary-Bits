---
title: "What is an Operating System?"
datePublished: Tue May 02 2023 14:11:42 GMT+0000 (Coordinated Universal Time)
cuid: clh6clirx000j09jo5ox97z6c
slug: what-is-an-operating-system
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683036671242/26fa329f-f195-44a2-a118-ec92c7068932.png
tags: operating-system

---

An Operating System (OS) acts as an interface connecting a computer user with the computer's hardware. An operating system falls under the category of system software that performs all the fundamental tasks like file management, memory handling, process management, handling the input/output, and governing and managing the peripheral devices like disk drives, networking hardware, printers, etc. Some well-liked Operating Systems are Linux, Windows, OS X, Solaris, OS/400, Chrome OS, etc.

## Features of an Operating System

Here is a list of some significant functions of an Operating System, which is found common in almost all operating systems:

1. **Resource management**: Operating systems manage the computer's resources, such as its memory, processor, and storage, and allocate them to different tasks as needed.
    
2. **Memory management**: Operating systems manage the computer's memory and ensure that each program or process has access to the memory it needs to run.
    
3. **Process management**: Operating systems create and manage processes, which are units of work executed by the computer.
    
4. **File management**: Operating systems manage the files on the computer, including organizing them and providing access for different programs and users.
    
5. **Security**: Operating systems include security features to protect the computer from unauthorized access and viruses.
    
6. **User interface**: Operating systems provide an interface for users to interact with the computer, such as through a graphical user interface (GUI) or command-line interface (CLI).
    
7. **Networking**: Many operating systems include support for networking, allowing the computer to communicate and exchange data with other devices over a network, such as the internet or a local area network (LAN).
    
8. **Device management**: Operating systems manage the devices connected to the computer, such as printers, keyboards, and storage devices.
    
9. **Power management**: Operating systems include features to manage the power usage of the computer and conserve energy when possible.
    
10. **Software installation and updates**: Operating systems provide a mechanism for installing and updating software applications.
    

These are just a few examples of features commonly found in operating systems. The specific features of an operating system depend on the particular system and its intended use.

## Examples of Operating Systems

* Windows
    
* Macintosh
    
* IpadOs
    
* Android
    
* Linux
    
* BSD
    
* Solaris
    

## Types of Operating Systems

There are various types of Operating Systems. Let’s see a few types of OS:

### Simple Batch Systems

As early computers used to be very expensive, we couldn't afford to waste processor time, so to maximize processor utilization, Simple batch systems evolved. The central idea behind simple batch systems uses software known as monitor, which interfaces with the processor directly and refrains users from accessing the processors directly.

The user fed an input to the computer operator, who gathered similar jobs(tasks to be performed) and placed an entire batch (group of similar type tasks) for utilization by the monitor. Each program is built to branch back to the monitor when it completes processing. At this point, the monitor automatically begins loading the following program.

With a batch Operating System, processor times alternate between the execution of the user's program and the execution of the monitor. However, now some main memory is given to the monitor, and the monitor consumes some processor time. Both of these are some forms of overhead. Despite this overhead, simple batch systems improve the utilization of the processor.

### Multi-programmed Batch Systems

Regardless of the automatic job sequencing provided by the Simple Batch OS, the processor is often idle. The problem is I/O devices couldn't compete with the processors in terms of speed. Thus I/O devices are slow. The main idea of Multi-programmed batch systems is when one job/task needs to wait for I/O, OS could switch to a different task/job and start executing it; when the I/O devices finished their execution, then again, it switches back to the first job and resumes its execution where it left off.

### Time-Sharing Systems

It has been developed to provide user interaction directly with the computer. Since, In batch multiprogramming, we used to provide **JCL (Job control commands)** with the job. But for things like transaction processing, we needed user interaction. Therefore the concept of time-sharing has been introduced. In this, a system clock generated interrupts at a rate of around one every **0.2 seconds**.

At each clock interrupt, the Operating System reclaims control and could assign the processor to another user. This technique is known as time slicing. Suppose n users interact with the same computer; each user will only see on average **1/n** of the effective computer capacity. Thus, at regular time intervals, the current user would be preempted and another user loaded in.

To retain the old user program status for later continuation, the old user programs and data were saved to disk before the new user programs and data were read.

Subsequently, the old user program code and data were restored in the main memory when that program was next given a turn. The main motive of time-sharing systems was to allow many users to share the computer resources which means max utilization of resources.

### Real-Time Operating System

In a real-time system, the time interval between input request and output is very small, so these systems can be used in a time constraint places like military software systems, space software, etc.

### Distributed Operating System

In distributed various computers, interconnected with each other communicate with each other through the shared communication network. Each machine has its own processors and memory unit for fast computation. These are also known as distributed systems.