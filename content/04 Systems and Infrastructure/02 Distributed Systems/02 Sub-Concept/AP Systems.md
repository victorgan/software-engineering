# AP Systems

> <- Back to [[CAP Theorem]]

Systems that prioritize Availability and Partition Tolerance over Consistency. During a network partition, these systems remain available but may return stale data. Converge to consistency when the partition heals. Examples: Cassandra, DynamoDB, CouchDB. Appropriate for social media feeds, shopping carts, DNS.

#distributed-systems #cap
