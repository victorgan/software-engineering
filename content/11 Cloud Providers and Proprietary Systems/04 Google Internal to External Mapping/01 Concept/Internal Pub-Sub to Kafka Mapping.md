# Internal Pub/Sub to Kafka Mapping

> <- Back to [[Infrastructure Mapping]]

| | Google Internal | Open Source / Industry | GCP |
|---|---|---|---|
| System | Pub/Sub (internal) | Kafka, RabbitMQ | Cloud Pub/Sub |
| Concept | Messaging | Message queues / Pub-sub | Managed messaging |

Google's internal Pub/Sub messaging system handles inter-service communication. Externalized as Cloud Pub/Sub on GCP. Industry equivalents include Apache Kafka (log-based), RabbitMQ (traditional broker), and AWS SQS/SNS. Cloud Pub/Sub combines queue and topic semantics.

---

#google-internal #mapping #pub-sub #kafka
