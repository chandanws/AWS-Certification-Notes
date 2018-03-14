# NAT

[Comparision of NAT Instances & NAT Gateways](https://docs.aws.amazon.com/AmazonVPC/latest/UserGuide/vpc-nat-comparison.html)

## Important Points about NAT Instances
 - When creating a NAT instance, disable Source/Destination check on the Instance
 - NAT instances must be in a public subnet
 - There must be a route out of the private subnet to the NAT instance, in order for this to work.
 - The amount of traffic that NAT instance can support depends on the instance size. If the requirements increase, increase the instance size.
 - In real environment, you can create high availability using Autoscaling Groups, multiple subnets in different AZs, and a script to automate failover.
 - NAT instances are behind a security group.

## Important Points about NAT Gateways
 - **Preferred by enterprise**
 - Scale automatically up to 10Gbps
 - No need to patch
 - Not associated with security groups
 - Automatically assigned a public IP address
 - Remember to update your route tables
 - No need to disable Source/Destination checks contrary to that of NAT Instances
 - More secure than a NAT Instance

## NACL(Network Acess Control List)
 - Your VPC automatically comes with a default network ACL, and by default it allows all outbound & inbound traffic
 - You can create custome network ACLS. By default, each customer network ACL denies all inbound & outbound traffic until you add rules.
 - Each network in the VPC must be associated with a network ACL. If you don't explicitly associate a subnet with a network ACL, the subnet is automatically associated with a default network ACL
 - You can associate a network ACL with multiple subnets; however, a subnet can be associated with only one network ACL at a time. When you associate a network ACL with a subnet, the previous association is removed.
 - Network ACLs can span availability zone but subnets cannot span availability zone.
 - Network ACLs contain a numbered list of rules that is evaluated in order, starting with the lowest numbered rule.
 - Network ACLs can have separate inbound & outbound rules and each rule can allow or deny traffic.
 - Network ACLs are stateless; responses to the allowed inbound traffic are subject to the rules for outbound traffic
 - Ephemeral ports are to be allowed on outbound rules only
 - Block IP addresses using ACLs & not security groups