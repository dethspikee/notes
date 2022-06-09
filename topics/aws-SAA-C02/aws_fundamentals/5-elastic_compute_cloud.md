<h1>EC2 and AMI</h2>

EC2 service provides access to virtual machines known as "instances". If you need to deploy any form of compute which require operating system, runtime environment, db dependencies, application and if you need to manage all of them then EC2 is the service to do that from.

EC2 Key facts & features:
- IAAS - provides virtual machines -> instances
- Private AWS service by-default launched into one of the VPC subnets
- If you need public access to EC2 instance you need to configure parent VPC network to allow that
- EC2 is launched into one of the subnets of the VPC meaning it's AZ resilient. If the AZ that an instance is launched into fails then the instance itself will likely fail
- When you launch EC2 instance you can choose from various sizes and capabilities for that instances. Those choices influence resources that the instance gets as well as any extra capabilities such as CPU use, more advanced storage etc. You can change some of this afterwards as well.

EC2 offers on-demand billing either by the second or by the hour depending on the software that is launched in an instance.

There are few components to an instance charge:
- Charge for running an instance (cpu and memory usage)
- Charge for the storage that the instance uses
- Extras for any commercial software that the instance is launched with

Instances can use number of different types of storage, two popular choices being:
- local on-host storage
- another AWS service called Elastic Block Store (EBS)

EC2 instance can be in one of the few states:
- Running
- Stopped
- Terminated

Instance termination is non-reversable action.

Those states are important because they influence charges. At the high level EC2 instance is composed of CPU, memory, disk and networking. When an instance is in running state you're being charged for all four of these categories. When instance is stopped it means no CPU, memory and networking resources are being used meaning you're not being charged for CPU, memory and networking usage, however, storage is still allocated to the instance and it's still being used even when in stopped state. To stop being charged you need to terminate your EC2 instance.

Amazon machine image is an image of an EC2 instance. AMI can be used to create EC2 instance or AMI can be created from EC2 instance.

AMI contains few importants things:
- Attached permissions these control which accounts can or can't use AMI. AMI can be set as public meaning everyone can launch instances from it. AMI can be set as "owner" meaning only owner of an AMI can launch EC2 instances from it. Finally you can add explicit permissions to that AMI where the owner grants access for specific AWS accounts.
- Root volume of an instance (C drive in windows or root volume in Linux.) drive that boots the OS
- Block device mapping this is a configuration which links the volumes that the AMI has and how they're presented to the OS. It determines which volume is a boot volume and which volume is a data volume.

You connect to EC2 instances running Windows distribution using RDP protocol running on port 3389. With Linux instances it uses SSH protocol which uses port 22.
