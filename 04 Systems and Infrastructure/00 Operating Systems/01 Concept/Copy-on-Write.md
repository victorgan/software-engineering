# Copy-on-Write

> <- Back to [[File Systems]]

Instead of overwriting data in place, writes go to a new location and the metadata pointer is updated atomically. Provides inherent crash consistency without a journal, enables cheap snapshots, and supports data integrity verification. Used by ZFS and Btrfs.

## Key Properties

- [[Atomic Updates]]
- [[Snapshot Support]]
- [[Data Integrity Verification]]

## Related

- [[Journaling]] (alternative approach to crash safety)
- [[Distributed File Systems]] (many use CoW concepts)

---

#operating-systems #file-systems #reliability
