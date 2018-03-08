# Lambda ([FAQs](https://aws.amazon.com/lambda/faqs/))

*AWS Lambda is a compute service where you can upload your code and create a Lambda function. AWS Lambda takes care of provisioning and managing the servers that you use to run the code. You don't have to worry about operating systems, patching, scaling etc.*

## You can use Lambda function in following ways:
 - As an event-driven compute service where AWS Lambda runs your code in response to events. These events could be changes to data in an Amazon S3 bucket or an Amazon DynamoDB table
 - As a compute service to run your code in response to HTTP requests using Amazon API gateway or API calls made using AWS SDKs.

## Important Points
 - Every time a user makes a request, a new Lambda function(Identical Code) gets triggered.
 - Lambda is priced based on number of requests
 - First 1 million requests are free
 - Lambda is also priced based on duration the code runs on the Lambda function. 
 - Lambda is a disruptive technology as:
 	- No servers are required
 	- Continuous Scaling
 	- Super cheap
 - Lambda scales out (Not up) automatically
 - Lambda functions are independent, 1 event = 1 function
 - Lambda is serverless
 - Lambda functions can trigger other lambda functions
 - In complex architecture, AWS X-Rays can help with debugging
 - Lambda can do things globally. We can backup S3 bucket to another S3 bucket
 - Lambda duration time is maximum of 5 minutes
 - Know the triggers for Lambda function

## Programming Languages supported by Lambda
 - Node.js
 - Java
 - Python 
 - C#