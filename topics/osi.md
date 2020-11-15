<h1>Open Systems Interconnection model</h1>

OSI model consits of 7 different layers. Each layer provides different service. 

So what happens when you type URL address in your browser followed by ENTER? 

LAYER 7 - Application layer 

This is the very first service provided to a client that makes a request to a server, 
for example, GET request if HTTP. This request (also known as message) contains headers 
such as cookies, content-type etc. and is turned into a long string. 

LAYER 6 - Presentation layer 

If you use HTTPS for example then this layer will encrypt the string provided by the Application
layer. 

LAYER 5 - Session layer

As multiple TCP (connection based) connections at the same time can be opened we need a way to 
distinguish them. We can use session layer to tag each individual message with unique session ID.

LAYER 4 - Transport layer 

This is where the message from above layers is broken into smaller segments. Each segment is tagged
with important information such as destination and source port numbers. We use destination ports
to allow segments to be delivered to correct application. We use source port numbers to be sure 
that they're returned to the correct application. 

LAYER 3 - Network layer 

This layer takes the segment from the layer above and turns it into a packet. It then attaches 2 
pieces of important information to it. Destination and source IP addresses. This layer transfers 
packets to the machine with the same IP address as the one in the destination IP address header.


LAYER 2 - Data link 

Each packet from the layer above is passed into this layer. This layer breaks down those packets
even further and it adds another headers. Target and source MAC addresses. This is now called frames.
Sometimes you don't know the MAC address, but the ARP protocol can solve this problem. 

LAYER 1 - Physical 

Electric or light signals etc. can now be used to transfer our frames 0s and 1s across the network. 


