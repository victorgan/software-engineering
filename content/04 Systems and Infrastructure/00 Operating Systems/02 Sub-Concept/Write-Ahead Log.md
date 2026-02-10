# Write-Ahead Log

> <- Back to [[Journaling]]

Changes are recorded in a sequential log before being applied to the main data structures. If a crash occurs, the log is replayed to bring the file system to a consistent state. The same principle is used in databases (WAL) and distributed systems.

#operating-systems #file-systems #reliability
