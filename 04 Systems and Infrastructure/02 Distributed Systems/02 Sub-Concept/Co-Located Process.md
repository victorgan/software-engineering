# Co-Located Process

> <- Back to [[Sidecar Pattern]]

The sidecar runs as a separate process on the same host (or in the same Kubernetes pod) as the main application. Communication is via localhost (fast, reliable). The sidecar shares the same lifecycle — it starts and stops with the main application. No network latency for sidecar communication.

#distributed-systems #patterns
