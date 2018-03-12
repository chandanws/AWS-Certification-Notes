# DynamoDB ([FAQs](https://aws.amazon.com/dynamodb/faqs/))

*DynamDB is a fast and flexible NoSQL database service for all applications that need consistent, single-digit millisecond latency at any scale. It is a fully managed database and supports both document and key-value data models. Its flexible data model and reliable performance makes it a great fit for mobile, web, gaming, ad-tech, IOT and many other applications*

## Important points about DynamoDB
 - Stored on SSD storage
 - Spread across 3 geographically distinct data centres
 - Two types of Reads:
	 - Eventual Consistent Reads
	 	Consistency across all copies of data is usually reached within a second. Repeating a read after a short amount of time would return the updated data (Best read performance)
	 - Strong Consistent Reads
	 	A strongly consistent read returns a result that reflects all writes that received a successful response prior to the read.
 - DynamoDB reads are cheaper than DynamoDB writes
 - DynamoDB allows push-button scaling i.e. it can be scaled on the fly
 - No down time is involved while scaling a DynamoDB

## DynamoDB Pricing
 - Provisioned Throughput Capacity
 	- Write throughput $0.0065 per hour for 10 units
 	- Read throughput $0.0065 per hour for 50 units
 - Storage Costs of $0.25Gb per month