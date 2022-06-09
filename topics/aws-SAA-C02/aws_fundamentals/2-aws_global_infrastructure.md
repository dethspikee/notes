<h1>AWS global infrastructure</h1>

AWS is a collection of smaller groupings of infrastructure connected together by a global high-speed network. We can take advantage of this to design systems which are resilient of failure and highly available.

We can highlight three concepts in the AWS' infrastructure:
- AWS Region
- AWS Edge location
- AWS Availability zone

AWS Region doesn't directly map to a continent or a country, a region is a creation of AWS, it's an area of the world that they have selected and inside this region is full deployment of aws infrastructure:
- Compute services
- Storage
- DB services
- AI
- Much more

When interacting with most AWS services, you're interacting with that service in a specific region. EC2 service in Ireland is separate from EC2 in Sydney.

You can't have a region in the same town or a city as all of your customers and for this reason AWS also provide Edge locations. Edge locations are much smaller than regions and generally only have content distribution services as well as some types of edge computing but they are located in many more places than regions. Edge locations are useful for companies like Netflix who need to store movies as close to their customers as possible because this allows low latency and high speed distributions.

AWS Regions have three main benefits:
- Each region is separate geograpically if something terrible should happens such as natural disaster then probably one region won't affect other regions.
- Different regions affect different geopolitical separation. 
- Regions give you location control - which allows you to tune your architecture for perfomance you can place the infrastructure as close to your customers as possible, even duplicating your infrastructure to other regions if the demand is there.

AWS Regions aren't the only level of granularity available to us, there are things inside regions:
- Multiple availability zones

With the availability zones you're given isolated infrastructure inside a region. They are isolated compute, storage, networking, power and facilities in a region. A disaster or a outage at one of the region's availability zones would most likely not affect other AZs in that region. If you have a system running in a region with three AZs that uses six virtual services you can spread those services equally across three AZs to increase system's resilience.

AZ is a logical thing inside AWS, AZ could be one data center but it also could be a part of multiple data centers. AWS don't give you visibility of what AZ is, just that it's isolated from other AZs in that region and connected with high speed networking. Services can be placed across AZs to make them resilient.