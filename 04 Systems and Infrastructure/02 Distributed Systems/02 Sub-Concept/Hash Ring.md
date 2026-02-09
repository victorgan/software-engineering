# Hash Ring

> <- Back to [[Consistent Hashing]]

Both keys and nodes are mapped to positions on a circular hash space (0 to 2^32-1). Each key is assigned to the first node encountered moving clockwise from the key's position. When a node is added or removed, only the keys between it and its predecessor are affected.

#distributed-systems #sharding
