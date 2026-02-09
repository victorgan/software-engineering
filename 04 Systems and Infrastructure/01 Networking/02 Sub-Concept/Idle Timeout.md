# Idle Timeout

> <- Back to [[Keep-Alive]]

The duration a connection can remain idle before being closed. TCP keep-alive probes detect dead connections (default: 2 hours on Linux, configurable). Application-level timeouts are typically shorter. Load balancers and firewalls may silently drop idle connections, requiring application-level heartbeats.

#networking #tcp
