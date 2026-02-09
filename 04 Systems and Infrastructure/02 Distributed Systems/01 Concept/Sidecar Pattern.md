# Sidecar Pattern

> <- Back to [[Distributed System Patterns]]

A co-located helper process deployed alongside the main application that handles cross-cutting concerns: logging, monitoring, networking, security. The application communicates with the sidecar via localhost. The basis of service mesh architecture (Envoy sidecar). Deployed as a separate container in the same pod (Kubernetes).

## Key Properties

- [[Co-Located Process]]
- [[Cross-Cutting Concerns]]
- [[Language Agnostic]]

## Related

- [[Service Mesh]] (built on the sidecar pattern)
- [[Bulkhead]] (sidecars provide resource isolation)

---

#distributed-systems #patterns
