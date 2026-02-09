# Consistent Hashing LB

> <- Back to [[Load Balancing Algorithms]]

Maps requests to servers using a hash ring, ensuring the same key always routes to the same server. When servers are added or removed, only 1/n keys are remapped (minimal disruption). Used for cache-friendly load balancing where routing the same user/key to the same server improves cache hit rates.

#networking #load-balancing #algorithms
