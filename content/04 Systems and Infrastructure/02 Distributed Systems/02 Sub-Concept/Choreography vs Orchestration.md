# Choreography vs Orchestration

> <- Back to [[Saga Pattern]]

Choreography: each service listens for events and decides what to do next (decentralized, loosely coupled, harder to track). Orchestration: a central coordinator tells each service what to do and handles the saga flow (centralized, easier to understand, single point of failure). Choose based on complexity and coupling needs.

#distributed-systems #patterns #transactions
