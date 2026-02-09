# Eventual Consistency Saga

> <- Back to [[Saga Pattern]]

Sagas trade strong consistency (ACID transactions) for eventual consistency across services. During saga execution, intermediate states are visible. Applications must handle these intermediate states gracefully (e.g., showing "order processing" rather than "order complete" until all steps finish).

#distributed-systems #patterns #transactions
