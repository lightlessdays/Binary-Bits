---
title: "A Brief Introduction to Subnet Masking"
datePublished: Tue Oct 24 2023 18:19:32 GMT+0000 (Coordinated Universal Time)
cuid: clo4nibdi000009mig0wuam5c
slug: a-brief-introduction-to-subnet-masking
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698171554182/46b994ca-ae1e-46d8-ab09-6350078e2a83.png

---

Consider the example of the telephone. If we want to make a call to someone using a telephone, it is only possible when we know the phone number of the other person. Without knowing the phone number, it is not possible to make a call. In the same way, if we want to send data to any host on the internet, we need the address of the recipient. This allows us to uniquely identify the host on the internet so that the data is transferred and communication is established between that particular host.

IP addresses are of two types - IPv4 and IPv6 addresses. IPv4 is a 32-bit address and IPv6 are 128-bit address. The **'v'** in IPv4 and IPv6 stands for version. The IPv4 address or the Internet Protocol Address is the fourth version of the Internet Protocol. It is a unique address.

The IPv4 address is divided into two parts - the network part and the host part(also referred to as netid and hostid).

IPv4 addresses are 32 bit-addresses and are divided into 4 octets(1 octet = 8 bits). They are usually represented in dotted decimals, but binary representation is another way to represent them.

Example: 192.168.1.152

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698169688010/ec12733d-b39c-4f3b-b844-855a46758c32.png align="center")

The IPv4 address works on the network layer which is responsible for the transmission of data in the form of packets. It is a connectionless protocol. IPv4 uses a 32-bit address space which provides 4,294,967,2964,294,967,296 (2 raised to power 32) unique addresses, but large blocks are reserved for particular networking purposes.

As discussed at the start of the article, there are 2 parts of the IPv4 address- the network part and the host part. The network part is also known as the net id whereas the host part is also known as the host id.

Before we discuss them in-depth, let us first discuss the classes of IPv4 addresses. There are 5 types of classful addressing namely- Class A, Class B, Class C, Class D, and Class E. They are classified based on address space which is divided into a fixed number of blocks and has a fixed number of hosts.

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698170562882/69ffccaf-0e97-43da-a752-26b99cf8c8b6.png align="center")

Here, each class has a fixed number of hostid and netid. Now let us comprehend what the network part and host part means.

**Network part :**  
The network part is also known as net id which is used to classify the network to which the host is connected.

**Host part :**  
The host part is also known as the host id which is the part of the IP address which is used to uniquely identify the host on a network.

IPV4 is divided into five Classes and each class has its use and property

* Class A (0-127)
    
* Class B (128-191)
    
* Class C (192-223)
    
* Class D (224-239)
    
* Class E (240-255)
    

Now, one question strikes our mind: How will we know that this IP address is of which class? The Answer is by seeing their First octet/part if the number lies in between the range it belongs to that class

For Ex- 10.165.192.239 by looking at this IP address the highlighted number 10 is in the first part/octet. Now we must check from the range that 10 lies in which class. The answer is Class A i.e. (0-127).

### Class A

* This Class range lies from 0-127.
    
* This Class is used when we are using default routing (0.0.0.0/0)
    
* This Class is also used for LAN Card testing (127.0.0.0 to 127.255.255.255)
    
* This Class is also used in DHCP Packets.
    
* The private IP range is from 10.0.0.0 to 10.255.255.255(Note- locally we use a private IP address but for internet access, we need a public IP address)
    
* Except that all IPs are for Public IP addresses.
    

### Class B

* This Class range lies from 128-191.
    
* This Class is used for APIPA (Automatic Private IP Addressing) in DHCP (169.254.0.1 to 169.254.255.254)
    
* The private IP range is from 172.16.0.0 to 172.31.255.255.
    
* Except that all IP addresses are Public IP addresses.
    

### Class C

* This Class range lies from 192-223.
    
* This Class has no reserved IP address.
    
* The private IP range is from 192.168.0.0 to 192.168.255.25.
    
* Mostly we use this class of IP address for Communication.
    
* Except that all IP addresses are Public IP addresses.
    

![](https://cdn.hashnode.com/res/hashnode/image/upload/v1698170766891/7510ff38-42db-4d1b-a08a-0bac1fc886ab.png align="center")

### Class D

* This Class range lies from 224-239.
    
* This Class is not used for assigning IP addresses to the devices.
    
* This Class is specially designed for Multicasting purposes.
    

### Class E

* This Class range lies from 240-255.
    
* This whole class is reserved for Scientific purposes and R & D.
    

## Subnet Masking

A subnet mask is a 32-bit number created by setting host bits to all 0s and setting network bits to all 1s. In this way, the subnet mask separates the IP address into the network and host addresses.

The “255” address is always assigned to a broadcast address, and the “0” address is always assigned to a network address. Neither can be assigned to hosts, as they are reserved for these special purposes.

The IP address, subnet mask and gateway or router comprise an underlying structure—the Internet Protocol—that most networks use to facilitate inter-device communication.

When organizations need additional subnetworking, subnetting divides the host element of the IP address further into a subnet. The goal of subnet masks are simply to enable the subnetting process. The phrase “mask” is applied because the subnet mask essentially uses its own 32-bit number to mask the IP address.

Since the internet must accommodate networks of all sizes, an addressing scheme for a range of networks exists based on how the octets in an IP address are broken down. You can determine based on the three high-order or left-most bits in any given IP address which of the five different classes of networks, A to E, the address falls within.

(Class D networks are reserved for multicasting, and Class E networks not used on the internet because they are reserved for research by the Internet Engineering Task Force IETF.)

A Class A subnet mask reflects the network portion in the first octet and leaves octets 2, 3, and 4 for the network manager to divide into hosts and subnets as needed. Class A is for networks with more than 65,536 hosts.

A Class B subnet mask claims the first two octets for the network, leaving the remaining part of the address, the 16 bits of octets 3 and 4, for the subnet and host part. Class B is for networks with 256 to 65,534 hosts.

In a Class C subnet mask, the network portion is the first three octets with the hosts and subnets in just the remaining 8 bits of octet 4. Class C is for smaller networks with fewer than 254 hosts.

Class A, B, and C networks have natural masks or default subnet masks:

* Class A: 255.0.0.0
    
* Class B: 255.255.0.0
    
* Class C: 255.255.255.0
    

You can determine the number and type of IP addresses any given local network requires based on its default subnet mask.

An example of a Class A IP address and subnet mask would be the Class A default submask of 255.0.0.0 and an IP address of 10.20.12.2.

### Class A Subnets

In Class A, only the first octet is used as Network identifier and rest of three octets are used to be assigned to Hosts (i.e. 16777214 Hosts per Network). To make more subnet in Class A, bits from Host part are borrowed and the subnet mask is changed accordingly.

For example, if one MSB (Most Significant Bit) is borrowed from host bits of second octet and added to Network address, it creates two Subnets (2<sup>1</sup>\=2) with (2<sup>23</sup>\-2) 8388606 Hosts per Subnet.

The Subnet mask is changed accordingly to reflect subnetting. Given below is a list of all possible combination of Class A subnets −

![Class A Subnets](https://www.tutorialspoint.com/ipv4/images/class_a_subnets.jpg align="center")

In case of subnetting too, the very first and last IP address of every subnet is used for Subnet Number and Subnet Broadcast IP address respectively. Because these two IP addresses cannot be assigned to hosts, sub-netting cannot be implemented by using more than 30 bits as Network Bits, which provides less than two hosts per subnet.

### Class B Subnets

By default, using Classful Networking, 14 bits are used as Network bits providing (2<sup>14</sup>) 16384 Networks and (2<sup>16</sup>\-2) 65534 Hosts. Class B IP Addresses can be subnetted the same way as Class A addresses, by borrowing bits from Host bits. Below is given all possible combination of Class B subnetting −

![Class B Subnets](https://www.tutorialspoint.com/ipv4/images/class_b_subnets.jpg align="center")

### Class C Subnets

Class C IP addresses are normally assigned to a very small size network because it can only have 254 hosts in a network. Given below is a list of all possible combinations of subnetted Class B IP addresses −

![Class C Subnets](https://www.tutorialspoint.com/ipv4/images/class_c_subnets.jpg align="center")