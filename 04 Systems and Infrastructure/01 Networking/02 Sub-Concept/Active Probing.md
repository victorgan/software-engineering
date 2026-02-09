# Active Probing

> <- Back to [[Health Checks]]

The load balancer periodically sends synthetic requests (HTTP GET, TCP connect, or custom checks) to backend servers. Configurable parameters: check interval, timeout, healthy/unhealthy thresholds (e.g., 3 consecutive failures = unhealthy). Catches issues even when no real traffic is flowing.

#networking #load-balancing #reliability
