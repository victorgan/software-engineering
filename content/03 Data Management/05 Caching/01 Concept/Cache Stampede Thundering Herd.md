# Cache Stampede / Thundering Herd

> <- Back to [[Cache Invalidation]]

When a popular cache entry expires, many concurrent requests simultaneously hit the database to regenerate it. Solutions include locking, request coalescing, and probabilistic early expiry.

## Key Properties

- [[Locking]]
- [[Request Coalescing]]
- [[Probabilistic Early Expiry]]

---

#caching #invalidation #stampede
