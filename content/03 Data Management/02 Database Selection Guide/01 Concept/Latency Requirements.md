# Latency Requirements

> <- Back to [[Key Decision Factors]]

Sub-millisecond requirements demand Redis/Memcached (in-memory). Single-digit millisecond needs suit DynamoDB. Low millisecond works with Postgres given proper indexing.

## Key Properties

- [[Sub-Millisecond Redis Memcached]]
- [[Single-Digit ms DynamoDB]]
- [[Low ms Postgres with Indexing]]

---

#database-selection #latency
