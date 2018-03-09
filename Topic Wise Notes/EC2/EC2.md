# EC2 (Elastic Compute Cloud) ([EC2 FAQs](https://aws.amazon.com/ec2/faqs/) [Autoscaling FAQs](https://aws.amazon.com/autoscaling/faqs/) [Load Balancing FAQs](https://aws.amazon.com/elasticloadbalancing/faqs/))

## What is it?
Amazon EC2 is a web service that provides resizable compute capacity in the cloud. EC2 reduces the time required to obtain and boot new server instances to minutes, allowing you to quickly scale capacity, both up and down, as your computing requirement changes.

Amazon EC2 changes the economics of computing by allowing you to pay only for the capacity that you actually use. Amazon EC2 provides developers the tools to build failure resilient applications and isolate themselves from common failure scenarios.

## EC2 Options
1. **On Demand** - Allow you to pay a fixed rate by hour(or by second) with no commitment. 
2. **Reserved** - Provide you with a capacity reservation, and offer a significant discount on hourly charge for an instance. 1 Year or 3 Year terms. Users able to make upfront payments to reduce their total computing costs even further.
	- Standard RIs(Up to 75% off on Demand)
	- Convertible RIs(Up to 54% off on Demand) Capability to change the attributes of reserved instances as long as the exchange results in creation of Reserved Instances of equal or greater value.
	- Scheduled RIs available to launch within the time windows you reserve. This option allows you to match your capacity reservation to a predictable recurring schedule that only requires a fraction of a day, a week, or a month.	
3. **Spot** - Enable you to bid whatever price you want for instance capacity, providing for even greater savings if your application has flexible start and end times. 
		- If you terminate the instance, you pay for the hour. 
		- If AWS terminates the instance, you get the hour it was terminated for free.
4. **Dedicated Hosts** - Physical EC2 server dedicated for your use. Dedicated hosts can help you reduce costs by allowing you to use your existing server-bound software licenses.

## EC2 Instance Types
![EC2 Instance Types](https://github.com/varunu28/AWS-Certification-Notes/blob/master/Images/EC2_Instance_Types.png)

## Important Points about EC2
 - By default, you cannot encrypt the EBS root device volume. You can use a third-party tool such as bit locker etc to encrpt the root volume or this can be done when creating AMIs in the AWS console or using the API.
 - Additional volumes can be encrypted. 
 - Termination protection is turned off by default, you must turn it on.
 - On an EBS-backed instance, the default action is for the root EBS volume to be deleted when instance is terminated.
 - To create a snapshot for Amazon EBS volumes that serve as root devices, you should stop the instance before taking the snapshot.
 - Snapshots of encrypted volumes are encrypted automatically.
 - Volumes restored from encrypted snapshots are encrypted automatically.
 - You can share snapshots only if they are unencrypted.
 	- These snapshots can be shared with other AWS accounts or made public.
 - Instance store volumes are sometimes called Ephemeral Storage.
 - Instance store volumes cannot be stopped if the underlying host fails, you will lose your data.
 - EBS backed instances can be stopped and you will not lose the data on this instance if it is stopped.
 - You can root EBS backed instances and instance store volumes and you will not lose data.
 - By default both root volumes will be deleted on termination. However with EBS volumes, you can tell AWS to keep the root device volumes.
 - Termination protection is turned off by default.
 - On an EBS-backed instance, the default action is for the root EBS volume to be deleted when the instance is terminated.

## You can select your AMI based on:
 - Region
 - Operating Systems
 - Architecture(32 bit or 64 bit)
 - Launch Permissions
 - Storage for the root device (Root device volume)
 	- Instance Store (EPHEMERAL Storage)
 	- EBS Backed Volumes

## Load Balancers & Health Check: ([Elastic Load Balancer FAQs](https://aws.amazon.com/elasticloadbalancing/faqs/))
 - Instances monitored by Elastic Load Balancers(ELBs) are reported as:
 	- InService
 	- OutofService
 - Health Checks check the instance health by talking to the instance
 - Have their own DNS name. You are never given an IP address.
 - Focus more on Classic load balancer for the exam

## Cloud Watch: ([Cloud Watch FAQs](https://aws.amazon.com/cloudwatch/faqs/))
 - Different from Cloud Trail as Cloud Trail does the audit of services whereas CloudWatch does monitoring of services.
 - Monitoring Periods
 	- Standard Monitoring = 5 minutes
 	- Detailed Monitoring = 1 minute
 - Dashboards - Create dashboards to see what is happening with your AWS environment.
 - Alarms - Allows you to set alarms that notify when particular thresholds are hit.
 - Events - CloudWatch events help you respond to state changes in your AWS resources.
 - Logs - CloudWatch Logs helps you to aggregate, monitor and store logs.

**http://169.254.169.254/latest/meta-data/ (IP for EC2 Metadata)**

## Placement Groups
A placement group is a logical grouping of instances within a single availability zone. Using placement groups enable applications to participate in a low-latency, 10 Gbps network. Placement groups are recommended for applicatios that benifit fron low network latency, high network throughput, or both.

 - A placement group can't span multiple availability zones.
 - The name for an availability group must be unique within an AWS account.
 - Only certain type of instances can be launched in a placement group
 	- Compute Optimized 
 	- GPU
 	- Memory Optimized 
 	- Storage Optimized
 - AWS recommends homogenous instances within placement group.
 - You can't merge placement groups.
 - You can't move an existing instance into a placement group. You can create an AMI from your existing instance, and then launch a new instance from the AMI into a placement group.