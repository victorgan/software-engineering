# Request Coalescing

> <- Back to [[Cache Stampede Thundering Herd]]

Multiple simultaneous requests for the same cache key are collapsed into a single database request. All waiting requests share the result.

#caching #invalidation #stampede
