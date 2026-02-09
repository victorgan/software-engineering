# Resource Isolation

> <- Back to [[Bulkhead]]

Allocating separate pools of resources (threads, connections, memory) for different dependencies or operations. If the payment service connection pool is exhausted, the user service connection pool is unaffected. Prevents a single slow dependency from consuming all shared resources.

#distributed-systems #patterns #resilience
