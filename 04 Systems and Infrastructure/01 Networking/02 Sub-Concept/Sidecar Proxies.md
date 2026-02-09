# Sidecar Proxies

> <- Back to [[Service Mesh]]

A proxy (typically Envoy) deployed alongside each service instance that intercepts all inbound and outbound network traffic. The application code is unaware of the mesh — the sidecar handles TLS, retries, circuit breaking, load balancing, and telemetry transparently. Injected automatically in Kubernetes.

#networking #service-mesh
