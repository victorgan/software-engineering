# IP-Based Affinity

> <- Back to [[Session Affinity]]

Hashing the client's IP address to consistently route to the same backend. Simple and works at L4 (no cookie needed). Breaks when clients share an IP (NAT, corporate proxies) or when client IPs change (mobile networks). Less precise than cookie-based affinity.

#networking #load-balancing
