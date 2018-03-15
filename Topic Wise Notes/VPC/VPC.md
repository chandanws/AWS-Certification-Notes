# VPC ([FAQs](https://aws.amazon.com/vpc/faqs/))
*Kind of a virtual/logical data centre in the cloud*

## Important Points
 - Consists of IGWs(or Virtual Private Gateways), Route Tables, Network Access Control Lists, Subnets and Security Groups
 - 1 Subnet = 1 Availability Zone
 - Security groups are stateful; Network access control lists are stateless

## What can you do with a VPC?
 - Launch instances into a subnet of your choosing
 - Assign custom IP address ranges in each subnet
 - Configure route tables between subnets
 - Create internet gateway and attach to the VPC
 - Much better security control over AWS resources
 - Instance security groups
 - Subnet network access control lists (ACLs)

## Default VPC vs Custom VPC
 - Default VPC is user friendly allowing you to immediately deploy instances
 - All subnets in the default VPC have a route out to the internet
 - No private subnets in default VPC
 - Each EC2 instance has both a public and a private IP address

## VPC Peering
 - Allows you to connect one VPC with another via a direct network route using private IP address
 - Instances behave as if they were on same private network
 - You can peer VPCs with other AWS accounts as well as with other VPCs in the same account
 - Peering is always in a star configuration i.e. 1 central VPC peers with 4 others. NO TRANSITIVE PEERING

## Creating a VPC
 - While creating a new VPC, a route table, a network access control list and a security group is created along with a VPC
 - 5 IP addresses are not available while creating a subnet i.e. only 251
 - We cannot have multiple Internet Gateways on a VPC

## VPC Flow Logs
VPC Flow Logs is a feature that enables you to capture information about the IP traffic going to and from network interfaces in your VPC. Flow log data is stored using Amazon CloudWatch Logs. After you have created a flow log, you can view and retrieve its data in Amazon CloudWatch Logs.

## Three levels for VPC Flow Logs
 - VPC
 - Subnet
 - Network Interface Level

## Important points for VPC Flow Logs
 - You cannot enable flow logs for VPCs that are peered with your VPC unless the peer VPC is in your account
 - You cannot tag a flow log
 - After you have created a flow log, you cannot change its configuration; for example you can't associate a different IAM role with a flow log.
 - Not all traffic is monitored.
