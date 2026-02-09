# Multi-Paxos

> <- Back to [[Paxos]]

An optimization of basic Paxos that elects a stable leader to skip the prepare phase for subsequent proposals. Since most of Paxos's overhead is in the prepare phase, Multi-Paxos significantly reduces message complexity for sequences of decisions. Most practical Paxos implementations use Multi-Paxos.

#distributed-systems #consensus
