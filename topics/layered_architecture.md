<h1>Layered Architecture</h1>

A layered architecture allows us to discuss a well-define, specific part of a 
large and complex system, making it much easier to change the implementation 
of the service provided by the layer. As long as the layer provides the same 
service to the layer above it, and uses the same services from the layer below
it, the remainder of the system remains unchanged when a layer's implementation
is changed. 

Changing the implementation of a service is very different from changing the 
service itself!

Each layer provides its service by (1) performing certain actions within that 
layer and by (2) using the services of the layer directly below it. 

<h2>Protocol Layering</h2>

Network designers organize protocols - and the network hardware and software 
that implement the protocols - in **layers**. Each protocol belongs to one of 
the layers. We are interested in the **services** that a layer offers to the 
layer above - the so-called **service model** of a layer. 

For example, the services provided by layer *n* may include reliable delivery 
of messages from one edge of the network to the other. This might be implemented
by using an unreliable edge-to-edge message delivery service of layer *n - 1*, 
and adding layer *n* functionality to detect and retransmit lost messages. 

A protocol layer can be implemented in software, in hardware, or in a combina-
tion of the two. 

Application-layer protocols - such as HTTP and SMTP - are almost always imple-
mented in software in the end systems; so are transport-layer protocols. 

<h2>Application Layer</h2>

The application layer is where network applications and their application-layer
protocols reside. 

Application layer includes many protocols, such as:

* HTTP provides Web document request and transfer 
* SMTP provides transfer of e-mail messages 
* FTP provides transfer of files between two end system 

Translation of human friendly internet addresses to 32-bit network addresses is 
also done with a help of application layer protocol DNS.

Application-layer protocol is distributed over multiple end systems, with the 
application in one end system using the protocol to exchange packets of infor-
mation with the application in another end-system. We refer to this packet of 
information at the application layer as a **message**. 

<h2>Transport Layer</h2>

The Internet's transport layer transports application-layer messages between 
application endpoints. In the Internet there are two transport protocols, 
*UDP* and *TCP*, either of which can transport application-layer messages. 

TCP provides a connection-oriented service to its applications. This service 
includes guaranteed delivery of application-layer messages to the destination 
and flow control (that is, sender/receiver speed matching). TCP also breaks 
longer messages into shorter segments and provides a congestion-control 
mechanism, so that a source throttles its transmission rate when the network is 
congested. The UDP protocol provides a connectionless service to its appli-
cations. It also provides no reliability, no flow control, and no congestion 
control. We will refer to a transport-layer packet as **segment**.

<h2>Network Layer</h2>

The Internet's network layer is responsible for moving network-layer packets 
known as **datagrams** from one host to another. The Internet transport-layer 
protocol (TCP or UDP) in a source host passes a transport-layer segment and a 
destination address to the network layer. The network layer then provides the 
service of delivering the segment to the transport layer in the destination host

The Internet's network layer includes the IP protocol, which defines the fields 
in the datagram as well as how the end systems and routers act on these fields.
There is only one IP protocol, and all Internet components that have a network
layer must run the IP protocol. The Internet's network layer also contains 
routing protocols that determine the routes that datagrams take between sources 
and destinations. The Internet has many routing protocols. 

<h2>Link Layer</h2>

The Internet's network layer routes a datagram through a series of routers 
between the source and destination. To move a packet from one node (host or 
router) to the next node in the route, the network layer relies on the services 
of the link layer. In particular, at each node, the network layer passes the 
datagram down to the link layer, which delivers the datagram to the next node 
along the route. 

