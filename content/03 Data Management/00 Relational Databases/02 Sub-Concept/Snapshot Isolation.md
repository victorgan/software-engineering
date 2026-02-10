# Snapshot Isolation

> <- Back to [[MVCC (Multi-Version Concurrency Control)]]

Each transaction sees a consistent snapshot of the database as of the transaction's start time. Readers never block writers and writers never block readers. Implemented via MVCC.

#relational-databases #transactions #mvcc #snapshot-isolation
