# CP Systems

> <- Back to [[CAP Theorem]]

Systems that prioritize Consistency and Partition Tolerance over Availability. During a network partition, these systems may become unavailable (reject requests) rather than return stale data. Examples: HBase, MongoDB (with majority reads), ZooKeeper, etcd. Appropriate for financial transactions and coordination services.

#distributed-systems #cap
