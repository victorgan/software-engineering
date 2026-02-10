# Compensating Transactions

> <- Back to [[Saga Pattern]]

When a step in a saga fails, compensating transactions undo the effects of previously completed steps. Unlike database rollbacks, these are application-level operations that must be explicitly designed and may require domain-specific logic.

#property #saga #compensating-transactions
