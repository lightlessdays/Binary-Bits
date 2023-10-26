---
title: "Basics of Network Address Translation (NAT)"
datePublished: Tue Oct 24 2023 17:41:21 GMT+0000 (Coordinated Universal Time)
cuid: clo4m57sy000208mkaon2cmsg
slug: basics-of-network-address-translation-nat
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698169247719/e0e58fc4-1fe0-4acc-a025-aecffdd32cec.png

---

NAT stands for network address translation. It’s a way to map multiple private addresses inside a local network to a public IP address before transferring the information onto the internet. Whoa! That's a lot of terminology. Let us simplify everything.

Every device on the Internet has an IP address. The IP address serves as the device’s identification – much like how a phone number identifies a particular phone.

When devices communicate on the Internet, they are sending data from their IP address to the IP address of their intended destination.

Sometimes, while data is en route to a destination, the IP addresses used in the communication need to be translated to different IP addresses.

This IP translation is similar to when multiple employees of the same company use their phones (with individual phone numbers) to make outbound phone calls, yet still appear as if they were all using the same company phone number.

The process of translating one IP address to another is known as Network Address Translation or NAT.

Let’s say that there is a laptop connected to a home network using NAT. That network eventually connects to a router that addresses the internet. Suppose that someone uses that laptop to search for directions to their favourite restaurant. The laptop is using NAT. So, it sends this request in an IP packet to the router, which passes that request along to the internet and the search service you’re using. But before your request leaves your home network, the router first changes the internal IP address from a private local IP address to a public IP address. Your router effectively translates the private address you’re using to one that can be used on the internet, and then back again. Now you know that your humble little cable modem or DSL router has a little, automated translator working inside of it.

If the packet keeps a private address, the receiving server won’t know where to send the information back to. This is because a private IP address cannot be routed onto the internet.

## Request for Comments 1918

We all know what a public IP Address is. It is our unique identity in the world of the internet. But what is a private IP Address?

As the internet became more popular years ago, the organization that manages IP addresses, known as the [Internet Assigned Numbers Authority (IANA)](https://www.iana.org/) realized that they needed to do something. So, they created a network address translation scheme. This scheme is described in a document called [Request for Comments (RFC)](https://www.rfc-editor.org/rfc/rfc1918) 1918. This is just one document of thousands that defines how the internet works. If you want to learn about NAT, this is the document that all router manufacturers must implement. No matter what type of NAT you use, you will be using RFC 1918 addresses.

If you were to try to send an RFC 1918 private IP address onto the internet, it would be much like sending a physical piece of mail with the return address of “anonymous,” yet requesting a return service notification. If you were to try doing that with a snail mail service, you would never get that return service notification, because the service wouldn’t be able to tell where “anonymous” even is.

## CISCO's Terminology

Cisco has created some NAT terminology that explicitly refers to the IP addresses and/or ports involved in Network Address Translation (NAT).

While discussing the addresses involved in a NAT, using the terms like “Source” and “Destination” are common. However, using such terms can create some ambiguity.

Specifically, the terms “Source” and “Destination” can create confusion in two cases:

The first case occurs when considering the response traffic — what was the Source in the initial traffic is now the Destination in the response traffic.

The second case occurs when considering the direction of traffic: inbound or outbound. Inbound traffic might need its Destination translated, but the response (outbound) traffic will need its Source *un*translated. Or potentially the exact opposite.

Cisco has designated some NAT terminology that explicitly references a set of addresses with absolute certainty and no ambiguity, that apply to all traffic directions.

* Inside Local
    
* Inside Global
    
* Outside Local
    
* Outside Global
    

These four terms consist of two pairs of two words: *Inside* vs *Outside* and *Local* vs *Global*. Each pair of words refers to unique elements and is best defined in contrast to one another:

* Inside vs Outside refers to the *physical location* of the real owner of the address in question
    
* Local vs Global refers to the *perspective you are viewing the address from*, in relationship to the NAT device
    

![Cisco NAT Terminology - Inside Local, Inside Global, Outside Local, Outside Global](https://www.practicalnetworking.net/wp-content/uploads/2017/10/cisco-terminology.gif align="left")

The attribute 10.1.1.11:3333 refers to a host on the Inside network and is what that host appears as when viewed from the Local perspective. Hence, this is the Inside Local address.

10.1.1.11:3333 will be translated to 73.8.2.11:3333, which still refers to a host that exists on the Inside network, but this time is what that host appears as when viewed from the Global perspective. Hence, this is the Inside Global address.

The attributes 82.6.4.2:80 refers to a host on the Outside network and is what that host appears as when viewed from the Local perspective. Hence, this is the Outside Local address.

82.6.4.2:80 will be translated to 82.6.4.2:80, which still refers to a host that exists on the Outside network, but this time is what that host appears as when viewed from the Global perspective. Hence, this is the Outside Global address.

```plaintext
Trick to Remember: INSIDE addresses are assigned to INSIDE devices and OUTSIDE addresses are assigned to outside devices. Local addresses are accessible only to inside devices. Global addresses are not communicated with inside devices and area accessible only to outside devices.
```

## ISP Migration

ISP migration refers to the process of changing your internet service provider (ISP) while keeping your network and services running smoothly. This typically happens when a company or organization wants to switch from one ISP to another for various reasons, such as better service or cost savings. NAT can ease the process of changing Internet service providers without renumbering internal systems.

One of the drawbacks of CIDR, "Introduction to Border Gateway Protocol 4," is that it can increase the difficulty of changing Internet service providers. If you have been assigned an address block that belongs to ISP1, and you want to change to ISP2, you almost always have to return ISP1's addresses and acquire a new address range from ISP2. This return can mean a painful and costly re-addressing project within your enterprise.

Switching ISPs can be tricky because your network relies on the addresses and connections provided by your current ISP. Here are the main challenges in a simple way:

1. **Address Change:** Each ISP provides a range of IP addresses for your network. When you switch ISPs, you get a new set of addresses. If your internal network uses these old addresses, you need a way to smoothly transition to the new ones without causing disruptions.
    
2. **Routes and Connectivity:** The internet relies on routes to know how to send data from one place to another. When you change ISPs, these routes need to be updated, which can be complex.
    
3. **Keeping Services Online:** If your organization has services that need to be available on the internet, like websites or email servers, they need to keep running without interruption during the ISP change.
    
4. **Possible Downtime:** There's a risk of temporary downtime during the transition, which means your network and services might not be available to your users for a short period.
    

Network Address Translation (NAT) is a helpful tool during ISP migration because it allows you to continue using your old addresses inside your network while presenting a new face to the internet using the addresses provided by the new ISP. This makes the transition smoother because:

* Your internal devices keep using the old addresses.
    
* The NAT device acts as a middleman, translating between your old addresses and new ones for external communication.
    
* This way, your services and connections can continue running without disruptions.
    
* When the migration is complete, your network will use the new ISP's addresses and the old ones will be phased out.
    

In summary, NAT is like a bridge that allows your network to change ISPs without causing major disruptions. It keeps your internal network the same while helping you adapt to new addresses and routes on the internet.

## TCP Load Distribution

TCP Load Distribution is a way to make sure that internet services, like websites or apps, stay responsive and fast even when lots of people are trying to use them at the same time. It's like ensuring there are enough cash registers open in a store during a big sale, so customers don't have to wait in long lines.

Here's how it works, without getting too technical:

1. **Multiple Servers:** Imagine you have several servers (computers) that are all identical and have the same information or services on them. They're like copies of a popular book in a library.
    
2. **People Trying to Access:** Now, picture lots of people trying to access your website or app. They all want to read that popular book in the library.
    
3. **Even Distribution:** TCP Load Distribution makes sure that when someone tries to read the book, they are sent to one of the available servers in a fair way. It's like the library staff guiding readers to different copies of the book so no one copy gets worn out from too much use.
    
4. **Balanced Sharing:** This way, no single server gets overwhelmed with too many requests, and everyone gets to access the service quickly. It's similar to making sure all cash registers in a store have customers, so no one is stuck in a slow line.
    

In actuality, there are four mirrored servers on the inside, and the NAT distributes sessions among them in a round-robin fashion.

This scheme is similar to DNS-based load sharing, in which a single name is resolved round-robin to several IP addresses. The disadvantage of DNS-based load sharing is that when a host receives the name/address resolution, the host caches it. Future sessions are sent to the same address, reducing the effectiveness of the load sharing. NAT-based load sharing performs a translation only when a new TCP connection is opened from the outside, so the sessions are more likely to be distributed evenly. In NAT TCP load balancing, non-TCP packets pass through the NAT untranslated.

It is important to note that NAT-based load balancing, like DNS-based load balancing, is not robust. NAT has no way of knowing when one of the servers goes down, so it continues to translate packets to that address. As a result, a failed or offline server can cause some traffic to the server farm to be black-holed.

So, why use it when it is disadvantageous? Well... it has advantages too... he main advantage is that it keeps the service fast and reliable, even when lots of people are using it. Here's why it's important:

* **Speed:** By spreading the load evenly, it ensures that users don't experience slowdowns or delays.
    
* **Reliability:** If one server has a problem, users can be sent to another one, so the service stays available.
    
* **Efficiency:** It uses the available resources effectively, making the most out of your servers, just like having multiple cash registers open during a sale.
    

In a nutshell, TCP Load Distribution is all about keeping services running smoothly and quickly, even when they're in high demand, by fairly sharing the load across multiple servers.

## Port Address Translation (PAT)

PAT is a clever tool used in NAT (Network Address Translation). So far, we've been talking about many-to-one NAT, where several private addresses are mapped to a single public address. But sometimes, you need a one-to-one mapping, meaning one private address corresponds to one public address.

This is where PAT comes in. Cisco calls it PAT, but others know it as NAPT or IP masquerading. Imagine your internet connection is like a restaurant. Each table at the restaurant represents a private address, and the restaurant's main entrance is a public address. With regular NAT, you'd have several tables sharing the entrance. But with PAT, it's like having many customers at each table, and they can all share the same entrance.

When your computer talks to another device over the internet, it's not just about the IP addresses; it's also about something called sockets. A socket is like a table at a restaurant. It has an IP address (the table) and a port (the chair at the table).

Let's say you're using a Telnet app to chat with your friend. Your computer's private address is 192.168.5.2, and it uses port 23. Your friend's computer is at 172.16.100.6, and their app uses port 1026.

Now, here's where PAT shines. It doesn't just translate the IP address; it also changes the port. So, even if your friend is chatting with you on port 1026, PAT makes it look like they're using port 23. This is like making all the chairs at the restaurant tables look the same, even though each table can have different customers.

In Figure 4-8, you see how PAT works. It's like many customers arriving at the restaurant (NAT) with their own favorite chairs (ports). Some customers are even at the same table but have different chairs. PAT lets them all share the same restaurant entrance (public address) without any confusion.

Thanks to PAT, you can have about 32,000 different "chairs" (ports) at the same "table" (public address). This is super handy for small offices or homes where many devices share one internet connection with just one address. It's like making the most of a single restaurant entrance during a busy dinner rush.

In a nutshell, PAT is like a clever restaurant host who arranges customers at tables, ensuring that even though they're sharing the same entrance, each customer feels like they have their special chair. It's a smart way to make the most of a single internet address, especially for smaller setups.

## Multihomed Autonomous Systems

When an organization, let's call it "the Subscriber," connects to the internet through multiple service providers (ISP1 and ISP2), it encounters challenges, particularly with the addressing system.

1. **Address Misalignment:** The Subscriber is assigned an address space (let's call it 205.113.50.0/23) from ISP1, and it's like having a specific set of keys to access the internet. But these keys are not aligned with the ones provided by ISP2, which is like having two different sets of keys for two gates to the internet.
    
2. **Routing Complications:** To ensure smooth internet communication, both ISP1 and ISP2 must let the world know about the Subscriber's address space (205.113.50.0/23). However, doing this properly can be tricky.
    
3. **Effect on Internet Routing:** This approach makes Internet routing less efficient. It's similar to having too many keys for different locks, and it can clutter the internet's routing tables.
    
4. **Length Limitations:** Some internet infrastructure doesn't handle very long keys (addresses), which could be a problem if your keys (addresses) are too specific.
    

Network Address Translation (NAT) comes to the rescue by addressing these issues:

1. **NAT as the Clever Gatekeeper:** Think of NAT as a gatekeeper who can change your keys (addresses) on the fly. When you approach a gate, NAT translates your keys into the right ones, so you can move seamlessly.
    
2. **Dynamic Key Translation:** In one scenario, NAT ensures your keys are the same, no matter which gate (ISP) you use. However, it secretly translates them to match each gate's requirements, kind of like having a universal remote control for different devices. This keeps your communication smooth and consistent.
    
3. **Master Key Concept:** In another scenario, NAT is even smarter. It doesn't rely on the keys (addresses) given by ISPs. Instead, it provides you with new keys that work for both gates. This is like having a master key for all the gates, which simplifies things.
    
4. **Efficient ISP Switching:** With NAT, switching between ISPs becomes much more manageable. You only need to change your keys (addresses), not the whole system. It streamlines the process and ensures uninterrupted internet connectivity.
    

In technical terms, NAT optimizes multihoming by performing address translation and effectively hiding the addressing complexities from the outside world. This simplifies routing, enhances compatibility, and allows organizations to smoothly switch between multiple service providers while using consistent addressing.

These are the basics of Network Address Translation (NAT).