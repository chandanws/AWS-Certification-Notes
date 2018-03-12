# Aurora ([FAQs](https://aws.amazon.com/rds/aurora/faqs/))

*Amazon Aurora is a MySQL-compatible, relational database engine that combines the speed and availabilty of high-end commercial databases with the simplicity and cost-effectiveness of open source databases. Aurora provides upto five times the better performance than MySQL at a price point one tenth that of a commercial database while delivering similar performance and availability.*

## Important Points 
 - Start with 10Gb, scales in 10Gb increments to 64Tb(Storage autoscaling)
 - Compute resources can scale upto 32vCPUs and 244Gb of memory
 - There is a downtime while scaling but the scaling period is pretty quick
 - 2 copies of data is available in each availability zone with minimum 3 AZs i.e. 6 copies of your data
 - Aurora is designed to handle the loss of 2 copies of data without affecting the write availabilty and upto 3 copies of data without affecting read availability.
 - Storage is self healing. Data blocks are continuously scanned for errors and repaired automatically
 - 2 types of replicas are available
 	- Aurora Replicas(15 currently)
 	- MySQL read replicas(15 currently)