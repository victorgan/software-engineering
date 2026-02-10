# Leader Lease

> <- Back to [[Leader Election]]

A time-bounded leadership claim that must be periodically renewed. If the leader fails to renew (crashed, partitioned), the lease expires and a new election occurs. Prevents stale leaders from continuing to act after being partitioned. Lease duration balances failover speed vs renewal overhead.

#distributed-systems #patterns
