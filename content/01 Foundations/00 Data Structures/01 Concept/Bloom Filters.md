# Bloom Filters

> ← Back to [[Hash-Based Structures]]

Space-efficient probabilistic data structure for membership testing. Can have false positives but never false negatives — "probably in the set" or "definitely not in the set."

## Key Properties

- [[Probabilistic Membership]]
- [[False Positives]]
- [[No False Negatives]]

## How It Works

Multiple hash functions map each element to bit positions in a bit array. To check membership, verify all corresponding bits are set.

## Related

- [[Hash Sets]] (exact alternative, more memory)
- [[Hash Functions]]
- [[Caching]] (used to avoid unnecessary cache lookups)

---

#data-structures #hashing #probabilistic
