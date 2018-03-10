# Route53 ([FAQs](https://aws.amazon.com/route53/faqs/))

## Types of Routing Policies
 - **Simple:** Default Routing policy when you create a new record set. This is most commonly used when you have a single resource that performs a given function for your domain.
 - **Weighted:** It allows you to split your traffic based on different weights assigned.
 - **Latency:** Allows you to route the traffic based on the lowest network latency for your end user(ie the region which will them fastest response time)
 - **Failover:** Used when you want to create an active/passive set up. In case of a health check failure for primary set up, Route53 would redirect traffic to passive set-up
 - **Geolocation:** It lets you choose where your traffic will be sent based on the geographic location of your users

## DNS Record Types supported by Route 53
 - A Record Type
 - AAAA Record Type
 - CAA Record Type
 - CNAME Record Type
 - MX Record Type
 - NAPTR Record Type
 - NS Record Type
 - PTR Record Type
 - SOA Record Type
 - SPF Record Type
 - SRV Record Type
 - TXT Record Type