# SHA-1 Hashing

> <- Back to [[Git Internals]]

Content-addressable storage where every object is identified by its SHA-1 hash. Identical content always produces the same hash, enabling deduplication and integrity verification. Git is transitioning to SHA-256 for improved collision resistance.

## Key Properties

- [[Content Addressability]]
- [[Integrity Verification]]
- [[Deduplication]]

## Related

- [[Object Model]] (objects identified by hash)

---

#git #internals #hashing
