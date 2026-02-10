# 11 — Cloud Providers & Proprietary Systems MOC

> ← Back to [[Software Engineering - Map of Content]]

Vendor-specific cloud services and proprietary internal systems. These are practical reference material for working with specific platforms — distinct from the universal concepts in [[04 - Systems and Infrastructure MOC]].

---

## [[AWS Services Guide]]

*Each service mapped to the concept it implements.*

### Compute
- **EC2 (Elastic Compute Cloud)** — Virtual machines (instances), instance types, AMIs, spot/reserved/on-demand pricing → [[Operating Systems]] processes
- **Lambda** — Serverless functions, event-driven, pay-per-invocation, 15min max → Serverless / FaaS
- **ECS (Elastic Container Service)** — Docker container orchestration (AWS-native), tasks, services → [[Cloud and Containers]]
- **EKS (Elastic Kubernetes Service)** — Managed Kubernetes control plane → [[Cloud and Containers]] / K8s
- **Fargate** — Serverless compute for containers (ECS/EKS), no instance management → Serverless containers
- **Elastic Beanstalk** — PaaS, deploy code directly, auto-manages infra → Simplified deployment
- **App Runner** — Fully managed container service, simpler than ECS, from source or image → PaaS for containers
- **Batch** — Managed batch processing, job queues, compute environments → Batch workloads

### Storage
- **S3 (Simple Storage Service)** — Object storage, buckets, versioning, lifecycle policies, storage classes (Standard, IA, Glacier) → Object storage / Data lake
- **EBS (Elastic Block Store)** — Block storage volumes attached to EC2, SSD (gp3, io2) vs HDD (st1, sc1) → VM disk storage
- **EFS (Elastic File System)** — Managed NFS, shared across instances, auto-scaling → [[Operating Systems]] / distributed file systems
- **S3 Glacier / Glacier Deep Archive** — Cold archival storage, minutes-to-hours retrieval → Long-term backup
- **FSx** — Managed Windows File Server (SMB) or Lustre (HPC) file systems → Specialized file storage

### Databases
- **RDS (Relational Database Service)** — Managed PostgreSQL, MySQL, MariaDB, Oracle, SQL Server. Automated backups, read replicas, Multi-AZ failover → [[Relational Databases]]
- **Aurora** — AWS-built MySQL/Postgres-compatible, 5x throughput vs standard, auto-scaling storage, Aurora Serverless → High-performance relational
- **DynamoDB** — Managed NoSQL key-value/document, single-digit ms latency, auto-scaling, global tables → [[NoSQL Databases]] / key-value
- **ElastiCache** — Managed Redis or Memcached → [[Caching]] / in-memory
- **Redshift** — Columnar data warehouse, massively parallel, Redshift Serverless → [[Data Pipelines]] / data warehouse
- **Neptune** — Managed graph database (Gremlin + SPARQL) → [[NoSQL Databases]] / graph
- **DocumentDB** — MongoDB-compatible managed document DB → [[NoSQL Databases]] / document
- **Timestream** — Managed time-series database → [[NoSQL Databases]] / time-series
- **MemoryDB** — Redis-compatible with durability (replaces Redis + persistence) → Durable in-memory
- **Keyspaces** — Managed Cassandra-compatible → [[NoSQL Databases]] / column-family
- **OpenSearch Service** — Managed Elasticsearch/OpenSearch → Search / [[Observability]] log analytics

### Networking
- **VPC (Virtual Private Cloud)** — Isolated network, subnets (public/private), route tables, internet/NAT gateways → [[Networking]] / network segmentation
- **Security Groups** — Stateful firewall rules per instance/resource → Network security
- **NACLs (Network ACLs)** — Stateless subnet-level firewall → Network security
- **ALB (Application Load Balancer)** — Layer 7, HTTP routing, path/host-based rules, gRPC support → [[Networking]] / load balancing
- **NLB (Network Load Balancer)** — Layer 4, TCP/UDP, ultra-low latency, static IPs → [[Networking]] / load balancing
- **Route 53** — DNS service, health checks, routing policies (latency, geolocation, failover, weighted) → [[Networking]] / DNS
- **CloudFront** — CDN, edge caching, Lambda@Edge for edge compute → [[Networking]] / CDN
- **API Gateway** — REST/WebSocket API management, throttling, auth, caching → [[API Design]]
- **PrivateLink** — Private connectivity to AWS services or between VPCs without internet → Network segmentation
- **Transit Gateway** — Connect multiple VPCs and on-premises networks → Hub-and-spoke networking
- **Global Accelerator** — Anycast IPs, route traffic to optimal region → Global load balancing

### Messaging & Events
- **SQS (Simple Queue Service)** — Managed message queue, standard (best-effort order) vs FIFO (exactly-once, ordered) → [[Distributed Systems]] / message queues
- **SNS (Simple Notification Service)** — Pub/sub, fan-out to multiple subscribers (SQS, Lambda, HTTP, email) → [[Distributed Systems]] / pub-sub
- **EventBridge** — Serverless event bus, event routing rules, schema registry, SaaS integrations → Event-driven architecture
- **Kinesis Data Streams** — Real-time data streaming, shards, 1-7 day retention → [[Data Pipelines]] / stream processing
- **Kinesis Firehose** — Deliver streaming data to S3, Redshift, OpenSearch → Stream-to-storage
- **MSK (Managed Streaming for Kafka)** — Managed Apache Kafka → [[Data Pipelines]] / Kafka
- **Step Functions** — Serverless workflow orchestration, state machines, saga pattern → [[Distributed Systems]] / saga

### Security & Identity
- **IAM (Identity and Access Management)** — Users, groups, roles, policies (JSON), least privilege → [[Authentication and Authorization]]
- **STS (Security Token Service)** — Temporary credentials, assume role, cross-account access → Federated identity
- **Cognito** — User authentication/signup, user pools (identity), identity pools (access to AWS), social login → [[Authentication and Authorization]]
- **KMS (Key Management Service)** — Managed encryption keys, envelope encryption, key rotation → [[Cryptography]]
- **Secrets Manager** — Store/rotate secrets (DB passwords, API keys), automatic rotation → [[Infrastructure Security]]
- **Certificate Manager (ACM)** — Free TLS certificates, auto-renewal, ALB/CloudFront integration → [[Cryptography]] / TLS
- **WAF (Web Application Firewall)** — Layer 7 protection, SQL injection, XSS, rate limiting rules → [[Application Security]]
- **GuardDuty** — Threat detection, anomaly detection across accounts → Threat monitoring
- **Security Hub** — Centralized security findings, compliance checks → Security posture

### Observability
- **CloudWatch** — Metrics, logs, alarms, dashboards, Log Insights (query language) → [[Observability]] / metrics and logs
- **X-Ray** — Distributed tracing, service map → [[Observability]] / distributed tracing
- **CloudTrail** — API call audit logging, who did what when → Security auditing

### Data & Analytics
- **Athena** — Serverless SQL queries on S3 data (Presto-based) → Ad-hoc analytics
- **Glue** — Managed ETL, data catalog, schema discovery, Spark-based → [[Data Pipelines]] / ETL
- **EMR (Elastic MapReduce)** — Managed Hadoop/Spark/Flink clusters → [[Data Pipelines]] / batch processing
- **Lake Formation** — Data lake setup, permissions, governance → [[Data Pipelines]] / data governance
- **QuickSight** — BI/visualization, dashboards, SPICE in-memory engine → Business intelligence

### ML & AI
- **SageMaker** — End-to-end ML platform: notebooks, training, deployment, model registry → [[MLOps]]
- **Bedrock** — Managed foundation models (Claude, Titan, Llama), RAG, fine-tuning → [[Natural Language Processing]] / LLMs
- **Rekognition / Comprehend / Textract / Polly / Transcribe** — Pre-built AI APIs (vision, NLP, OCR, speech) → AI services

---

## [[GCP Services Guide]]

*Each service mapped to the concept it implements. GCP equivalents to AWS noted where applicable.*

### Compute
- **Compute Engine** — Virtual machines, machine types, preemptible/spot VMs, sole-tenant nodes → [[Operating Systems]] processes *(≈ EC2)*
- **Cloud Functions** — Serverless functions, event-driven, HTTP or event triggers → Serverless / FaaS *(≈ Lambda)*
- **Cloud Run** — Serverless containers, auto-scales to zero, any language/framework, built on Knative → Serverless containers *(≈ Fargate + App Runner)*
- **GKE (Google Kubernetes Engine)** — Managed Kubernetes, Autopilot mode (fully managed nodes), multi-cluster → [[Cloud and Containers]] / K8s *(≈ EKS)*
- **App Engine** — PaaS, standard (sandboxed) and flexible (custom Docker) environments → PaaS *(≈ Elastic Beanstalk)*
- **Batch** — Managed batch jobs, built on Compute Engine → Batch workloads *(≈ AWS Batch)*

### Storage
- **Cloud Storage (GCS)** — Object storage, buckets, storage classes (Standard, Nearline, Coldline, Archive), versioning → Object storage / data lake *(≈ S3)*
- **Persistent Disk** — Block storage for Compute Engine, SSD (pd-ssd) vs balanced (pd-balanced) vs standard → VM disk storage *(≈ EBS)*
- **Filestore** — Managed NFS → Shared file storage *(≈ EFS)*

### Databases
- **Cloud SQL** — Managed PostgreSQL, MySQL, SQL Server. Automated backups, read replicas, high availability → [[Relational Databases]] *(≈ RDS)*
- **AlloyDB** — Postgres-compatible, Google-built, columnar engine for analytics mixed with transactions → High-performance relational *(≈ Aurora)*
- **Cloud Spanner** — Globally distributed relational DB, strong consistency, horizontal scaling, SQL. Used by Google internally → Distributed SQL *(no direct AWS equivalent; closest: Aurora Global)*
- **Firestore** — Serverless NoSQL document DB, real-time sync, offline support, strong consistency → [[NoSQL Databases]] / document *(≈ DynamoDB, but document-oriented)*
- **Bigtable** — Managed wide-column NoSQL, HBase-compatible API, low latency at massive scale → [[NoSQL Databases]] / column-family *(≈ Keyspaces/DynamoDB for wide-column)*
- **Memorystore** — Managed Redis and Memcached → [[Caching]] / in-memory *(≈ ElastiCache)*
- **BigQuery** — Serverless data warehouse, SQL, petabyte-scale, columnar, built-in ML (BQML), streaming inserts → [[Data Pipelines]] / data warehouse *(≈ Redshift, but serverless)*

### Networking
- **VPC** — Virtual private cloud, subnets, firewall rules, shared VPC across projects → [[Networking]] / network segmentation *(≈ AWS VPC)*
- **Cloud Load Balancing** — Global L7 (HTTP/S), regional L4 (TCP/UDP), internal, auto-scaling backends → [[Networking]] / load balancing *(≈ ALB + NLB)*
- **Cloud DNS** — Managed DNS, DNSSEC → [[Networking]] / DNS *(≈ Route 53)*
- **Cloud CDN** — Content delivery, edge caching, integrated with load balancer → [[Networking]] / CDN *(≈ CloudFront)*
- **Cloud Armor** — DDoS protection and WAF for HTTP(S) load balancers → [[Application Security]] *(≈ AWS WAF + Shield)*
- **Cloud NAT** — Managed NAT for outbound traffic from private instances → Network address translation
- **Private Service Connect** — Private connectivity to Google services and between VPCs → Network segmentation *(≈ PrivateLink)*
- **API Gateway / Apigee** — API management. API Gateway: lightweight, serverless. Apigee: full-featured, enterprise API platform → [[API Design]] *(≈ AWS API Gateway)*

### Messaging & Events
- **Pub/Sub** — Managed message/event streaming, at-least-once delivery, push/pull subscriptions, ordering, dead letter → [[Distributed Systems]] / pub-sub *(≈ SNS + SQS + Kinesis combined)*
- **Cloud Tasks** — Managed task queue, rate-controlled execution, retry policies → Async task execution *(≈ SQS + Lambda triggers)*
- **Eventarc** — Event routing from Google Cloud sources, Cloud Audit Logs, Pub/Sub to Cloud Run/Functions → Event-driven architecture *(≈ EventBridge)*
- **Workflows** — Serverless workflow orchestration, YAML/JSON definitions → Workflow orchestration *(≈ Step Functions)*
- **Dataflow** — Managed Apache Beam, batch and stream processing, auto-scaling → [[Data Pipelines]] / stream processing *(≈ Kinesis + EMR for streaming)*

### Security & Identity
- **Cloud IAM** — Resource-level permissions, roles (basic, predefined, custom), service accounts, policy hierarchy (org → folder → project) → [[Authentication and Authorization]] *(≈ IAM)*
- **Identity Platform** — User authentication, multi-tenancy, social login, MFA → [[Authentication and Authorization]] *(≈ Cognito)*
- **Cloud KMS** — Managed encryption keys, HSM-backed, key rotation → [[Cryptography]] *(≈ KMS)*
- **Secret Manager** — Store and access secrets, versioning, automatic rotation → [[Infrastructure Security]] *(≈ Secrets Manager)*
- **Certificate Authority Service** — Private CA, issue/manage certificates → [[Cryptography]] / PKI *(≈ ACM Private CA)*
- **Security Command Center** — Centralized security findings, vulnerability scanning, compliance → Security posture *(≈ Security Hub)*

### Observability
- **Cloud Monitoring** — Metrics, dashboards, alerting, uptime checks → [[Observability]] / metrics *(≈ CloudWatch Metrics)*
- **Cloud Logging** — Centralized logs, log-based metrics, sinks to BigQuery/GCS/Pub/Sub → [[Observability]] / logs *(≈ CloudWatch Logs)*
- **Cloud Trace** — Distributed tracing, latency analysis → [[Observability]] / distributed tracing *(≈ X-Ray)*
- **Cloud Profiler** — Continuous CPU/memory profiling in production → [[Performance Engineering]] / profiling
- **Audit Logs** — Who did what, where, when → Security auditing *(≈ CloudTrail)*

### Data & Analytics
- **BigQuery** — (see Databases above) Also serves as the primary analytics engine. Serverless, ML integration, BI Engine for dashboards.
- **Dataproc** — Managed Hadoop/Spark clusters → [[Data Pipelines]] / batch processing *(≈ EMR)*
- **Dataflow** — (see Messaging above) Managed Apache Beam for ETL/stream → [[Data Pipelines]] *(≈ Glue + Kinesis Analytics)*
- **Data Catalog** — Metadata management, data discovery, policy tags → [[Data Pipelines]] / data governance *(≈ Glue Data Catalog)*
- **Composer** — Managed Apache Airflow, DAG-based workflow orchestration → [[Data Pipelines]] / orchestration *(≈ MWAA / managed Airflow)*
- **Looker / Looker Studio** — BI and visualization → Business intelligence *(≈ QuickSight)*
- **Dataplex** — Data lake management, governance, discovery across distributed data → Data lake governance *(≈ Lake Formation)*

### ML & AI
- **Vertex AI** — Unified ML platform: notebooks, training, AutoML, model registry, deployment, pipelines → [[MLOps]] *(≈ SageMaker)*
- **Vertex AI Studio / Model Garden** — Access to Gemini, PaLM, open models, prompt design → [[Natural Language Processing]] / LLMs *(≈ Bedrock)*
- **Vision AI / Natural Language AI / Speech-to-Text / Text-to-Speech** — Pre-built AI APIs → AI services *(≈ Rekognition/Comprehend/Transcribe/Polly)*
- **TPUs (Tensor Processing Units)** — Custom ML accelerators, available as Cloud TPU VMs → [[Deep Learning]] / training at scale *(no AWS equivalent; closest: Trainium/Inferentia)*

---

## [[AWS vs GCP — Service Mapping]]

| Concept | AWS | GCP |
|---|---|---|
| VMs | EC2 | Compute Engine |
| Serverless Functions | Lambda | Cloud Functions |
| Serverless Containers | Fargate / App Runner | Cloud Run |
| Managed K8s | EKS | GKE |
| Object Storage | S3 | Cloud Storage (GCS) |
| Block Storage | EBS | Persistent Disk |
| Managed RDBMS | RDS | Cloud SQL |
| High-Perf Relational | Aurora | AlloyDB |
| Global Distributed SQL | — | Cloud Spanner |
| NoSQL Document/KV | DynamoDB | Firestore |
| Wide-Column NoSQL | Keyspaces | Bigtable |
| In-Memory Cache | ElastiCache | Memorystore |
| Data Warehouse | Redshift | BigQuery |
| Search | OpenSearch Service | — (use Elastic Cloud on GCP) |
| Message Queue | SQS | Pub/Sub (pull) / Cloud Tasks |
| Pub/Sub | SNS | Pub/Sub |
| Event Bus | EventBridge | Eventarc |
| Stream Processing | Kinesis | Dataflow (Beam) |
| Managed Kafka | MSK | — (use Confluent on GCP) |
| Workflow Orchestration | Step Functions | Workflows |
| Managed Airflow | MWAA | Composer |
| ETL | Glue | Dataflow |
| Managed Spark/Hadoop | EMR | Dataproc |
| CDN | CloudFront | Cloud CDN |
| DNS | Route 53 | Cloud DNS |
| Load Balancer (L7) | ALB | Cloud Load Balancing (HTTP/S) |
| Load Balancer (L4) | NLB | Cloud Load Balancing (TCP/UDP) |
| API Management | API Gateway | Apigee / API Gateway |
| WAF | AWS WAF | Cloud Armor |
| IAM | IAM | Cloud IAM |
| User Auth | Cognito | Identity Platform |
| Secrets | Secrets Manager | Secret Manager |
| Encryption Keys | KMS | Cloud KMS |
| Metrics/Alerts | CloudWatch | Cloud Monitoring |
| Logs | CloudWatch Logs | Cloud Logging |
| Tracing | X-Ray | Cloud Trace |
| Audit Logs | CloudTrail | Audit Logs |
| ML Platform | SageMaker | Vertex AI |
| Foundation Models | Bedrock | Vertex AI Studio / Model Garden |
| IaC (native) | CloudFormation | Deployment Manager |
| BI / Dashboards | QuickSight | Looker Studio |

---

## [[Google Internal Technologies]]

*Google's internal stack predates most open-source and cloud equivalents. Many industry standards were directly inspired by Google's internal systems. Understanding these is valuable for working at Google, where the internal stack is the primary development environment.*

### Compute & Orchestration
- **Borg** — Cluster management and container orchestration. Runs nearly all Google workloads. Inspired → **Kubernetes** (external), GKE (GCP). Concept: [[Cloud and Containers]] / container orchestration.
- **Omega** — Next-gen cluster scheduler research (shared-state scheduling). Influenced → K8s scheduler design.
- **Tupperware (Meta) vs Borg** — Meta's equivalent; Borg is Google's. Both manage millions of containers across data centers.

### Storage
- **Colossus** — Google's distributed file system (successor to GFS). Underpins nearly every Google storage service. Inspired → **HDFS** (Hadoop Distributed File System). Concept: [[Operating Systems]] / distributed file systems.
- **GFS (Google File System)** — Original distributed file system (2003 paper). Append-optimized, large files. Directly inspired → **HDFS**. Concept: [[Operating Systems]] / distributed file systems.

### Databases & Data
- **Bigtable (internal)** — Wide-column distributed storage. The original (2006 paper). Externalized as → **Cloud Bigtable** (GCP). Inspired → **HBase**, **Cassandra** (partially). Concept: [[NoSQL Databases]] / column-family.
- **Spanner** — Globally distributed, strongly consistent relational database with TrueTime (atomic clocks + GPS). Externalized as → **Cloud Spanner** (GCP). Inspired → **CockroachDB**, **YugabyteDB**. Concept: [[Relational Databases]] / distributed SQL.
- **F1** — Distributed SQL query engine built on Spanner. Powers Google Ads. Concept: distributed relational queries.
- **Megastore** — Predecessor to Spanner, combined NoSQL scalability with SQL-like features. Historical significance.
- **Mesa** — Highly scalable, highly available data warehousing system for Google Ads metrics. Near real-time aggregation. Concept: [[Data Pipelines]] / data warehouse.
- **Napa** — Cloud-native data warehouse system powering BigQuery and other services. Concept: serverless analytics.

### Search & Indexing
- **Caffeine** — Google's web indexing infrastructure, continuous (near real-time) indexing. Concept: search indexing.
- **Mustang** — Google's web search serving system. Concept: distributed search.

### RPC & Networking
- **Stubby** — Google's internal RPC framework. Externalized as → **gRPC** (open source). Concept: [[Networking]] / RPC, [[API Design]].
- **GSLB (Global Software Load Balancer)** — Google's global load balancing. Externalized as → **Cloud Load Balancing** (GCP). Concept: [[Networking]] / load balancing.
- **Maglev** — Google's network load balancer (2016 paper). Software-defined, ECMP-based. Concept: [[Networking]] / L4 load balancing.
- **B4** — Google's private WAN (software-defined networking between data centers). OpenFlow-based. Concept: [[Networking]] / SDN.
- **Andromeda** — Google's network virtualization stack. Underpins GCP VPC networking. Concept: [[Networking]] / virtual networking.

### Messaging & Streaming
- **Pub/Sub (internal)** — Google's internal messaging system. Externalized as → **Cloud Pub/Sub** (GCP). Industry equivalent: **Kafka**, **RabbitMQ**, **SQS/SNS**. Concept: [[Distributed Systems]] / message queues.

### Data Processing
- **MapReduce** — Original distributed data processing framework (2004 paper). Externalized → **Hadoop MapReduce**. Superseded internally by Flume. Concept: [[Data Pipelines]] / batch processing.
- **FlumeJava / Flume** — Successor to MapReduce at Google. Pipeline-based data processing. Externalized as → **Apache Beam** (unified batch/stream API), **Dataflow** (GCP). Concept: [[Data Pipelines]].
- **MillWheel** — Stream processing framework (2013 paper). Low-latency, exactly-once. Influenced → **Apache Beam** streaming model, **Dataflow** (GCP). Concept: [[Data Pipelines]] / stream processing.
- **Dremel** — Interactive query engine for nested data (2010 paper). Columnar storage, tree-shaped execution. Externalized as → **BigQuery** (GCP). Inspired → **Apache Drill**, **Presto/Trino**, **Apache Impala**. Concept: [[Data Pipelines]] / analytics.

### Build & Development
- **Blaze** — Google's build system. Externalized as → **Bazel** (open source). Hermetic builds, caching, remote execution. Concept: [[CI-CD]] / build systems.
- **Piper** — Google's monorepo (single code repository for almost all Google code, billions of lines). Managed via CitC (Clients in the Cloud). Concept: [[Version Control]] / monorepo.
- **Critique** — Google's code review tool. Industry equivalent: **GitHub PRs**, **Gerrit** (open source, also from Google). Concept: [[Code Quality]] / code review.
- **Gerrit** — Open-source code review tool (originated at Google for Android). Concept: [[Code Quality]] / code review.
- **Tricorder** — Static analysis platform integrated into code review (Critique). Concept: [[Code Quality]] / static analysis.
- **TAP (Test Automation Platform)** — Continuous testing at scale, runs affected tests on every change. Concept: [[Testing]] / CI testing.
- **Forge** — Google's distributed build service. Remote execution and caching. Concept: [[CI-CD]] / distributed builds.

### Monitoring & Operations
- **Borgmon** — Google's monitoring system (monitors Borg workloads). Externalized as → **Prometheus** (directly inspired). Concept: [[Observability]] / metrics.
- **Dapper** — Google's distributed tracing system (2010 paper). Inspired → **Zipkin**, **Jaeger**, **OpenTelemetry**. Externalized as → **Cloud Trace** (GCP). Concept: [[Observability]] / distributed tracing.
- **Monarch** — Google's internal time-series database for monitoring. Backs Cloud Monitoring. Concept: [[Observability]] / metrics storage.
- **Sponge** — Test results storage and analysis. Concept: test analytics.

### Machine Learning
- **TensorFlow** — Originally internal, open-sourced 2015. Deep learning framework. Concept: [[Deep Learning]].
- **TPUs (Tensor Processing Units)** — Custom ASICs for ML training and inference. Available externally via GCP. Concept: [[Deep Learning]] / hardware acceleration.
- **Vizier** — Hyperparameter tuning service. Externalized as → **Vertex AI Vizier** (GCP). Open source: **OSS Vizier**. Concept: [[MLOps]] / hyperparameter optimization.
- **TFX (TensorFlow Extended)** — End-to-end ML pipeline framework. Open-sourced. Concept: [[MLOps]] / ML pipelines.

### Security & Identity
- **BeyondCorp** — Google's zero-trust security model (no VPN, identity-based access). Inspired the industry zero-trust movement. Externalized as → **BeyondCorp Enterprise** (GCP). Concept: [[Infrastructure Security]] / zero trust.
- **ALTS (Application Layer Transport Security)** — Google's mutual TLS for internal RPC. All service-to-service communication authenticated. Concept: [[Cryptography]] / mTLS.
- **Zanzibar** — Google's global authorization system (consistent, scalable relationship-based access control). Inspired → **SpiceDB**, **Authzed**, **OpenFGA**, **Ory Keto**. Concept: [[Authentication and Authorization]] / ReBAC.
- **Titan** — Custom security chip in Google servers and Pixel devices. Hardware root of trust. Concept: [[Infrastructure Security]] / hardware security.

### Configuration & Deployment
- **Rapid** — Google's release and deployment system. Manages rollouts across Borg. Concept: [[CI-CD]] / deployment.
- **Borg Config (BCL)** — Configuration language for Borg jobs. Evolved to → **GCL (Generic Config Language)** → **Jsonnet** (open-sourced) → influenced **CUE** language. Concept: configuration management.
- **GSLB + Traffic Director** — Gradual rollout, canary deployments, traffic shifting at global scale. Concept: [[CI-CD]] / deployment strategies.

---

## [[Google Internal → External Mapping]]

| Google Internal | Open Source / Industry | GCP External | Concept |
|---|---|---|---|
| Borg | Kubernetes | GKE | Container orchestration |
| Colossus / GFS | HDFS | — | Distributed file system |
| Bigtable | HBase, Cassandra | Cloud Bigtable | Wide-column NoSQL |
| Spanner | CockroachDB, YugabyteDB | Cloud Spanner | Distributed SQL |
| Dremel | Presto/Trino, Apache Drill | BigQuery | Interactive analytics |
| MapReduce | Hadoop MapReduce | — (legacy) | Batch processing |
| FlumeJava | Apache Beam | Dataflow | Data pipelines |
| MillWheel | Apache Beam (streaming) | Dataflow | Stream processing |
| Stubby | gRPC | — | RPC framework |
| Borgmon | Prometheus | Cloud Monitoring | Metrics collection |
| Dapper | Zipkin, Jaeger, OpenTelemetry | Cloud Trace | Distributed tracing |
| Blaze | Bazel | — | Build system |
| Chubby | ZooKeeper, etcd | — | Distributed lock service |
| Pub/Sub (internal) | Kafka, RabbitMQ | Cloud Pub/Sub | Messaging |
| BeyondCorp | Zero-trust frameworks | BeyondCorp Enterprise | Zero-trust security |
| Zanzibar | SpiceDB, OpenFGA | — | Authorization |
| TensorFlow | TensorFlow (itself) | Vertex AI | ML framework |
| Jsonnet (from BCL/GCL) | Jsonnet, CUE | — | Configuration language |
| Critique | Gerrit, GitHub PRs | — | Code review |

### Key Papers to Read
- **"The Google File System" (2003)** — GFS, the distributed file system that started it all
- **"MapReduce" (2004)** — Simplified data processing on large clusters
- **"Bigtable" (2006)** — A distributed storage system for structured data
- **"The Chubby Lock Service" (2006)** — Loosely-coupled distributed lock service (inspired ZooKeeper)
- **"Dremel" (2010)** — Interactive analysis of web-scale datasets (became BigQuery)
- **"Dapper" (2010)** — Large-scale distributed systems tracing (inspired Zipkin/Jaeger)
- **"Megastore" (2011)** — Providing scalable, highly available storage
- **"Spanner" (2012)** — Google's globally-distributed database with TrueTime
- **"F1" (2013)** — A distributed SQL database built on Spanner
- **"Borg" (2015)** — Large-scale cluster management at Google (inspired Kubernetes)
- **"Maglev" (2016)** — A fast and reliable software network load balancer
- **"Zanzibar" (2019)** — Google's consistent, global authorization system
- **"BeyondCorp" (2014)** — A new approach to enterprise security

---

#cloud-providers #aws #gcp #google-internal #proprietary-systems
