# Stateless Execution

> <- Back to [[Serverless Limitations]]

Functions cannot maintain state between invocations — each invocation may run on a different instance. State must be externalized to databases, caches (Redis, DynamoDB), or object storage (S3). In-memory caching within a warm instance is possible but unreliable since instances can be recycled at any time.

#cloud #serverless
