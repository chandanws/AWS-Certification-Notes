# Kinesis ([FAQs](https://www.amazonaws.cn/en/kinesis/streams/faqs/))

Amazon Kinesis is a platform on AWS to send your streaming data. Kinesis makes it easy to load and analyze streaming data, and also providint the ability for you to build your own custom applications.

## Core Kinesis Services
 - Kinesis Streams
 	- Default storage of 24 hours. Increased upto 7 days
 	- Stores/Streams the data into **Shards**
 	- 5 transactions/second for reads
 	- Maximum total data read of 2 MP per second
 	- Upto 1000 records per second for writes
 	- Write rate upto 1MB per second
 	- Total capacity of stream is sum of capacities of its shards
 - Kinesis Firehose: 
 	- Data is sent directly to Firehose. No consumers required
 	- Directly analyze data using Lamdas
 - Kinesis Analytics:
 	- Allows to run SQL queries on the data stored in Firehose or Streams