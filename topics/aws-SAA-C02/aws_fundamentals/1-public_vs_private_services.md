<h1>Private and Public services</h1>

A public service can be accessed via public endpoints such as simple storage service (s3). Private aws service runs within VPC, only things within that VPC or what is connected to that VPC can access the service.

For both of these there are permissions and networking, so even though S3 is a public service by default an identity other than account root user has no authorization to access that resource.

There are three different network zones:

Public Internet | Aws public zone (services such as S3) | Aws private zone (services running inside VPCs)

On-premises networks can access VPCs only if configured via VPN or Direct connect.

You can attach internet gateway between aws public and private zones. It allows extra functionality:
- It allows private zone resources to access public internet as long as private service has allocated public IP address. It can also access public aws services such as S3. Remember that data exchanged between private aws service and public aws service doesn't touch the public internet.