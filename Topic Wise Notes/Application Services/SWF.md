# SWF (Simple Workflow Service) ([FAQs](https://aws.amazon.com/swf/faqs/))
It is a web service that makes it easy to coordinate work across distributed application components. 

## Important Points
 - SQS has a retention period of 14 days, SWF up to 1 year of workflow executions.
 - SWF presents task-oriented API, whereas Amazon SQS offers a message oriented API
 - SWF ensures that a task is assigned only once and is never duplicated.
 - SWF keeps track of all the tasks and events in an application.

## SWF Actors
 - Workflow Starters: Application that can initiate a workflow
 - Deciders: Control the flow of activity tasks in a workflow execution
 - Activity Workers: Carry out the activity tasks