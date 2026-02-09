# Log Replication

> <- Back to [[Raft]]

The leader accepts client requests, appends them to its log, and replicates the log entries to followers. An entry is committed when a majority of nodes have written it. Committed entries are guaranteed to be durable and applied in order. The replicated log ensures all nodes execute the same sequence of commands.

#distributed-systems #consensus
