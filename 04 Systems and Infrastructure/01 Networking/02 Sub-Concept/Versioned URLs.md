# Versioned URLs

> <- Back to [[Cache Invalidation]]

Including a version identifier in the URL (e.g., style.abc123.css or /api/v2/users) so that updated content gets a new URL. Allows setting very long cache TTLs since the old URL never changes. New content is automatically a cache miss. The most reliable cache invalidation strategy.

#networking #cdn #caching
