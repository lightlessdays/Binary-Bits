---
title: "Introduction to Java"
datePublished: Fri Apr 28 2023 11:47:39 GMT+0000 (Coordinated Universal Time)
cuid: clh0hover000i09l5f7rjb5er
slug: overview-of-java
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1682683657875/eb74dede-afef-4933-b31d-02e8a7a86b5e.png
tags: programming, java

---

Welcome to this series of Java tutorials, where we will be learning and decoding Java from scratch. This is the first article of the series. Check out the entire series here: [https://binarybits.hashnode.dev/series/java](https://binarybits.hashnode.dev/series/java)

## Overview

Java is a programming language that James Gosling developed at Sun Microsystems in the year 1995, which later on was taken into possession by the Oracle Corporation in 2009.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682680576539/243e20a6-d79b-43cd-bf64-1653621035a9.png align="center")

Java is the name of a beautiful island in Indonesia. It is also said that the first coffee was named right here after java coffee. The name was chosen by James Gosling during the daytime when he was enjoying a cup of coffee near his office. Java was initially called by the name: OAK.

However, in the wake of Oak Technologies, the team officially decided to rename it. The options they considered were Silk, Revolutionary, Dynamic, DNA, and Jolt. Even though Silk was further selected, they decided to go along with Java as it was unique, and a lot of people preferred it.

Now the most basic question that must be coming to your mind is: Why should I learn Java? We will come to that question. But, first, let us understand some basic terminologies related to Java.

## Java Development Kit (JDK)

As the name formally states, Java Development Kit is a full-time kit that has a compiler, Java Runtime Environment(JRE), Debuggers, and Java documents included in it. For further execution in Java, we need to have JDK installed on our computers to further lead to the creation, compilation, and running of the Java program.

Here, as we use JDK, we need an environment to run the programs. We use JRE Java Runtime Environment, which provides the least requirements to execute the Java program. It provides the JVM, Core classes, and supporting files.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1682681346906/1a8bfbd1-3466-4b03-a617-3bb1ef7d1d7a.png align="center")

## Java Runtime Environment (JRE)

JDK includes JRE, which, in turn, after installation, allows the Java program to run. But we still can't compile it. It has a browser, the applet supports, and a few plugins included in it. So, to run a Java program on your respective computers, you need JRE.

JRE is made up of multiple elements altogether, and they are:

Java virtual machine (JVM) Java class libraries Java class loader When our software tends to execute a particular program, it requires some environment to run in. Usually, it's any operating system, for example, Unix, Linux, Microsoft Windows, or macOS. Here JRE acts as a translator and facilitator between the Java program and the operating system.

## Java Virtual Machine (JVM)

This generally is referred to as JVM and contains three phases that we have to follow. It is a very important part not only of JDK but also JRE as it is inbuilt in both of the places. When you run a program using the JRE and JDK, it also goes to the JVM as it is required to run the Java program and interprets the program. The phases are as follows:

1. **Compile the Code:** The Java Development Kit(JDK) provides us with the JAVAC compiler to get through this step. We require the JDK to convert our source code into a specific format (compiled code) that can be easily interpreted by the Java Runtime Environment(JRE).
    
2. **Run the Code:** JVM runs the bytecode provided by the compiler. Since Java is a platform-independent language, the compiled code produced by the JAVAC compiler is converted to machine code using platform-specific JVMs. Different platforms have different JVMs. JVMs convert the bytecode into platform-specific machine code.
    

## Garbage Collector

Within Java, the programmers cannot delete the objects. Hence, to delete or recollect a memory, JVM has a Garbage Collector. These Garbage Collectors can recollect those objects which have not been referenced. Using this Java makes the life of a programmer very convenient by managing memory. Despite this, programmers should be aware of what they are writing in their codes or if they are using objects that have already been used for longer. This is because this collector can’t restore the memory of objects that are referenced. Garbage collection here is an automatic process.

![Meme Source: starecat.com](https://images-cdn.9gag.com/photo/aDDDm9w_700b.jpg align="center")

## Why should I learn Java?

Now comes the question: Why should you learn Java? Well... you should learn Java because of the following reasons:

1. **It is platform-independent.** First and foremost, the compiler converts the source code to its bytecode, and later on, JVM executes the bytecode generated by its compiler. Further, this bytecode can be run on any other platform, for example, Windows, Linux, or macOS. This means that we can compile a program on Windows, then we can run it on Linux as well using Linux's JVM.
    
    Every Operating System has different sets of JVM. These different JVMs generate different platform-specific machine codes from the same bytecode. Hence, the output which will appear on all the Operating systems will be the same after the execution of our source code. And, so we call it a Platform Independent language.
    
2. **It is object-oriented.** Object Oriented Programming organizes the software design and logic around classes, objects and data rather than procedures or functions. Object Oriented Programming uses real-world concepts to implement the application code and keep data security and integrity at the center of the design. Let's understand this with the help of a real-life example: We all know that under the Class of Car, we have many options like Alto, WaganR, Santro, etc. In this manner: Each Car object has its specific Model, Colour, Engine power, Top Speed, Year of Manufacture, etc., which altogether are called the properties of the Car Class The functions performed by it, like Start, Stop, Move, etc., are the methods of this Car Class. No memory is allocated on the creation of a class, but we allocate memory when the object is created, which in our case is a new car object.
    
3. **It is simple.** Java is generated in a very convenient manner to be able to understand easily. If you understand the basic OOPs, it is easy to master the art. Moreover, it does not contain any complex features like pointers, multiple inheritances, operator overloading, etc.
    
4. **It is robust.** So the literal meaning of robust can be easily understood as reliable. Java has been developed in such a way that it checks for errors pretty early, which results in errors being detected by the Java compiler, which is pretty difficult when it comes to other programming languages.
    
5. **It is secure.** Java turns out to be very secure, and that is because we do not have access to pointers here. Due to the lack of pointers, we are unable to get access to outbound arrays, and this makes it impossible for the flaws like buffer overflow or stack corruption to occur.
    
6. **It is portable.** Having no implementations and being independent of the aspects of specification make Java Portable. It can be run on any platform as it is completely platform-independent like Windows Linux macOS. This means that if you compile a program on Linux, you can run it on Windows and the other way around.
    
7. **It is architecturally neutral.** This can be seen as one of the best features of Java as it states that a Java program can be easily executed on any processor irrespective of its vendor and architecture. Java application generates a .class file, which corresponds to our applications but contains code in binary format. It provides architecture-neutral ease as bytecode is not dependent on any machine architecture.
    
8. **It is multi-threaded.** Using this feature, it becomes easy for us to write programs that are able enough to perform multiple tasks simultaneously. This comes in handy to developers when they make interactive applications that can run smoothly.
    
9. **It gives high performance.** The Java architecture is designed in such a way that it reduces the overhead when we run an application, and at some times, it uses the JIT(Java In Time) compiler where the compiler easily compiles the code on-demand basics where it only compiles the methods that we call which makes the applications execute faster.
    
10. **It is distributed.** When we use the Java programming language, we get able enough to create distributed applications. RMI(Remote Method Invocation) and EJB(Enterprise Java Beans) help us to create distributed applications. Let’s understand in simple words: The language can easily be distributed onto more than one system which is connected through an internet connection. Objects on one JVM can be easily used to execute the procedures on a remote JVM.
    
11. **It is dynamic.** Java can be easily considered to be more dynamic than the C and C++ programming languages. This can be said by looking at its ability to adapt to an evolving environment. The programs are capable of carrying an extensive amount of run-time information, and this information can be used in the verification of objects during the run-time.
    
12. **It has sandbox execution.** Java programs run in a separate space that allows user to execute their applications without affecting the underlying system with the help of a bytecode verifier. Bytecode verifier also provides additional security as its role is to check the code for any violation of access.
    

Now we have studied enough about Java. Now is the time to code and get our hands dirty. So, see you in the next article where we will be looking at our first Java program.

![LEt's get our hands dirty - A Dirty Job | Make a Meme](https://media.makeameme.org/created/lets-get-our-8ca97fe6d0.jpg align="center")