# Spanner to CockroachDB Mapping

> <- Back to [[Data Systems Mapping]]

| | Google Internal | Open Source | GCP |
|---|---|---|---|
| System | Spanner | CockroachDB, YugabyteDB | Cloud Spanner |
| Concept | Distributed SQL | Distributed SQL | Managed distributed SQL |

Google's Spanner (2012 paper) introduced globally distributed, strongly consistent relational databases using TrueTime (atomic clocks + GPS). CockroachDB and YugabyteDB are open-source systems inspired by Spanner's design, using hybrid logical clocks instead of TrueTime. Cloud Spanner exposes the internal system on GCP.

---

#google-internal #mapping #spanner #cockroachdb
