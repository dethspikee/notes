<h1>Encapsulation</h1>

At the sending host, an **application-layer message** is passed to the trans-
port layer. In the simplest case, the transport layer takes the message and 
appends additional information (so-called transport-layer header information)
that will be used by the receiver-side transport layer. The application-layer 
message and the transport-layer header information together constitute the 
**transport-layer segment**. The transport-layer segment thus **encapsulates**
the application-layer message. The added information might include information
allowing the receiver-side transport layer to deliver the message up to the 
appropriate application, and error detection bits that allow the receiver 
to determine whether bits in the message have been changed in route. 

The transport layer then passes the segment to the network layer, which adds 
network-layer header information such as **source** and **destination** end 
system addresses, creating a **network-layer datagram**. The datagram is then 
passed to the link-layer, which will add its own link-layer header information
and create a **link-layer frame**. Thus, we see that at each layer, a packet has
two types of fields: **header fields** and a **payload field**. The payload is 
typically a packet from the layer above. 

A large message may be divided into multiple transport-layer segments (which 
might themselves each be divided into multiple network-layer datagrams). At the 
receiving end, such a segment must then be reconstructed from its constituent 
datagrams. 