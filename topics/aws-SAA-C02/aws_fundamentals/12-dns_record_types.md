1) Nameserver (NS) - these records allow delegation to occur in DNS
2) A and AAAA records - map host names to IP addresses (A to IPv4 and AAAA to IPv6)
3) Cname (Canonical name) - let's you create shortcuts maps host to host names. As an example you can point 3 CName records (FTP, mail, wwww) to a single A record and in that way you can point 3 different host name to a single IP address
4) MX Records - used by email servers. MX records have two values, priority and value. Lower the value for the priority, higher the priority
5) TXT record - allows to add arbitrary text to records. A system that holds our email may ask us to add TXT record to the domain containing random text so the ownership of that domain can be verified


TTL - numeric value in seconds used on records to specify how long records can be cached for
