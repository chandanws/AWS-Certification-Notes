# RDS ([FAQs](https://aws.amazon.com/rds/faqs/)) **MOST IMPORTANT**

*Mostly used for OLTP(Online Transaction Processing)*

## Available for:
- SQL Server
- Oracle
- MySQL Server
- Postgre SQL
- Maria DB
- SQL
- Aurora

## Backups
 - **Automated Backups** 
 	- Allow you to recover your database to any point in time within a "retention period".
 	- Retention period can be between one and 35 days. It will take a full daily snapshot and will also store transaction logs throughout the day. 
 	- When you do a recovery, AWS will first choose the most recent daily back up, and then apply transaction logs relevant that day. This allows for a point in time recovery down to a second, within the retention period.
 	- Automated backups are enabled by default. The backup is stored in S3 and you get free storage space equal to the size of the database.
 	- Backups are taken in a defined window. During the backup window, storage I/O may be suspened while the data is being backed up which may cause elevated latency.
 	- Automated backups are deleted once you delete the RDS instance, even though you will be prompted to do a final database backup at the time of deleting the RDS instance.
 - **Snapshots**
 	- Snapshots are done manually.
 	- They are stored even after you delete the original RDS instance.

*Whenever you restore either an automatic backup or a manual snapshot, the restored version of the database will be a new RDS instance with a new end point*

*When you add a rule to an RDS security group you do need to specify a port number or protocol*

*If you are using Amazon RDS Provisioned IOPS storage with MySQL and Oracle database engines the maximum size RDS volume you can have by default is 6TB*

## Encryption
 - Encryption at rest is supported for MySQL, Oracle, SQL Server, Postgre SQL & MariaDB. Encryption is done using the AWS key management service (KMS)
 - Once an RDS instance is encrypted the data stored at rest in the underlying storage is encrypted, as are its automated backups, read replicas and snapshots.
 - At present time, encrypting an existing DB instance is not supported. To use Amazon RDS encryption for an existing database, create a new DB instance with encryption enabled and migrate your data into it.

## Multi AZ
 - Multi AZs allow you to have an exact copy of your production database in another availabilty zone. AWS handles the replication, so when your production database is written to, this write will be synchronized to the backup.
 - In event of planned database maintanence, DB instance failure, or an Availability Zone failure, Amazon RDS will automatically failover to the standby so that database operations can resume quickly without administrative intervention.
 - It is for distaster recovery only. Not for performance improvement.
 - Available for:
 	- SQL Server
 	- Oracle
 	- MySQL Server
 	- Postgre SQL
 	- Maria DB

## Read Replica
 - Read replica allow you to have a read only copy of your production database. 
 - This is achieved by using Asynchronous replication from the primary RDS instance to read replica. 
 - You use read replica primarily for very read-heavy database workloads.
 - Supported for:
 	- MySQL Server
 	- PostgreSQL
 	- MariaDB
 - Used for scaling. Not for disaster recovery
 - Can have 5 read replicas copies of any database
 - Must have automatic backups turned on in order to deploy a read replica
 - Can have read replicas of read replicas
 - Each replica will have its own DNS end point
 - You cannot have read replicas that have Multi-AZ
 - You can create read replicas of Multi AZ source database 
 - Read replicas can be promoted to be their own databases. This breaks the replication.
 - Read replica in second region for MySQL and MariaDB. Not for PostgreSQL

## DynamoDB vs RDS
DynamoDB offers "push button" scaling, meaning that you can scale your databases on the fly, without any downtime.

RDS is not so easy and you usually have to use a bigger instance size or to add a replica