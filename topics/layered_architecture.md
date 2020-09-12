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

