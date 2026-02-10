# Locking

> <- Back to [[Cache Stampede Thundering Herd]]

When a cache entry expires, only one request acquires a lock to regenerate it. Other requests wait for the lock to be released, then read the freshly cached value.

#caching #invalidation #stampede
