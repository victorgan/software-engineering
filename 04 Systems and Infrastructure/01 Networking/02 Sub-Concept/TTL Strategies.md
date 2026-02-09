# TTL Strategies

> <- Back to [[TTL]]

Best practices for TTL management: use low TTLs (60-300s) for records that need fast failover or frequent updates; use high TTLs (3600-86400s) for stable records to reduce query load; lower TTL well in advance of planned changes; consider that some resolvers ignore low TTLs or enforce minimums.

#networking #dns
