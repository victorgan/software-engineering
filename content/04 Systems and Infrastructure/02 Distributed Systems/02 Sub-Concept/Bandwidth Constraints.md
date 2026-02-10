# Bandwidth Constraints

> <- Back to [[Fallacies of Distributed Computing]]

Network bandwidth is finite and shared. Moving large amounts of data between services or regions takes time and costs money. Design systems to minimize data transfer: send only what is needed, compress data, use efficient serialization (Protocol Buffers vs JSON), and co-locate data with computation.

#distributed-systems #fundamentals
