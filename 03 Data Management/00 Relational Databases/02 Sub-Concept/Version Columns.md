# Version Columns

> <- Back to [[Optimistic vs Pessimistic Locking]]

Optimistic locking strategy where a version number or timestamp column is checked at update time. If the version has changed since the read, the update is rejected and the application retries.

#relational-databases #transactions #optimistic-locking
