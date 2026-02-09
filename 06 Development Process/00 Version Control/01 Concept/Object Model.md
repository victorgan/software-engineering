# Object Model

> <- Back to [[Git Internals]]

Git stores data as four types of objects: Blobs (file contents), Trees (directories mapping names to blobs/trees), Commits (snapshots pointing to a tree with metadata), and Tags (named references to commits). All objects are immutable and content-addressed.

## Key Properties

- [[Blob Objects]]
- [[Tree Objects]]
- [[Commit Objects]]

## Related

- [[SHA-1 Hashing]] (how objects are addressed)
- [[The DAG]] (commit graph structure)

---

#git #internals #object-model
