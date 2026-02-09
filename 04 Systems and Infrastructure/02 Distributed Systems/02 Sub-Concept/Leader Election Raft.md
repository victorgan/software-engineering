# Leader Election Raft

> <- Back to [[Raft]]

Raft uses randomized election timeouts to elect a leader. If a follower does not hear from the leader within its timeout, it becomes a candidate and requests votes. The candidate with votes from a majority becomes the new leader. Randomization prevents split votes in most cases.

#distributed-systems #consensus
