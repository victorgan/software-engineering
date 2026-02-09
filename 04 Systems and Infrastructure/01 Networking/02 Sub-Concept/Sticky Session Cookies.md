# Sticky Session Cookies

> <- Back to [[Session Affinity]]

The load balancer sets a cookie (e.g., SERVERID) on the first response that identifies the backend server. Subsequent requests from the same client include this cookie, allowing the LB to route to the same backend. More reliable than IP-based affinity when clients are behind NAT.

#networking #load-balancing
