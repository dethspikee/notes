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
output buffer. 

