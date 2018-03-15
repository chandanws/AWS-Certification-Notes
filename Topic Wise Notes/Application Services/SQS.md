# SQS (Simple Queue Service) ([FAQs](https://aws.amazon.com/sqs/faqs/))
It is a distributed queue system that enables web service applications to quickly and reliably queue messages that one component in the application generates to be consumed by another component. A queue is temporary repository of messages that are awaiting processing.

## Important Points
 - SQS is pull based, not pushed base
 - Messages can be kept in queue from 1 minute to 14 days. Default is 4 days
 - Visibility time out is the time the message is invisible from the queue once the reader picks it up
 - Visibility timeout is maximum 12 hours
 - Messages can contain upto 256 Kb of text in any format
 - SQS gaurantees that the message would be processed at least once.
 - Any component can later retrieve the message programmatically using the Amazon SQS API
 - Queue acts as a buffer between the component producing and saving data, and the component receiving the data for processing.
 - Long polling is a way to retrieve your messages from your Amazon SQS queues.

## Two types of Queue
 - Standard Queue(Default)
 	- Allows nearly-unlimited number of transactions per second
 	- Standard queues gaurantee that message is delievered at least once.
 	- Provides best effort ordering which ensures that messages are generally delievered in the same order as they are sent.
 - FIFO Queue 
 	- Messages are delievered in the order in which they arrive.
 	- Also support multiple ordered message groups within a single queue.
 	- FIFO queues are limited to 300 transactions per second.