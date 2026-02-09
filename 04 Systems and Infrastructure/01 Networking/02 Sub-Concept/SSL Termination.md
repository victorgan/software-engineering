# SSL Termination

> <- Back to [[Layer 7 Load Balancing]]

The load balancer decrypts incoming HTTPS traffic and forwards unencrypted HTTP to backend servers. This offloads the computationally expensive TLS handshake and encryption from backends, simplifies certificate management, and allows the LB to inspect request contents for routing.

#networking #load-balancing #security
