# Journaling

> <- Back to [[File Systems]]

Write-ahead logging for file system crash recovery. Changes are first written to a journal (log), then applied to the actual file system. If a crash occurs mid-write, the journal is replayed on recovery to restore consistency. Used by ext4, XFS, and NTFS.

## Key Properties

- [[Write-Ahead Log]]
- [[Crash Recovery]]
- [[Journal Modes]]

## Related

- [[Copy-on-Write]] (alternative approach to crash safety)
- [[File System Concepts]] (journaling protects metadata and data)

---

#operating-systems #file-systems #reliability
