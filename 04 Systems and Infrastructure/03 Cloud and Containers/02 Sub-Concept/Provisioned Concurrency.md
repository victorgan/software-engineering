# Provisioned Concurrency

> <- Back to [[Cold Starts]]

Pre-initializing a specified number of function instances so they are always warm and ready to serve requests. Eliminates cold starts for those instances. Available on AWS Lambda and Google Cloud Functions. Adds cost (paying for idle warm instances) but provides predictable latency for latency-sensitive applications.

#cloud #serverless #performance
