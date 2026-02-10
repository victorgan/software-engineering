# Safe and Idempotent Methods

> <- Back to [[HTTP Methods]]

Safe methods (GET, HEAD, OPTIONS) do not modify server state and can be cached/prefetched. Idempotent methods (GET, PUT, DELETE) produce the same result regardless of how many times they are called. POST is neither safe nor idempotent. These properties guide retry logic and caching strategies.

#networking #http
