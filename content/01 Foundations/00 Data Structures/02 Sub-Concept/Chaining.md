# Chaining

> ← Back to [[Hash Tables]]

Each bucket stores a linked list (or other collection) of entries. On collision, append to the list. Simple to implement. Performance degrades gracefully with high load factor. Java HashMap uses chaining (with tree fallback at high bucket count).

#property #hashing
