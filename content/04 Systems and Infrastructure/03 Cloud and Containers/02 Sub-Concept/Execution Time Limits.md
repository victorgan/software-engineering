# Execution Time Limits

> <- Back to [[Serverless Limitations]]

FaaS platforms impose maximum execution times: AWS Lambda 15 minutes, Google Cloud Functions (1st gen) 9 minutes, Azure Functions 10 minutes (consumption plan). Long-running tasks must be broken into smaller steps using Step Functions, workflows, or queues. Not suitable for WebSocket connections or long-polling.

#cloud #serverless
