# Borg to Kubernetes Mapping

> <- Back to [[Infrastructure Mapping]]

| | Google Internal | Open Source | GCP |
|---|---|---|---|
| System | Borg | Kubernetes | GKE |
| Concept | Container orchestration | Container orchestration | Managed Kubernetes |

Borg is Google's internal cluster manager that runs nearly all workloads. Kubernetes was directly inspired by Borg and designed by the same team. GKE provides managed Kubernetes on GCP. Key differences: Borg uses a monolithic scheduler while K8s is more modular; Borg supports Google-specific features like Borglet.

---

#google-internal #mapping #borg #kubernetes
