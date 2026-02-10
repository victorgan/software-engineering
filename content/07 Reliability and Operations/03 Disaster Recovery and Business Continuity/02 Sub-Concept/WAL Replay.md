# WAL Replay

> <- Back to [[Point-in-Time Recovery]]

Write-Ahead Log (WAL) replay applies a sequence of logged database changes to a base backup to reconstruct the database state at any point in time. WAL files capture every write operation, enabling recovery to any moment between backups.

#disaster-recovery #pitr #wal
