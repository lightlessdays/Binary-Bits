---
title: "Concept of Page Replacement"
datePublished: Wed May 03 2023 08:30:41 GMT+0000 (Coordinated Universal Time)
cuid: clh7futv9001v09mnh7jg0b8x
slug: concept-of-page-replacement
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1683102610851/2da81c1a-6e3b-4320-a33f-7a30d14822ed.png
tags: operating-system

---

Page replacement is needed in operating systems that use virtual memory using Demand Paging. As we know that in Demand paging, only a set of pages of a process is loaded into the memory. This is done so that we can have more processes in the memory at the same time.

When a page that is residing in virtual memory is requested by a process for its execution, the Operating System needs to decide which page will be replaced by this requested page. This process is known as page replacement and is a vital component in virtual memory management.

## Need for Page Replacement

A Page Fault occurs when a program running in the CPU tries to access a page that is in the address space of that program, but the requested page is currently not loaded into the main physical memory, the RAM of the system.

Since the actual RAM is much less than the virtual memory the page faults occur. So whenever a page fault occurs, the Operating system has to replace an existing page in RAM with the newly requested page. In this scenario, page replacement algorithms help the Operating System in deciding which page to replace. The primary objective of all the page replacement algorithms is to minimize the number of page faults.

## What is a Page Replacement Algorithm?

Page Replacement Algorithms decide which page to remove, also called swap out when a new page needs to be loaded into the main memory. Page Replacement happens when a requested page is not present in the main memory and the available space is not sufficient for allocation to the requested page.

When the page that was selected for replacement was paged out, and referenced again, it has to read in from the disk, and this requires I/O completion. This process determines the quality of the page replacement algorithm: the lesser time waiting for page-ins, the better the algorithm.

A page replacement algorithm tries to select which pages should be replaced to minimize the total number of page misses. There are many different page replacement algorithms. These algorithms are evaluated by running them on a particular string of memory references and computing the number of page faults. The fewer page faults the better the algorithm for that situation.

## First In First Out (FIFO) Algorithm

This is the simplest page replacement algorithm. In this algorithm, the OS maintains a queue that keeps track of all the memory pages, with the oldest page at the front and the most recent page at the back.

When there is a need for page replacement, the FIFO algorithm, swaps out the page at the front of the queue, that is the page which has been in the memory for the longest time.

For example:

Consider the page reference string of size 12: 1, 2, 3, 4, 5, 1, 3, 1, 6, 3, 2, 3 with frame size 4(i.e. maximum 4 pages in a frame).

![](https://afteracademy.com/images/what-are-the-page-replacement-algorithms-fifo-bbf705290d1e6776.jpg align="left")

**Total Page Fault = 9**

* Initially, all 4 slots are empty, so when 1, 2, 3, and 4 came they are allocated to the empty slots in order of their arrival. This is page fault as 1, 2, 3, and 4 are not available in memory.
    
* When 5 comes, it is not available in memory so page fault occurs and it replaces the oldest page in memory, i.e., 1.
    
* When 1 comes, it is not available in memory so page fault occurs and it replaces the oldest page in memory, i.e., 2.
    
* When 3,1 comes, it is available in the memory, i.e., Page Hit, so no replacement occurs.
    
* When 6 comes, it is not available in memory so page fault occurs and it replaces the oldest page in memory, i.e., 3.
    
* When 3 comes, it is not available in memory so page fault occurs and it replaces the oldest page in memory, i.e., 4.
    
* When 2 comes, it is not available in memory so page fault occurs and it replaces the oldest page in memory, i.e., 5.
    
* When 3 comes, it is available in the memory, i.e., Page Hit, so no replacement occurs.
    

**Page Fault ratio = 9/12 i.e. total miss/total possible cases**

### Advantages of the FIFO Algorithm

* Simple and easy to implement.
    
* Low overhead.
    

### Disadvantages of the FIFO Algorithm

* Poor performance.
    
* Doesn’t consider the frequency of use or last used time, simply replaces the oldest page.
    
* Suffers from Belady’s Anomaly(i.e. more page faults when we increase the number of page frames).
    

## Least Recently Used (LRU) Algorithm

east Recently Used page replacement algorithm keeps track of page usage over a short period. It works on the idea that the pages that have been most heavily used in the past are most likely to be used heavily in the future too.

In LRU, whenever page replacement happens, the page which has not been used for the longest amount of time is replaced.

For example:

![](https://afteracademy.com/images/what-are-the-page-replacement-algorithms-lru-0e258594b2dec232.jpg align="left")

**Total Page Fault = 8**

Initially, all 4 slots are empty, so when 1, 2, 3, and 4 came they are allocated to the empty slots in order of their arrival. This is page fault as 1, 2, 3, and 4 are not available in memory.

* When 5 comes, it is not available in memory so page fault occurs and it replaces 1 which is the least recently used page.
    
* When 1 comes, it is not available in memory so page fault occurs and it replaces 2.
    
* When 3,1 comes, it is available in the memory, i.e., Page Hit, so no replacement occurs.
    
* When 6 comes, it is not available in memory so page fault occurs and it replaces 4.
    
* When 3 comes, it is available in the memory, i.e., Page Hit, so no replacement occurs.
    
* When 2 comes, it is not available in memory so page fault occurs and it replaces 5.
    
* When 3 comes, it is available in the memory, i.e., Page Hit, so no replacement occurs.
    

**Page Fault ratio = 8/12**

### Advantages of the LRU Algorithm

* Efficient.
    
* Doesn't suffer from Belady’s Anomaly.
    

### Disadvantages of the LRU Algorithm

* Complex Implementation.
    
* Expensive.
    
* Requires hardware support.
    

## **Optimal Page Replacement Algorithm**

The optimal Page Replacement algorithm is the best page replacement algorithm as it gives the least number of page faults. It is also known as OPT, clairvoyant replacement algorithm, or Belady’s optimal page replacement policy.

In this algorithm, pages are replaced which would not be used for the longest duration of time in the future, i.e., the pages in the memory which are going to be referred farthest in the future are replaced.

This algorithm was introduced long back and is difficult to implement because it requires future knowledge of the program's behaviour. However, it is possible to implement optimal page replacement on the second run by using the page reference information collected on the first run.

For example:

![](https://afteracademy.com/images/what-are-the-page-replacement-algorithms-optimal-8e02fc8a1f4517de.jpg align="left")

**Total Page Fault = 6**

Initially, all 4 slots are empty, so when 1, 2, 3, and 4 came they are allocated to the empty slots in order of their arrival. This is page fault as 1, 2, 3, and 4 are not available in memory.

* When 5 comes, it is not available in memory so page fault occurs and it replaces 4 which is going to be used farthest in the future among 1, 2, 3, 4.
    
* When 1,3,1 comes, they are available in the memory, i.e., Page Hit, so no replacement occurs.
    
* When 6 comes, it is not available in memory so page fault occurs and it replaces 1.
    
* When 3, 2, 3 comes, it is available in the memory, i.e., Page Hit, so no replacement occurs.
    

**Page Fault ratio = 6/12**

### Advantages of Optimal Page Replacement Algorithm

* Easy to Implement.
    
* Simple data structures are used.
    
* Highly efficient.
    

### Disadvantages of Optimal Page Replacement Algorithm

* Requires future knowledge of the program.
    
* Time-consuming.
    

So, these are some of the page replacement algorithms that are used in paging. Hope you learned something new today. :)