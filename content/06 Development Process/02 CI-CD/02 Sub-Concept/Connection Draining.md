# Connection Draining

> <- Back to [[Zero-Downtime Deployments]]

Allowing in-flight requests to complete before shutting down an instance. The load balancer stops sending new requests to the instance while existing connections are allowed to finish, preventing dropped requests during deployment.

#property #cicd #zero-downtime #connection-draining
