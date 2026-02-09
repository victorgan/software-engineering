# Write-Behind (Write-Back)

> <- Back to [[Caching Strategies]]

Write to cache immediately, then asynchronously write to the database. Low write latency but risk of data loss if the cache fails before the async write completes.

## Key Properties

- [[Write to Cache Immediately]]
- [[Async Write to DB]]
- [[Risk of Data Loss]]

---

#caching #strategies #write-behind
