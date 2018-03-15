# SNS (Simple Notification Service) ([FAQs](https://aws.amazon.com/sns/faqs/))

SNS is a web service that makes it easy to set up, operate, and send notifications from cloud. It provides developers with a highly scalable, flexible, cost effective capability to publish messages from an application and immediately deliver them to subscribers or other applications.

## Important Points
 - To prevent messages from being lost, all messages published to Amazon SNS are stored redundantly across multiple availability zones.
 - Instantaneous, push-based delievery(no polling)
 - Simple APIs and easy integration with applications
 - Flexible message delivery over multiple transport protocols
 - Pay-as-you go model
 - Simple point and click interface

## SNS Subscribers
 - HTTP
 - HTTPS
 - Email
 - Email-JSON
 - SQS
 - Application
 - Lambda

## SNS vs SQS
 - Both messaging services in AWS
 - SNS - Push
 - SQS - Polls(Pulls)