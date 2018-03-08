# EFS (Amazon Elastic File System) ([FAQs](https://aws.amazon.com/efs/faq/))

*Amazon Elastic File System is a file storage service for Amazon Elastic Compute Cloud(EC2) instances. Amazon EFS is easy to use and provides a simple interface that allows you to create and configure file systems quickly and easily. With Amazon EFS, storage capacity is elastic, growing and shrinking automatically as you add and remove files, so your application have the storage they need, when they need it*

## Important Points
 - Supports the Network File System version 4 (NFSv4) protocol
 - You only pay for the storage you use (no pre-provisioning required)
 - Can scale up to petabytes
 - Can support thousand of concurrent connections
 - Data is stored accorss multiple Availabilty Zones within a region
 - Its a block based storage compared to S3 which is an object based storage
 - Read after write concurrency
 - Allows multiple EC2 instances to connect to it compared to an EBS volume which is mounted to a single instance