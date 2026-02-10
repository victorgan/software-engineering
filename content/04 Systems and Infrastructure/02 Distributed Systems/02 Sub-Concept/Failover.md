# Failover

> <- Back to [[Leader Election]]

When the leader fails, a new leader must be elected. Automatic failover detects the failure (via heartbeat timeout) and triggers a new election. Manual failover requires human intervention. The failover process must ensure the new leader has all committed data to prevent data loss.

#distributed-systems #patterns
