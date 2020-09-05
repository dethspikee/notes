<h1>Overview of Delay in Packet-Switched Networks</h1>

Recall that a packet starts in a host (the source), passes through a series of 
routers, and ends its journey in another host (the destination). As packet 
travels from one node (host or router) to the subsequent node (host or router)
along this path, the packet suffers from several types of delays at *each* node 
along the path. The most important of of these dalays are:

* Nodal processing delay
* Queuing delay 
* Transmission delay 
* Propagation delay 

Together these delays accumulate to give a **total nodal delay**. 

A packet can be transmitted on a link only if there is no other packet currently
being transmitted on the link and if there are no other packets preceding it in 
the queue (buffer); if the link is currently busy or if there are other packets 
already queued for the link, the newly arrving packet will then join the queue. 

<h2>Processing Delay</h2>

The time required to examine the packet's header and determine where to direct 
the packet is part of the **processing delay**. Processing delay can also
include other factors, such as the time needed to check for bit-level errors.
Processing delays in high-speed routers are typically on the order of micro-
seconds or less. After this nodal processing, the router directs the packet to
the queue that preceds the link to another router. 

<h2>Queuing Delay</h2>

At the queue, the packet experiences **queuing delay** as it waits to be trans-
mitted onto the link. The length of the queuing delay of a specific packet will
depand on the number of earlier-arriving packets that are queued and waiting for 
transmission onto the link. If the queue is empty and no other packet is 
currently being transmitted, then our packet's queuing delay will be zero. 
On the other hand, if the traffic is heavy the queuing delay will be long. 
Queuing delays can be on the order of microseconds to milliseconds in practice. 

<h2>Transmission Delay</h2>

Assuming that packets are transmitted in a first-come-first-served manner, as is
common in packet-switched networks, our packet can be transmitted only after all
the packets that have arrived before it have been transmitted. Denote the length
of the packet by L bits, and denote the transmission rate of the link from 
router A to router B by B bits/sec. The **transmission delay** is *L/R bits*.
This is the amount of time required to push (transit) all of the packet's bits 
into the link.Transmission delays are typically on the order of microseconds to 
milliseconds.

<h2>Propagation Delay</h2>

Once a bit is pushed into the link, it needs to propagate to router B. The time 
required to propagate from the beginning of the link to router B is the 
**propagation delay**. The bit propagates at the propagation speed of the link.
The propagation speed depends on the physical medium of the link. 

<h2>Comparing Transmission and Propagation Delay</h2>

The transmission delay is the amount of time required for the router to push out 
the packet; it is a function of the packet's length and the transmission rate of 
the link, but has nothing to do with the distance between the two routers. The
propagation delay, on the other hand, is the time it takes a bit to propagate 
from one router to the next; it is a function of the distance between two 
routers, but has nothing to do with the packet's length or the transmission rate 
of the link.

<h2>Packet Loss</h2>

In reality a queue (buffer) proceding a link has a finite capacity. 
Packet can arrive to find a full queue, and with no place to store such packet, 
a router will **drop** that packet, that is, the packet will be **lost**. From
an end-system viewpoint, a packet loss will look like a packet having been 
transmitted into the network core but never emerging from the network at the 
destination. A lost packet may be retransmitted on an end-to-end basis in order
to ensure that all data are eventually transferred from source to destination. 

<h2>End System, Application, and Other Delays</h2>

In addition to processing, transmission, and propagation delays, there can be 
additional significant delays in the end systems. 




