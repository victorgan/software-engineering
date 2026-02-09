# Database Failover

> <- Back to [[Failover Strategies]]

Automatic promotion of a database replica to primary when the current primary fails. Critical concerns include split-brain prevention (two nodes both believing they are primary) and ensuring replication lag does not cause data loss during failover.

## Key Properties

- [[Automatic Replica Promotion]]
- [[Split-Brain Prevention]]
- [[Replication Lag Impact]]

---

#disaster-recovery #failover #database
