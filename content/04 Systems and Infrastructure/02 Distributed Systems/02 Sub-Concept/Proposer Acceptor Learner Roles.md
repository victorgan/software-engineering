# Proposer Acceptor Learner Roles

> <- Back to [[Paxos]]

Paxos defines three roles: Proposers suggest values, Acceptors vote on proposals (a value is chosen when a majority of acceptors agree), and Learners learn the chosen value. In practice, a single node often plays multiple roles. The separation of concerns enables formal correctness proofs.

#distributed-systems #consensus
