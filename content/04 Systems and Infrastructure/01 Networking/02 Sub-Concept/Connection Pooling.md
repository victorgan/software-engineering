# Connection Pooling

> <- Back to [[Keep-Alive]]

Maintaining a pool of pre-established connections that can be reused by multiple requests. Common in database clients, HTTP clients, and load balancers. Eliminates connection setup latency and reduces the number of sockets in TIME_WAIT. Pool size tuning is critical — too small causes contention, too large wastes resources.

#networking #tcp #performance
