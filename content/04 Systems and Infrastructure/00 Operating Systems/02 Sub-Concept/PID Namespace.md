# PID Namespace

> <- Back to [[Namespaces]]

Isolates process ID number spaces so that processes in different namespaces can have the same PID. The first process in a PID namespace becomes PID 1 (init) for that namespace. This is how containers see their own process tree independently from the host.

#operating-systems #linux #containers
