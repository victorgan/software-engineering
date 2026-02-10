# N+1 Query Problem (API Design)

> <- Back to [[GraphQL Challenges]]

When resolving a list of N items, each item triggers an additional database query for related data, resulting in N+1 total queries. Solved by DataLoader which batches and deduplicates requests within a single execution tick.

#property #graphql #n-plus-one
