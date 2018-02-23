# Cloud Front CDN (Under Networking & Content Delivery Services)

## What is it?
Amazon Cloud Front can be used to deliver your entire website, including dynamic, static, streaming and interactive content using a global network of edge locations. Requests for your content are automatically routed to the nearest edge location, so content is delivered with the best possible performance. 

Amazon Cloud Front is optimized to work with other AWS services, like S3, EC2, Load Balancer and Route53. Cloud Front also works seamlessly with any Non-AWS origin server, which stores the original, definitive versions of your files.

## Key Points
 - **Edge Location -** This is the location where content will be cached. This is separate to an AWS Region/(Availability Zone)AZ
 - **Origin -** This is the origin of all files that the CDN will distribute. This can be S3 bucket, an EC2 instance, an Elastic Load Balancer or Route53
 - **Distribution -** This is the name given to the CDN which consists of a collection of Edge Locations

## Key Terminology
 - Web Distribution - Typically used for websites
 - RTMP - Media Streaming/ Flash files

## Important Points
 - Edge locations are not just read only, you can write to them also (i.e. Put an object in them). The update would be updated back to the origin server.
 - Objects are cached for life of TTL (Time to live) (Default value is 24 hours)
 - You can clear the cache objects but it would be charged for. Otherwise the object in usual scenario would expire after the TTL period.