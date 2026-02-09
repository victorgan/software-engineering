# Consistent Hashing

> ← Back to [[Hash-Based Structures]]

Hash technique that minimizes key redistribution when nodes are added or removed. Only K/n keys need to move on average (K = total keys, n = number of nodes).

## Key Properties

- [[Partitioning]]

## How It Works

Keys and nodes are placed on a hash ring. Each key is assigned to the nearest node clockwise. Virtual nodes improve balance.

## Related

- [[Hash Tables]]
- [[Distributed Systems]] (primary use case)
- [[Sharding and Partitioning]]

---

#data-structures #hashing #distributed-systems
