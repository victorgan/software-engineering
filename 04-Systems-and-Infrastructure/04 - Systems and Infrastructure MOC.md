# 04 — Systems & Infrastructure MOC

> ← Back to [[Software Engineering - Map of Content]]

The machines, networks, and platforms that run our software. Understanding these is what separates engineers who can build systems that scale from those who can't.

---

## [[Operating Systems]]

### Processes & Threads
- **Process** — Independent execution unit, own memory space, PID
- **Thread** — Lightweight execution within a process, shared memory
- **Process Lifecycle** — Created, ready, running, waiting, terminated
- **Context Switching** — Saving/restoring state, CPU overhead
- **Inter-Process Communication (IPC)** — Pipes, sockets, shared memory, message queues, signals
- **Green Threads / Fibers** — User-space threads, cooperative scheduling (Go goroutines, Erlang processes)
- **Coroutines** — Cooperative multitasking, yield points (Python async, Kotlin coroutines)

### CPU Scheduling
- **Preemptive vs Cooperative** — OS-controlled vs voluntary yielding
- **Algorithms** — FIFO, Shortest Job First, Round Robin, Priority, Multilevel Feedback Queue
- **Real-Time Scheduling** — Hard vs soft real-time, rate monotonic, EDF

### Memory Management
- **Virtual Memory** — Address translation, page tables, TLB (Translation Lookaside Buffer)
- **Paging** — Fixed-size pages, page faults, demand paging, page replacement (LRU, Clock)
- **Segmentation** — Variable-size segments, logical grouping
- **Memory-Mapped Files** — mmap, zero-copy I/O
- **Kernel vs User Space** — Privilege levels, system calls, mode switching
- **OOM Killer** — Linux out-of-memory handling, cgroups memory limits

### File Systems
- **Concepts** — Inodes, directories, file descriptors, hard/soft links
- **Journaling** — Write-ahead logging for crash recovery (ext4, XFS, NTFS)
- **Copy-on-Write** — ZFS, Btrfs, snapshot support
- **VFS (Virtual File System)** — Abstraction layer, mount points
- **Distributed File Systems** — NFS, HDFS, GlusterFS, Ceph
- **I/O Models** — Blocking, non-blocking, I/O multiplexing (select, poll, epoll, kqueue), async I/O (io_uring)

### Linux Internals (commonly needed)
- **Namespaces** — PID, network, mount, user — basis of containers
- **cgroups** — Resource limits (CPU, memory, I/O) — basis of containers
- **systemd** — Init system, service management, units, journald
- **eBPF** — Programmable kernel tracing, networking, security
- **Signals** — SIGTERM, SIGKILL, SIGHUP, signal handling

---

## [[Networking]]

### OSI / TCP-IP Model
- **Physical Layer** — Cables, wireless, electrical signals
- **Data Link Layer** — Ethernet, MAC addresses, ARP, switches
- **Network Layer** — IP (IPv4, IPv6), routing, ICMP, subnetting, CIDR
- **Transport Layer** — TCP (reliable, ordered), UDP (fast, unreliable), QUIC
- **Application Layer** — HTTP, DNS, SMTP, FTP, SSH, TLS

### TCP Deep Dive
- **Three-Way Handshake** — SYN, SYN-ACK, ACK
- **Flow Control** — Sliding window, receiver window
- **Congestion Control** — Slow start, congestion avoidance, fast retransmit (Reno, Cubic, BBR)
- **Connection Termination** — FIN, TIME_WAIT, lingering sockets
- **Keep-Alive** — Persistent connections, connection pooling

### HTTP
- **HTTP/1.1** — Keep-alive, pipelining, chunked transfer
- **HTTP/2** — Multiplexing, header compression (HPACK), server push, streams
- **HTTP/3** — QUIC-based, UDP transport, 0-RTT connection setup
- **Methods** — GET, POST, PUT, PATCH, DELETE, OPTIONS, HEAD
- **Status Codes** — 2xx success, 3xx redirect, 4xx client error, 5xx server error
- **Headers** — Content-Type, Authorization, Cache-Control, CORS headers
- **Cookies & Sessions** — Stateful interactions, SameSite, Secure, HttpOnly flags

### DNS
- **Resolution Process** — Recursive resolver → root → TLD → authoritative
- **Record Types** — A, AAAA, CNAME, MX, TXT, NS, SOA, SRV
- **TTL** — Caching duration, propagation delays
- **DNS Security** — DNSSEC, DNS-over-HTTPS (DoH), DNS-over-TLS (DoT)

### Load Balancing
- **Layer 4 (Transport)** — TCP/UDP level, fast, connection-based (HAProxy, NLB)
- **Layer 7 (Application)** — HTTP level, content-based routing, header inspection (Nginx, ALB, Envoy)
- **Algorithms** — Round robin, weighted round robin, least connections, IP hash, consistent hashing
- **Health Checks** — Active (probing) vs passive (monitoring responses)
- **Session Affinity / Sticky Sessions** — Route same user to same backend

### CDN (Content Delivery Networks)
- **Edge Caching** — Serve content from geographically close servers
- **Origin Shield** — Intermediate cache layer to protect origin
- **Cache Invalidation** — Purge, versioned URLs, cache-control headers
- **Providers** — Cloudflare, AWS CloudFront, Akamai, Fastly

### Other Networking Topics
- **WebSockets** — Full-duplex, persistent connection, real-time communication
- **gRPC** — HTTP/2 based, Protocol Buffers, bidirectional streaming (see [[API Design]])
- **Service Mesh** — Istio, Linkerd, sidecar proxies, mTLS, traffic management
- **API Gateway** — Rate limiting, auth, routing, transformation (Kong, AWS API Gateway)
- **NAT, Firewalls, VPNs** — Network segmentation, port forwarding, WireGuard

---

## [[Distributed Systems]]

### Fundamental Concepts
- **CAP Theorem** — Consistency, Availability, Partition Tolerance — pick two (practically: CP or AP)
- **PACELC Theorem** — Extension of CAP — when no partition: latency vs consistency tradeoff
- **Fallacies of Distributed Computing** — Network is reliable, latency is zero, bandwidth is infinite, etc.
- **Distributed Time** — No global clock, logical clocks (Lamport), vector clocks, hybrid logical clocks

### Consistency Models
- **Strong Consistency** — Reads always return most recent write (linearizability)
- **Sequential Consistency** — All processes see same order
- **Causal Consistency** — Causally related operations are ordered
- **Eventual Consistency** — Given time, all replicas converge
- **Read-Your-Writes** — You always see your own writes

### Consensus Algorithms
- **Paxos** — Classic, complex, foundational
- **Raft** — Understandable consensus, leader election, log replication (used in etcd, CockroachDB)
- **Zab** — ZooKeeper Atomic Broadcast
- **Byzantine Fault Tolerance** — Handling malicious nodes (PBFT, used in blockchain)

### Replication
- **Single-Leader** — One writer, read replicas, replication lag
- **Multi-Leader** — Multiple writers, conflict resolution (last-writer-wins, CRDTs)
- **Leaderless** — Quorum reads/writes, read repair, anti-entropy (Dynamo-style: Cassandra, Riak)
- **CRDTs (Conflict-Free Replicated Data Types)** — Merge without coordination (G-Counter, OR-Set)

### Partitioning / Sharding
- **Range-Based** — Partition by key ranges, risk of hotspots
- **Hash-Based** — Partition by hash of key, even distribution
- **Consistent Hashing** — Minimal redistribution on node changes
- **Cross-Partition Queries** — Scatter-gather, denormalization
- **Rebalancing** — Adding/removing nodes, data migration

### Message Queues & Event Systems
- **Point-to-Point** — One consumer per message (SQS, RabbitMQ work queues)
- **Pub/Sub** — Multiple subscribers per message (Kafka topics, SNS, Google Pub/Sub)
- **Message Ordering** — FIFO queues, partition-level ordering
- **Delivery Guarantees** — At-most-once, at-least-once, exactly-once (hardest)
- **Dead Letter Queues** — Failed message handling, retry policies
- **Backpressure** — Slow consumers, flow control

### Distributed System Patterns
- **Circuit Breaker** — Prevent cascading failures, fail fast
- **Bulkhead** — Isolate failures, limit blast radius
- **Retry with Exponential Backoff** — Jitter, max retries, idempotency
- **Saga Pattern** — Distributed transactions via compensating actions
- **Sidecar Pattern** — Co-located helper process (basis of service mesh)
- **Leader Election** — ZooKeeper, etcd, Raft-based

---

## [[Cloud and Containers]]

### Containerization
- **Docker** — Images, containers, Dockerfile, layers, multi-stage builds
- **Container Registries** — Docker Hub, ECR, GCR, GHCR
- **Container Networking** — Bridge, host, overlay networks
- **Container Storage** — Volumes, bind mounts, tmpfs
- **Security** — Rootless containers, image scanning, secrets management

### Container Orchestration
- **Kubernetes (K8s)** — Pods, Deployments, Services, Ingress, ConfigMaps, Secrets
- **K8s Networking** — ClusterIP, NodePort, LoadBalancer, network policies
- **K8s Storage** — PersistentVolumes, PersistentVolumeClaims, StorageClasses
- **K8s Scaling** — HPA (Horizontal Pod Autoscaler), VPA, Cluster Autoscaler
- **Helm** — Package manager for K8s, charts, values, releases
- **Operators** — Custom controllers, CRDs (Custom Resource Definitions)
- **Service Mesh on K8s** — Istio, Linkerd, sidecar injection

### Cloud Providers (AWS as canonical example)
- **Compute** — EC2, Lambda, ECS, EKS, Fargate
- **Storage** — S3, EBS, EFS, Glacier
- **Databases** — RDS, Aurora, DynamoDB, ElastiCache, Redshift
- **Networking** — VPC, subnets, security groups, Route53, CloudFront, ALB/NLB
- **Messaging** — SQS, SNS, EventBridge, Kinesis
- **Identity** — IAM, roles, policies, STS, Cognito

### Infrastructure as Code (IaC)
- **Terraform** — Declarative, provider-agnostic, state management, modules
- **AWS CloudFormation** — AWS-native, stacks, drift detection
- **Pulumi** — IaC in general-purpose languages (TypeScript, Python, Go)
- **Ansible** — Configuration management, playbooks, idempotent
- **GitOps** — Argo CD, Flux — Git as source of truth for infrastructure

### Serverless
- **Functions as a Service (FaaS)** — AWS Lambda, Google Cloud Functions, Azure Functions
- **Cold Starts** — Latency on first invocation, provisioned concurrency
- **Event-Driven** — Trigger on HTTP, queue messages, file uploads, schedules
- **Limitations** — Execution time limits, stateless, vendor lock-in
- **Serverless Frameworks** — Serverless Framework, SAM, SST

---

#systems #infrastructure #distributed-systems #cloud #containers
