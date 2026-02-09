# Data Ownership

> <- Back to [[Microservices]]

Each service owns its data, no shared databases. Services encapsulate their data storage and expose it only through their API. Shared databases create tight coupling between services, defeating the purpose of the microservices architecture.

## Key Properties

- [[Database per Service]]
- [[Data Sovereignty]]
- [[Cross-Service Queries]]

## Related

- [[Saga Pattern]] (distributed transactions)
- [[CQRS]] (optimize read/write models)

---

#architecture #microservices #data-ownership
