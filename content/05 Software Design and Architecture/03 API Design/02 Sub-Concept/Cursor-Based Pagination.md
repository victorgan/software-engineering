# Cursor-Based Pagination

> <- Back to [[Pagination]]

Uses an opaque cursor token pointing to a specific position in the result set. More stable than offset-based pagination when data changes. The server encodes the position in the cursor, and the client passes it to get the next page.

#property #pagination #cursor-based
