<h1>DNS Fundamentals</h1>

DNS is a discovery service. It's how systems are discovered on the internet and often in private networks. It translates information which machines need to and from informations which humans need.

DNS database is huge and has to be distributed and resilient.

Important terms:

1) DNS client - refers to the device which wants the data that DNS has, for example IP address of amazon.co.uk. It's usually a piece of software running in the OS of the device you use.
2) DNS Resolver - that could be a piece of software running also on the dns client (your laptop, pc, tablet) or it could be separate server running inside your internet router or a physical server running inside your internet provider. It's the DNS resolver that queries the DNS system on your behalf. So the DNS client talks to DNS resolver and asks the DNS resolver to query DNS on its behalf.
3) DNS Zone - part of the global DNS data e.g. amazon.com.
4) Zonefile - is how the data for that zone is physically stored.
5) DNS Nameserver - this is the server which hosts these zonefiles.

So DNS resolver service needs to locate the correct nameserver for the given zone, query that nameserver, retrieve the information it needs and then pass it back to DNS client.

DNS is distributed, the data is stored in zonefiles and zonefiles are stored on nameserver gloabally. DNS has to have starting point. That starting point is called DNS Root.

DNS root is hosted on 13 special nameservers known as root servers. The root servers are operated by 12 different large global organizations. These organizations only manage the root servers not the root zone database. Each root server can be a cluster of servers distributed globally by it's represented by one entity each of which has a letter. These servers are an entry point. We need to understand how our laptops can find these servers.

Generally your laptop will use DNS resolver server that's usually located within your internet router or internet provider. The vendor of your OS (Microsoft, Linux etc.) supply what's known as the Root hints. Those root hints files are essentially just a list of these root servers.

Root zone is managed by IANA.

