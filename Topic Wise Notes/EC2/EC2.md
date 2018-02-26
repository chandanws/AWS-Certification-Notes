# EC2 (Elastic Compute Cloud)

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