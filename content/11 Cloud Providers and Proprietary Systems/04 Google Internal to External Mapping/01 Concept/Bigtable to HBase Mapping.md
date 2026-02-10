# Bigtable to HBase Mapping

> <- Back to [[Data Systems Mapping]]

| | Google Internal | Open Source | GCP |
|---|---|---|---|
| System | Bigtable | HBase, Cassandra | Cloud Bigtable |
| Concept | Wide-column NoSQL | Wide-column NoSQL | Managed wide-column NoSQL |

Google's Bigtable (2006 paper) was the original wide-column store. HBase was directly inspired by the paper and built on top of HDFS/Hadoop. Cassandra borrowed Bigtable's data model combined with Dynamo's distribution model. Cloud Bigtable exposes the internal system as a managed GCP service.

---

#google-internal #mapping #bigtable #hbase
