Network Routing is the process of selecting path across one more networks. A Computer network consists of several systems, called **Network nodes**, and paths or links that connect these nodes. In an interconnected network, communication between two nodes can take place over multiple paths. Routing is the process of selecting the **best** path using predetermined rules.
![](https://cf-assets.www.cloudflare.com/slt3lc6tev37/5biqo5wm6nM8GSmiNyiAnl/b6b5c9befeda6ba99b4380d84953de18/routing-diagram.svg)
# Why is routing important?
Routing increases the efficiency of network communication. Network communication failures can cause users to wait longer for website pages to load. Web site servers can also be unable to handle large numbers of users, resulting in server outages. Routing minimizes network failures by managing data traffic so that the network can use as much capacity as possible without congestion.
# How work routing?
In routing, data send as packet. All of packet has header that include destination address. When a data packet arrives, the [[Router]] first looks for its address in the routing table.

For example, when you visit a website on a computer on an office network, the data packet first moves to the office network router. The router queries the header packet and determines the destination of the packet. It then queries the internal table and forwards the packet to the next router or to another device, such as a printer, within the network itself.
# What are the routing types?
Routing is divided into two types, depending on how the router creates the routing table.
### Static Routing
In static routing, network administrators use static tables to manually configure and select network paths. Static routing is useful when network designs or parameters are expected to remain constant.

In this routing technique, static characteristics can lead to disadvantages such as network congestion. Although administrators can also configure alternative routes in case a link fails, static routing usually limits network performance by reducing the adaptability and flexibility of the network.
### Dynamic routing
In dynamic routing, routers create and update routing tables at runtime based on actual network conditions. They attempt to find the fastest source-to-destination route by using dynamic routing protocols, which are a set of rules that create, maintain, and update dynamic routing tables.

Dynamic routing can address changing network conditions such as traffic volume, bandwidth, and network failure.
# Routing Protocols
Routing protocol is a rule that defines how data packets can be routed to a destination via the most efficient route on the network.
### Internal Gateway Protocol
Internal gateway protocols work most efficiently in autonomous systems, which are networks controlled by administrators in a single organization.
#### Routing Information Protocol (RIP)
Routing Information Protocol (RIP) determines the shortest path between networks based on the number of **hops(how many other routers go through)**. RIP is a legacy protocol that is not currently in use because it is not suitable for large-scale network implementations.
#### Open Shortest Path First (OSPF)
It collects information from all other routers in the autonomous system to identify the shortest and fastest path to the destination of the data packet.
### External Gateway Protocol
External gateway protocols are better suited for managing the transmission of information between two autonomous systems.
#### Border Gateway Protocol (BGP)
BGP defines communication over the Internet. The Internet is a collection of large autonomous systems that are all connected to one another. All autonomous systems have Autonomous System Numbers (ASN) that are assigned by registering with the Internet Assigned Numbers Authority.

---
Reference link 🙂     
https://aws.amazon.com/what-is/routing/
https://www.cloudflare.com/learning/network-layer/what-is-routing/