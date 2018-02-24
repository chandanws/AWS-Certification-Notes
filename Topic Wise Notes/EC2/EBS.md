# EBS

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