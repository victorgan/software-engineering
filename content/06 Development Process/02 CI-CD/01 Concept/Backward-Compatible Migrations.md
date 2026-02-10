# Backward-Compatible Migrations

> <- Back to [[Database Migrations in Deployment]]

Expand-and-contract pattern: first expand the schema (add new columns/tables), deploy code that works with both schemas, then contract (remove old columns). Avoids breaking running code during deployment.

## Key Properties

- [[Expand and Contract]]
- [[Dual Schema Support]]
- [[Safe Migration Pattern]]

---

#cicd #migrations #backward-compatible
