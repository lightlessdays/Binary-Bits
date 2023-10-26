---
title: "What is Routing?"
datePublished: Thu Oct 26 2023 12:34:48 GMT+0000 (Coordinated Universal Time)
cuid: clo762oti000109jv6wn9bi0t
slug: what-is-routing
cover: https://cdn.hashnode.com/res/hashnode/image/upload/v1698323661993/8a87cf9a-d89d-40d4-a9c2-2551da9e35fc.png

---

Routers are devices designed to manage and control the flow of data within computer networks. They act as traffic directors, making sure that data packets (small units of data) are sent to the right destination. Routers examine the destination address of data packets and decide where to send them next. They connect different networks together, like your home network to the internet, and help data navigate this interconnected web.

Routing is the process of directing data from one place to another within a network or between different networks. It's like planning the best path for information to travel from its source to its destination. In simple terms, routing is like a GPS system for data, determining the most efficient route for it to follow.

There are two methods of determining path of data, or we can say that there are two kinds of routing:

1. Static Routing
    
2. Dynamic Routing
    

### Static Routing

Static routing is a method where network administrators manually configure routing information into routers. These routers use predetermined paths for forwarding data packets. In other words, the routes are set and do not adapt or change unless manually adjusted by an administrator.

**Advantages:**

* **Simplicity**: Static routing is straightforward to set up and understand. You define the routes, and the router follows them.
    
* **Predictability**: Since routes are manually configured, there are no surprises. Network behavior is consistent and stable.
    
* **Lower Overhead**: Static routing consumes less processing power and bandwidth because there's no need for routers to exchange routing information.
    

**Disadvantages:**

* **Lack of Adaptability**: Static routes don't adjust to network changes. If there's a failure or a change in network topology, it won't be automatically accommodated.
    
* **Maintenance Intensive**: Keeping static routes up-to-date can be time-consuming, especially in large or dynamic networks.
    
* **Not Suitable for Large Networks**: In extensive networks, configuring and managing numerous static routes can become impractical.
    

### Dynamic Routing

Dynamic routing relies on routing protocols to automatically exchange information among routers. These protocols allow routers to learn about network changes and adapt their routing tables accordingly.

**Advantages:**

* **Adaptability**: Dynamic routing responds to network changes, such as link failures or the addition of new routes, without manual intervention.
    
* **Scalability**: Dynamic routing is more practical in larger networks, as it reduces the administrative burden of configuring and maintaining routes.
    
* **Efficiency**: It optimizes the network by choosing the best path based on real-time conditions.
    

**Disadvantages:**

* **Complexity**: Dynamic routing protocols can be complex, and understanding their behavior may require specialized knowledge.
    
* **Resource Intensive**: Dynamic routing protocols consume more processing power, memory, and bandwidth compared to static routing, which can be a concern in smaller or resource-constrained networks.
    
* **Security Risks**: If not configured correctly, dynamic routing can expose the network to security vulnerabilities.
    

### Differences between Dynamic and Static Routing

| **Dynamic Routing** | Static Routing |
| --- | --- |
| Configuration Complexity is generally independent of the network size | Configuration Complexity increases with the network size |
| Automatically adapts to topology changes | Administrator intervention required |
| Less secure | More secure; as they are not advertised over the network |
| The route depends on the current topology | Route to destination is always the same |
| Uses CPU, memory, and link bandwidth to calculate and communicate routes. | No extra resources are needed. |