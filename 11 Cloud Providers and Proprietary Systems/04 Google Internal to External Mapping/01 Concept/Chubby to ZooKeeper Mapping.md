# Chubby to ZooKeeper Mapping

> <- Back to [[Data Systems Mapping]]

| | Google Internal | Open Source | GCP |
|---|---|---|---|
| System | Chubby | ZooKeeper, etcd | -- |
| Concept | Distributed lock service | Distributed coordination | -- |

Chubby (2006 paper) is Google's distributed lock service providing coarse-grained locking and reliable storage for small data. ZooKeeper was directly inspired by Chubby and became the standard for distributed coordination in the Hadoop ecosystem. etcd serves a similar role in Kubernetes. No direct GCP equivalent.

---

#google-internal #mapping #chubby #zookeeper
