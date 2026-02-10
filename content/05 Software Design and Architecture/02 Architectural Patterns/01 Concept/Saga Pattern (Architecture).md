# Saga Pattern (Architecture)

> <- Back to [[Microservices]]

Manage distributed transactions across multiple services using a sequence of local transactions. Each service performs its transaction and publishes an event. If one step fails, compensating transactions undo previous steps. Two styles: choreography (events) and orchestration (central coordinator).

## Key Properties

- [[Choreography Saga]]
- [[Orchestration Saga]]
- [[Compensating Transactions]]

## Related

- [[Event Sourcing]] (event-based coordination)
- [[Data Ownership]] (why sagas are needed)

---

#architecture #microservices #saga
