# Automatic Retry on Conflict

> <- Back to [[Software Transactional Memory (STM)]]

When an STM transaction detects that another transaction has modified the same data (a conflict), it automatically rolls back its changes and retries from the beginning. This optimistic concurrency control avoids deadlocks entirely — transactions never hold locks.

#concurrency #models #stm #retry
