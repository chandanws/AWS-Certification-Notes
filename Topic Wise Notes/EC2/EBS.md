# EBS ([FAQs](https://aws.amazon.com/ebs/faqs/))

## What is it?
Amazon EBS allows you to create storage volumes and attach them to Amazon EC2 instances. Once attached, you can create a file system on top of these volumes, run a database, or use them in any other way you should use a block device. Amazon EBS volumes are placed in a specific availability zone, where they are automatically replicated to protect you from the failure of a single component.

## EBS Volume Types
1. **General Purpose SSD(GP2)**
	- General purpose, balances both price & performance
	- Ratio of 3 IOPS per GB with up to 10,000 IOPS and the ability to burst up to 3000 IOPS for extended periods of time for volumes at 3334 GiB and above.
2. **Provision IOPS SSD(IO1)**
	- Designed for I/O intensive applications such as large relational or NoSQL databases.
	- Use if you need more than 10,000 IOPS
	- Can provision up to 20,000 IOPS per volume
3. **Throughput Optimized HDD(ST1)**
	- Frequently accessed workloads
	- Big Data
	- Data Warehouse
	- Log Processing
	- Cannot be a boot volume
4. **Cold HDD(SC1)**
	- Less frequently accessed data
	- Lowest Cost Storage for infrequently accessed workloads
	- File Server
	- Cannot be a boot volume
5. **Magnetic(Standard)**
	- Lowest cost per gigabyte of all EBS volume types that is bootable. 
	- Magnetic volumes are ideal for workloads where data is accessed infrequently, and applications where the lowest storage cost is important. 

**You cannot mount 1 EBS volume to multiple EC2 instances, instead use EFS**

## Upgrading EBS Volume Types
 - To move an EBS volume from 1 availability zone to another, you would have to create a snapshot first and then create another EBS volume using that snapshot.
 - Snapshots exist on S3
 - Volume exist on EBS
 - Snapshots are point in time copies of Volumes.
 - Snapshots are incremental - this means that only the blocks that have changed since your last snapshot are moved to S3
 - To create a snapshot for Amazon EBS volumes that serve as root devices, you should stop the instance before taking the snapshot.
 - However you can take a snap while the instance is running
 - You can create AMIs from both Volumes and Snapshots
 - You can change EBS volumes on the fly, including changing the size and storage type.
 - Volumes will always be in the same availibility zone as EC2 instance.
 - To move an EC2 volume from one AZ/Region to another, take a snap or an image of it, then copy it to the new AZ/Region.
 - Snapshots of encrypted volumes are encrypted automatically.
 - Volumes restored from encrypted snapshots are encrypted automatically.
 - You can share the snapshots, but only if they are unencypted. They can be shared with other AWS accounts or can be made public.