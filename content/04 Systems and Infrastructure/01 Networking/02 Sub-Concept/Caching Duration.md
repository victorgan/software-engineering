# Caching Duration

> <- Back to [[TTL]]

The TTL value in seconds determines how long resolvers cache a DNS record. Common values: 300 (5 min) for dynamic services, 3600 (1 hour) for stable services, 86400 (1 day) for rarely changing records. Lower TTLs before planned changes enable faster cutover.

#networking #dns
