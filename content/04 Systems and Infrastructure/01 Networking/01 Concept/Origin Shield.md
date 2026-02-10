# Origin Shield

> <- Back to [[CDN]]

An intermediate cache layer between edge servers and the origin. When an edge server has a cache miss, it queries the origin shield instead of the origin directly. This reduces the number of requests hitting the origin server, especially during cache invalidation events or traffic spikes.

## Key Properties

- [[Intermediate Cache Layer]]
- [[Origin Protection]]
- [[Collapsed Forwarding]]

## Related

- [[Edge Caching]] (first layer of CDN caching)
- [[Cache Invalidation]] (shield absorbs invalidation thundering herd)

---

#networking #cdn
