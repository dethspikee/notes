<h1>Packet Switching</h1>

In a network application, end systems exchange **messages** with each other. 
Messages can contain anything that the application designer wants. To send a 
message from a source end system to destination end system, the source breaks
long messages into smaller chunks of data known as **packets**. Between source 
and destination, each packet travels through communication links and *packet 
switches* (like routers and link-layer switches). Packets are transmitted over 
each communication link at a rate equal to the *full* transmission rate of the 
link.

If a source end system or a packet switch is sending a packet of *L bits* over 
a link with a transmission rate *R bits/second*, then the time to transmit the 
packet is *L/R* seconds. 

<h2>Store-and-forward Transmission</h2>

Most packet switches use *store-and-forward transmission* at the inputs to the
links. Store-and-forward transmission means that the packet switch must receive
*the entire packet* before it can begin to transmit the first bit of the packet 
onto the outbound link. 

Routers need to receive, store and process the entire packet before forwarding. 

<h2>Queueing Delays and Packet Loss</h2>

Each packet switch has multiple links attached to it. For each attached link,
the packet switch has an **output buffer** (also called output queue), which 
stores packets that the router is about to send into that link. 

If an arriving packet needs to be transmitted onto a link but find the link busy
with the transmission of another packet, the arriving packet must wait in the 
output buffer. Some packets might suffer output buffer **queueing delays**. 
These delays are variable and depend on the level of congestion in the network. 

Since the amount of buffer space is finite, an arriving packet might arrive to 
the full buffer. **Packet loss** will occur - either the arriving packet or one 
of the already queued packets will be dropped. 

<h2>Forwarding Tables and Routing Protocols</h2>

How does the router determine which link it should forward the packet onto? 
Packet forwarding is actually done in different ways in different types of 
computer networks. Let's describe how it is done in the Internet. 

In ther Internet, every end system has an address called an IP address. When a 
source end system wants to send a packet to a destination end system, the source
inludes the destination's IP address in the packet's header. When a packet 
arrives at a router in the network, the router examines a portion of the
packet's destination address and forwards the packet to an adjacent router. More 
specifically, each router has a **forwarding table** that maps destination 
addresses (or portions of the destination addresses) to that router's outbound
link. When a packet arrives at a router, the router examines the address and 
searches its forwarding table, using this destination address, to find 
appropriate outbound link. The router then directs the packet to this outbound 
link. 

Internet has a number of special **routing protocols** that are used to auto-
matically set the forwading tables. A routing protocol may, for example, 
determine the shortest path from each router to each destination and use the 
shortest path results to configure the forwading tables in the routers. 



