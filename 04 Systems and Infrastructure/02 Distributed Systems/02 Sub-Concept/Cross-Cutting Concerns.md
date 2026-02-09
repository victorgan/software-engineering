# Cross-Cutting Concerns

> <- Back to [[Sidecar Pattern]]

Functionality needed by every service but not part of core business logic: logging, metrics, tracing, authentication, encryption, rate limiting, health checking. The sidecar handles these concerns uniformly across all services, ensuring consistent behavior without duplicating code in every service.

#distributed-systems #patterns
