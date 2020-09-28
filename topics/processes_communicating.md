<h1>Processes Communicating</h1>

How does the programs, running on multiple end systems, communicate with each 
other? 

It's not actually programs but **processes** that communicate with each other. 
A process can be thought of as a program that is running within an end system. 
Processes on two different end systems communicate with each other by exchanging
**messages** across the computer network. A sending process creates and sends 
messages into the network; a receiving process receives these messages and 
possibly responds by sending messages back. Processes reside in the application
layer of the five-layer protocol stack. 

<h2>Client and Server processes</h2>

A network application consists of pairs of processes that send messages to each 
other over a network. For example, in the Web application a client browser 
process exchanges messages with a Web server process. In a P2P, a file is 
transferred from a process in one peer to a process in another peer. 
For each pair of communicating processes, we typically label one of the two  
processes as the **client** and the other process as the **server**. We define
the client and server processes as follows:

*In the context of a communication session between a pair of processes, the 
process that initiates the communication is labeled as the client. The process
that waits to be contacted to begin the session is the server.*

<h2>The Interface Between the Process and the Computer Network</h2>

Any message sent from one process to another must go through the underlying 
network. A process sends messages into, and receives messages from, the network
through a software interface called a **socket**. A process is analogous to a 
house and its socket is analogous to its door. When a process wants to send a 
message to another process on another host, it shoves the message out its door
(socket). Once the message arrives at the destination host, the message passes 
through the receiving process' door (socket), and the receiving process then 
acts on the message. 

A socket is the interface between the application layer and the transport layer 
within a host. It is also referred to as the **Application Programming Interface
(API)** between the application and the network. The application developer has 
control of everything on the application-layer side of the socket but has little 
control of the transport-layer side of the socket. The only control that the 
application developer has on the transport-layer side is (1) the choice of 
transport protocol and (2) perhaps the ability to fix a few transport-layer 
parameters such as maximum buffer and maximum segment sizes. 


</h2>Addressing Processes</h2>

In order for a process running on one host to send packets to a process running 
on another host, the receiving process needs to have an address. To identify 
receiving process, two pieces of information need to be specified: (1) the 
address of the host and (2) an identifier that specifies the receiving process
in the destination host. In the Internet, the host is identified by its 
**IP Address**. In addition to knowing the address of the host to which a 
message is destined, the sending process must also identify the receiving pro-
cess (more detailed, the receiving socket) running in the host. This is import-
ant because a host could be running many network applications. A destination 
**port number** serves this purpose. Popular applications have been assigned 
specific port numbers:

* Port 80 - web server 
* Port 25 - mail server process 