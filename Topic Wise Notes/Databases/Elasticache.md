# Elasticache ([FAQs](https://aws.amazon.com/elasticache/faqs/))

*Elasticache is a web-service that makes it easy to deploy, operate and scale in-memory cache in the cloud. The service improves the performance of web applications by allowing you to retrieve information from fast, managed, in-memory caches, instead of relying entirely on slow-disk based databases.*

## Important Points
 - Can be used to significantly improve latency and throughput for many read-heavy application workloads
 - It improves application performance by storing critical pieces of information in memory for low-latency access.
 - A good choice if your database is particularly read heavy and not prone to frequent changes

## Types of Elasticache
 - Memcached: A widely adopted memory object caching system. Elasticache is protocol compliant with memcached, so popular tools will work seamlessly with the service
 - Redis: A popular open-source in-memory key-value store that supports data strucutures such as sorted sets and lists. Elasticache supports Master/Slave replication and Multi AZ which can be used to achieve cross AZ redundancy