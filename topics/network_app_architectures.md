<h1>Network Application Architectures</h1>

Application architecture is distinctly different from the network architecture.
From the application developer's perspective, the network architecture is fixed 
and provides a specific set of services to applications. The **application 
architecture**, on the other hand, is designed by the application developer 
and dictates how the application is structured over the various end systems.

Two predominant architectural paradigms are used in modern network applications:
* client-server architecture
* peer-to-peer (P2P) architecture 

In **client-server** there is an always-on host, called the *server*, which 
services requests from many other hosts, called *clients*. 

In a **P2P architecture**, there is minimal (or no) reliance on dedicated 
servers. Instead the application exploits direct communication between pairs of 
intermittently connected hosts, called *peers*. One of the most compelling 
features of P2P architectures is their **self-scalability**. For example, in a
P2P file-sharing application, each peer adds service capacity to the system by 
distributing files to other peers. 

