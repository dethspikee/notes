<h1>VPC</h1>

VPC is a service to create private networks inside AWS. VPCs are also used to connect your AWS private networks to your on-premises networks to create hybrid environment.

VPCs are regional services meaning they are regional resilient. VPCs operate from multiple AZs in a specific AWS region.

VPC by default is private and isolated from other VPCs, AWS public zone and public internet. You can of course configure it otherwise.

There are two types of VPCs available in the region:
- Default VPCs max. 1 per region
- Custom VPC many per region

VPCs are created within AWS region. A region can have multiple custom VPCs and unless configured otherwise they cannot communicate with each other. VPCs are regionally resilient.

Every VPC is allocated a range of IP addresses called the VPC CIDR. CIDR defines start and end range of IP addresses that VPC can use. Everything inside a VPC uses CIDR range of that VPC. Custom VPCs can have multiple CIDR ranges but the default VPC only gets one and is always the same - 172.31.0.0/16

The way VPC provides resilience is that it can be divided into subnets across AZs of the region.

Default VPC facts:
- Only one per region
- Always the same CIDR range
- Subnet is created in each AZ in the region
- Comes with few things pre-configured such as IGW (Internet Gateway), security group and NACL
- By default anything placed in the default VPC subnets is assigned a public IPv4 IP address