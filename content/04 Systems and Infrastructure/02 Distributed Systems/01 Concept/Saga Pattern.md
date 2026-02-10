# Saga Pattern

> <- Back to [[Distributed System Patterns]]

Managing distributed transactions across multiple services using a sequence of local transactions with compensating actions for rollback. If step 3 fails, compensating actions undo steps 2 and 1. Two styles: choreography (events trigger next steps) and orchestration (central coordinator).

## Key Properties

- [[Compensating Actions]]
- [[Choreography vs Orchestration]]
- [[Eventual Consistency Saga]]

## Related

- [[Delivery Guarantees]] (sagas often use message queues)
- [[Point-to-Point Messaging]] (choreography uses events)

---

#distributed-systems #patterns #transactions
