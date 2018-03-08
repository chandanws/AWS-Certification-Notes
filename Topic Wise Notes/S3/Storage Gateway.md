# Storage Gateway ([FAQs](https://aws.amazon.com/snowball/faqs/))

## What is it?
AWS Storage Gateway is a service that connects an on-premises software application with cloud-based storage to provide seamless and secure integration between an organization's on-premises IT environment and AWS's storage infrastructure. The service enables you to securely store data to AWS cloud for scalable and cost-effective storage.

AWS Storage Gateway's software appliance is available for download as a VM image that you install on host in your datacenter. Storage gateway supports either VMware ESXi or Microsoft Hyper-V. Once the gateway is installed and associated with your AWS account through activation process, you can use the AWS Management Console to create the storage gateway option that is right for you.

## Four types of Storage Gateways
1. **File Gateway (NFS)** (Essentially for flat files, stored directly on S3)
Files are stored as objects in S3 buckets, accessed through a Network File System(NFS) mount point. Ownership, permissions and timestamps are durably stored in S3 in the user-metadata of the object associated with the file. Once objects are transferred to S3, they can be managed as native S3 objects and bucket policies such as versioning, lifecycle management and CRR apply directly to objects stored in the bucket.

2. **Volumes Gateway (iSCSI)** (Essentially a virtually hard-disk)
Volume interface presents your applications with disk volumes using the iSCSI block protocol.
Data written to these volumes can be asynchronously backed up as point-in-time snapshots of your volumes and stored in the cloud as Amazon EBS(Elastic Block Store) snapshots.
Snapshots are incremental backups that capture only changed blocks. All snapshots storage is also compressed to minimize your storage charges.

#### Two Types
	- **Stored Volumes**
		Stored Volumes let you store your primary data locally, while asynchronously backing up that data on AWS.Stored volumes provide your on-premises applications with low-latency access to their entire datasets, while providing durable, off-site backups. You can create storage volumes and mount them as iSCSI devices from your on premises application servers. Data written to your stored volumes is stored on your on-premises storage hardware.This data is asynchronously backed up to Amazon S3 in form of Amazon EBS snapshots. 1GB-16TB in size.
	- **Cached Volumes**
		It lets you use S3 as primary data storage while retaining frequently accessed data locally in your storage gateway. Cached volumes minimize the need to scale your on-premise storage infrastructure, while still providing your applications with low-latency access to frequently accessed data. The storage volumes can be upto 32 TiB. 1GB-32TB in size.

3. **Tape Gateway (VTL)** (Essentially an archival solution)
It offers durable,cost-effective solution to archive data in cloud. The VTL interface it provides lets you leverage your existing tape-based cartridges that you create on your tape gateway. Each tape gateway is preconfigured with a media changer and tape drives, which are available to existing client backup applications as iSCSI devices. You can add tape cartridges you need. Supported by NetBackup, Backup Exec, Veeam etc.