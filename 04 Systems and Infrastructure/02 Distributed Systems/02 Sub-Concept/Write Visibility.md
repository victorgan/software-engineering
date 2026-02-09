# Write Visibility

> <- Back to [[Read-Your-Writes]]

Ensuring that a client can immediately read the data it just wrote, even in a system with eventual consistency. The write must be visible to subsequent reads from the same client, though other clients may still see stale data until replication catches up.

#distributed-systems #consistency
