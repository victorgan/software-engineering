# Repeatable Read

> <- Back to [[Isolation Levels]]

Transactions see a consistent snapshot from the start of the transaction. Prevents dirty reads and non-repeatable reads but may allow phantom reads in some implementations. Default in MySQL InnoDB.

#relational-databases #transactions #isolation
