# RedShift ([FAQs](https://aws.amazon.com/redshift/faqs/))

*Amazon RedShift is a powerful, fully managed, petabyte-scale data warehouse service in the cloud. Customers can start small for just $0.25 per hour with no commitments and can scale to a petabyte or more for $1000 per terabyte per year, less than a tenth of most other data warehousing solutions. Mostly used for OLAP(Online Analytical Processing)*

## Important Points
 - Single Node(160 Gb)
 - Multi-Node
 	- Leader Node: Manages Client connections & receives queries
 	- Compute Node: Store data and perform queries and computations. Up to 128 Compute nodes
 - Achieves its speed due to columnar storage

## Columnar Data Storage by RedShift
Instead of storing data as series of rows, RedShift organizes data by column. Unlike row based systems, which are ideal for transaction processing, column-based systems are ideal for data warehousing and analytics.

## Advanced Compression
Columnar data stores can be compressed much more than row based data because similar data is stored sequentially on disk. While loading data, Amazon RedShift automatically samples the data and selects the most appropriate compression scheme.

## Massively Parallel Processing(MPP)
RedShift automatically distributes data and query load across all nodes. RedShift makes it easy to add nodes to data warehouse and enables to maintain fast query performance as your data warehouse grows.

## RedShift Pricing
 - Compute Node Hours: Total number of hours you run across all nodes in a billing period. You are billed 1 unit per node. Only compute nodes are charged, not leader nodes.
 - Backup
 - Data Tranfer (Only within a VPC, not outside it)

## Security
 - Encrypted in transit using SSL
 - Encrypted at rest using AES-256 encryption
 - By default RedShift takes care of key management
 - Can manage your keys through HSM(Hardware Security Modules)
 - Can manage your keys through AWS Key Management Service

## Availability
 - Currently available in only 1 AZ
 - Can restore snapshots to new AZs in event of an outage   