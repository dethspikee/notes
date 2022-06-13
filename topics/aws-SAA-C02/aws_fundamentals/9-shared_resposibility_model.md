<h1>Shared resposibility model</h1>

Shared responsibility model definies which elements you (the customer) manage and which elements AWS manages.

At the high level, aws has a responsibility for security of the cloud. You as a customer has a responsibility for the security IN the cloud.

AWS is responsible for managing security of regions, AZs, edge locations, in other words the security of the hardware used in the global infrastructure. The same holds true for the compute, storage, db and networking which AWS also provide to you. AWS also manages software that sits on top of the hardware mentioned above and is used to provide AWS services.

You accept responsibility for an O/S upwards meaning stuff like:
- Client-side data encryption
- Data integrity
- Authentication
- Server-side encryption
- Networking data protection
- Firewall configuration
- Any customer data