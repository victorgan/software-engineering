# Readiness Probes

> <- Back to [[Health Checks]]

Health checks that determine if a service is ready to accept traffic. Unlike liveness probes, a failing readiness probe removes the instance from the load balancer without restarting it, allowing it time to recover (e.g., after a dependency becomes available).

#sre #health-checks #readiness
