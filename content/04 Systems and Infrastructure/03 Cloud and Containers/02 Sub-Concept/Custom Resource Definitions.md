# Custom Resource Definitions

> <- Back to [[Operators]]

CRDs extend the Kubernetes API with new resource types (e.g., PostgresCluster, PrometheusRule). Users create instances of custom resources using standard kubectl commands. CRDs define the schema (OpenAPI validation) and can be versioned. The operator's controller watches for changes to these custom resources.

#cloud #containers #kubernetes
