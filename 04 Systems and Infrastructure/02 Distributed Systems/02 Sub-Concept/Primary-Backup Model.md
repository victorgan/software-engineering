# Primary-Backup Model

> <- Back to [[Zab]]

One node (the primary/leader) handles all write requests and broadcasts state changes to backups. If the primary fails, a backup is promoted. Simpler than multi-writer approaches but the primary is a single point of failure for writes (though not for reads in some configurations).

#distributed-systems #consensus
