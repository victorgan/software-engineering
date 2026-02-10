# Health Check Endpoints

> <- Back to [[Health Checks]]

Dedicated HTTP endpoints (e.g., /health, /healthz, /ready) that report server status. Liveness checks indicate the process is running. Readiness checks indicate the service can handle traffic (dependencies available, warmed up). Kubernetes uses both to manage pod lifecycle.

#networking #load-balancing #reliability
