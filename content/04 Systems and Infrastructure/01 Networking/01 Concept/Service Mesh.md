# Service Mesh

> <- Back to [[Other Networking Topics]]

A dedicated infrastructure layer for handling service-to-service communication. Sidecar proxies (Envoy) are deployed alongside each service to handle traffic management, mutual TLS, observability, and retries transparently. Implementations include Istio and Linkerd.

## Key Properties

- [[Sidecar Proxies]]
- [[Mutual TLS]]
- [[Traffic Management]]

## Related

- [[Service Mesh on K8s]] (Kubernetes-specific service mesh deployment)
- [[API Gateway]] (handles north-south traffic; mesh handles east-west)

---

#networking #service-mesh
