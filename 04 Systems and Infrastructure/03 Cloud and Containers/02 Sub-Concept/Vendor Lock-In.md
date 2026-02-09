# Vendor Lock-In

> <- Back to [[Serverless Limitations]]

Serverless functions often depend heavily on provider-specific services (Lambda + API Gateway + DynamoDB + SQS). Migrating to another provider requires rewriting integrations. Mitigations: use open standards where possible, abstract provider-specific code behind interfaces, and evaluate whether the productivity benefits outweigh the lock-in risk.

#cloud #serverless
