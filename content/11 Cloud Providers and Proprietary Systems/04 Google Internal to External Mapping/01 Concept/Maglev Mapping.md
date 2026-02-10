# Maglev Mapping

> <- Back to [[Infrastructure Mapping]]

| | Google Internal | Open Source / Industry | GCP |
|---|---|---|---|
| System | Maglev | -- | Cloud Load Balancing |
| Concept | L4 software load balancer | -- | Global load balancing |

Maglev is Google's software-defined network load balancer (2016 paper). ECMP-based, handles packets at line rate. No direct open-source equivalent, though its consistent hashing algorithm (Maglev hashing) has been widely adopted. Powers GCP Cloud Load Balancing.

---

#google-internal #mapping #maglev #load-balancing
