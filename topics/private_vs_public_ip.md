<h1>Public vs. Private IP Address and Port Forwarding</h1>


These days you might have multiple devices in your local network, so you cannot
assign public IP address to all your devices (phone, tablet, laptop etc.).

A modem is simply a form of interface converter. It handles different 
signalling systems, different low level protocols, and different speeds between
the interface to the ISP that is normally using analogue signals and the digital
interface to the next device. This could be a single PC or a router.

In a home environment, the normal set up has a modem connected to the incoming 
ISP connection, which in turn connects to a NAT router, which connects to your 
devices - PCs, games consoles, phones, tablets, etc. The Network Address Translation
in the router allows all your devices to share the single connection through the modem 
to the ISP. The NAT function replaces the individual devices addresses with the single 
public address for packets going to the Internet and does the reverse replacement when 
responses come back. It may also juggle port numbers if two devices choose the same source
port number when connecting to the same website. This allows the NAT to correctly identify
which device is to receive a response from the site.

Most homes these days have a device called *router*. Router serves multiple purposes:
* Router is the entity that connects you to the Internet (it has a modem)
* Router is the entity that gets a public IP address
* The rest of your network will become an internal network, local area network 

We need addressing system to address entities in the local area network. 

Router is also assigned private IP address so if we want to host a web application on a 
computer that belongs to local network (but is not a router), we need to create port forwarding 
on a router to make sure that all requests coming from the outside are forwarded to appropriate host. 





