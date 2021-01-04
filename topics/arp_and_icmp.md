<h1>ARP and ICMP</h1>

<h2>Default Gateway</h2>

Every host in every network has at least two settings (IP address and network
mask). Every host also has a "default gateway". Default gateway is a device
that acts as a gateway to Internet for devices located in the local network. 
Default router is used for connections to other networks. All packets meant 
for other networks are routed through default gateway router.

<h2>ARP Protocol</h2>

Address resolution protocol:

1) Network layer protocol
2) Doesn't have IPv3 header
3) Resolves destination IP address to destination MAC address
4) ARP request from the source host is sent to broadcast MAC address
5) ARP response is sent unicast from destination host with target IP address to
   the source host

<h2>How packets are sent to remote hosts</h2>

Computer will not send ARP request for a host located in different network.
Computer will use the network mask and apply it to its own IP address, find out
the network prefix then do the same again to destination IP address and it will
find out that the network prefix is different. That means that the host is in
different network. 

Now, without any ARP request, computer will send a packet to default gateway.
On a data-link layer in a destination MAC address it will add MAC address of
LAN interface of default gateway.

<h2>ICMP Protocol</h2>

Internet Control Message Protocol used for connection verification and error
detection protocol
