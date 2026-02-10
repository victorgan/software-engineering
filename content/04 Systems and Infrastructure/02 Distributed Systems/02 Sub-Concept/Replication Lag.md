# Replication Lag

> <- Back to [[Single-Leader Replication]]

The delay between a write being accepted by the leader and that write being applied to a replica. Typically milliseconds in normal conditions but can grow to seconds or minutes under high load or network issues. Applications reading from replicas must tolerate or account for this lag.

#distributed-systems #replication
