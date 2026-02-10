# Packfiles

> <- Back to [[Git Internals]]

Delta compression for efficient storage. Git periodically packs loose objects into packfiles that store objects as deltas against similar objects. This dramatically reduces repository size, especially for large files with small changes.

## Key Properties

- [[Delta Compression]]
- [[Pack Index]]
- [[Garbage Collection]]

## Related

- [[Object Model]] (what gets packed)
- [[Large File Storage]] (alternative for binaries)

---

#git #internals #packfiles
