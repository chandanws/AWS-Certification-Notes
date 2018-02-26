 # Security Groups

## Important Points
 - 1 EC2 instance can have multiple security groups
 - Any change to a security group rule is applied immediately
 - Security groups are STATEFUL. All inbound rules are added to outbound rules automatically
 - All inbound traffic is blocked by default
 - All outbound traffic is allowed by default
 - You can have any number of EC2 instances within a security group
 - You cannot block specific IP address using Security Groups, instead use Network Access Control Lists
 - You can specify allow rules, but not deny rules.