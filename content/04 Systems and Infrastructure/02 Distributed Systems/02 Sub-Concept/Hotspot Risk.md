# Hotspot Risk

> <- Back to [[Range-Based Partitioning]]

Certain key ranges may receive disproportionate traffic, overloading a single partition. For example, time-series data with a timestamp key concentrates all recent writes on one partition. Mitigation: add a prefix/suffix to spread load, or use compound partition keys.

#distributed-systems #sharding
