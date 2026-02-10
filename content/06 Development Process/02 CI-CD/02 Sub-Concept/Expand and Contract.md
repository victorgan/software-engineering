# Expand and Contract

> <- Back to [[Backward-Compatible Migrations]]

A two-phase migration pattern: (1) Expand: add the new schema alongside the old, deploy code that handles both. (2) Contract: once all code uses the new schema, remove the old columns/tables. Ensures zero downtime during schema changes.

#property #cicd #migrations #expand-contract
