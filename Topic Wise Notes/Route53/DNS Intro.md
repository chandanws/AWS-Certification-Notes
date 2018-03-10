# Intro to DNS
*DNS is used to convert a human-friendly domain name into an Internet Protocol(IP) address*

## IPv4 vs IPv6
 - The IPv4 is a 32 bit field and has over 4 billion different addresses.
 - IPv6 was created to solve the depletion issue we faced from IPv4 and has an address space of 128bits.
 - An Elastic Load Balancer(ELB) does not have a pre-defined IPv4 address. Only a DNS name.

## Domain Names
```google.com```
The last word in the domain name represents "top level domain". The second word in a domain name is known as a second level domain name.

## Domain Registrars
A registrar is an authority that can assign domain names directly under one or more top-level domains. Ex GoDaddy.com

## SOA Records (Start of Authority)

It stores information about:
 - The name of the server that supplied the data for the zone.
 - The administrator of the zone
 - The current version of the data file
 - The no of seconds a secondary name server should wait before checking for updates
 - The no of seconds a secondary name server should wait before retrying a failed zone transfer
 - The maximum no of seconds that a secondary name server can use data before it must either be refreshed or expired
 - The default number of seconds for the time-to-live file on resource records

## NS(Name Server) Records
Used by top level domain servers to direct traffic to the Content DNS server which contains authoritative DNS records

## A Records
It is the fundamental type of DNS record and "A" stands for address. The A record is used by a computer to translate the name of domain to an IP address. 

## TTL (Time to live)
Length of DNS record is cached on either the resolving servers or the users own local PC is equal to the value of TTL in seconds. The lower the TTL, the faster changes to DNS records to propogate throughout the internet.

## CNAMES (Canonical Names)
It can be used to resolve one domain name to another. Multiple domain names pointing to same address

## Alias Records
Alias records are used to map resource record sets in your hosted zone to Elastic Load Balancers, CloudFront distributions or S3 buckets that are configured as websites.

**Note:** A CNAME can't be used for naked domain names

## Tips
 - ELBs(Elastic Load Balancers) do not have predefined IPv4 addresses, you resolve to them using a DNS name.
 - Making a request would get charged if using a CNAME but not when using Alias record
 - Always choose Alias record over a CNAME when given a choice