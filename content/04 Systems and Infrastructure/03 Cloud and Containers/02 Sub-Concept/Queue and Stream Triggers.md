# Queue and Stream Triggers

> <- Back to [[Event-Driven Serverless]]

Functions triggered by messages in queues (SQS, Cloud Tasks) or events in streams (Kinesis, Kafka, DynamoDB Streams). The cloud provider manages polling and batching. Functions process messages in batches for throughput. Failed messages can be sent to dead letter queues for retry.

#cloud #serverless #messaging
