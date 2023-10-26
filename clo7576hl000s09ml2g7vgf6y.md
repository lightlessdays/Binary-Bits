---
title: "Basic Networking Commands"
datePublished: Thu Oct 26 2023 12:10:18 GMT+0000 (Coordinated Universal Time)
cuid: clo7576hl000s09ml2g7vgf6y
slug: basic-networking-commands
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698322188628/d4d62079-5b45-460b-8af2-caeae0996d0a.png
tags: networking-commands

---

Hello readers! In this article, I will be talking about four basic networking commands: `ipconfig`, `ping`, `netstat` and `tracert`.

Let us start with `ipconfig`.

### ipconfig

`ipconfig` displays all current TCP/IP network configuration values and refreshes Dynamic Host Configuration Protocol (DHCP) and Domain Name System (DNS) settings. Used without parameters, `ipconfig` displays Internet Protocol version 4 (IPv4) and IPv6 addresses, subnet mask, and default gateway for all adapters.

The `ipconfig` has many uses, as it’s quite a versatile tool. It has basic functions, such as viewing IP (Internet Protocol) address information and troubleshooting network issues, which is helpful for all users. However, it also has more advanced functions for professional use, such as blocking scripts and diagnosing VPN problems.

### ping

Available on almost all operating system platforms, the ping command is used to verify the reachability of a targeted device. It does this by sending an Internet Control Message Protocol (ICMP) echo message to the target; if the target receives the message (and is not configured to drop it), it responds to the initial sender with an ICMP echo reply message. In a perfect world, with no firewalls, and all devices configured to respond to these messages, the ping command would work perfectly. However, many devices (or devices en route, like firewalls) are purposely configured to ignore ICMP echo messages automatically, in order to hide their existence and avoid being targeted by attackers. In these cases, engineers must decide whether the unsuccessful ping is a real problem or a purposeful part of a network’s design.

### traceroute

The `traceroute` command is typically used along with the `ping` command to further determine the reachability of a destination. traceroute works a bit differently from `ping`; instead of simply sending a message to the destination directly, it aims to find the path from the source to the target destination. It does this by using either ICMP echo messages on Windows or the User Datagram Protocol (UDP) probe messages on Linux and Cisco IOS. It figures out the path by taking advantage of the IP Time to Live (TTL) field.

Before we understand what `traceroute` is, I believe we must understand what TTL is.

It’s important to understand what the TTL field does. In normal circumstances, the TTL is used as a loop-prevention mechanism; it works by being set to a number which is then decremented at every respective IP “’hop.” If the TTL reaches a device and is decremented to 0, the packet is dropped and an ICMP “destination unreachable” message is sent back to the source device.

When used by the `traceroute` command, the TTL finds each of the hops in the path between the source and the destination:

1. Initially, the source sends an ICMP or UDP message to the destination with a TTL of 1.
    
2. When the packet reaches the first hop, the TTL is decremented to 0; the device drops the packet and sends back an ICMP “destination unreachable” message.
    
3. To find the second hop, the TTL is set to 2, for the third hop it’s set to 3, and so on; typically three packets are sent for each step toward the destination (three with a TTL set to 1, three with a TTL set to 2, and so on).
    
4. These ICMP “destination unreachable” messages are received by the running traceroute command and interpreted into a readable output showing the path toward the destination.
    

As with the `ping` command, many organizations block the ICMP echo messages and some of the UDP messages; and the output should be read with this fact in mind.

### netstat

`netstat` displays active TCP connections, ports on which the computer is listening, Ethernet statistics, the IP routing table, IPv4 statistics (for the IP, ICMP, TCP, and UDP protocols), and IPv6 statistics (for the IPv6, ICMPv6, TCP over IPv6, and UDP over IPv6 protocols). Used without parameters, this command displays active TCP connections.