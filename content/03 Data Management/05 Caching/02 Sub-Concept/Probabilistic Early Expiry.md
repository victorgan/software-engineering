# Probabilistic Early Expiry

> <- Back to [[Cache Stampede Thundering Herd]]

Each request has a small probability of refreshing the cache before the TTL expires. Spreads regeneration over time, preventing a thundering herd at the exact expiry moment.

#caching #invalidation #stampede
