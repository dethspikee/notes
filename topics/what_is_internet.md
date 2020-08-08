<h1>What is Internet?</h1>

Internet is a computer network that interconnects billion of computing devices
throughout the world. Devices connected to the Internet are called **hosts**
or **end systems**. 

End systems are connected together by a network or **communication links** 
and **packet switches**. There are many different types of communication
links, which are made up of different physical media, including coaxial 
cable, copper wire, optical fiber and radio spectrum. Different links can 
transmit data at different rates, with a **transmission rate** of a link 
measured in **bits/second**.

When one end system has data to send to another end system, the sending end 
system segments the data and adds header bytes to each segment. The resulting
packages of information called **packets** are then sent through the network 
to the destination end system where they are reassembled into the original data.

A **packet switch** takes a packet arriving at one of its *incoming* 
communication links and forwards that packet on one of its *outgoing*
communication links. Packet switches come in many shapes and flavors, but 
the two most prominent types are **routers** and **link-layer switches**. 

Both types forward the packets toward their ultimate destination. Link-layer 
switches are typically used in *access networks*, while routers are typically 
used in the *network core*. 

The sequence of communication links and packet switches traversed by a packet 
from the sending end system to a receiving end system is known as 
**route** or **path** through the network. 

End systems access the Internet through **Internet Service Providers (ISPs)**,
including residential ISPs such as local cable or telephone companies; 
corporate ISPs; university ISPs; ISPs that provide WiFi access in airports, 
hotels, coffee shops, and other public places; and cellular data ISPs, providing
mobile access to our smartphones and other devices. Each ISP is in itself 
a network of packet switches and communication links. ISPs provide a variety 
of types of network access to the end systems, including residential broadband
access such as *cable modem* or *DSL*, *high-speed local area network access*,
and *mobile wireless acess*. ISPs also provide Internet access to content 
providers, connecting Web sites and video servers directly to the Internet. 
The internet is all about connecting end systems to each other, so the ISPs
that provide access to end systems must also be interconnected. 

Each ISP network, wheter upper-tier or lower-tier, is managed independently,
runs the IP protocal, and conforms to certain naming and address conventions. 


End systems, packet switches, and other pieces of the Internet run **protocols**
that control sending and receiving of information within the Internet.
The **Transmission Control Protocol (TCP)** and the **Internet Protocol (IP)**
are two of the most important protocols in the Internet. The IP protocol 
specifies the format of the packets that are sent and received among routers 
and end systems. The Internet's principal protocols are collectively 
known as **TCP/IP**. 
