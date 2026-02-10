# Anti-Corruption Layer

> <- Back to [[DDD in Practice]]

A translation layer at the boundary between bounded contexts that prevents one model from corrupting another. Translates between the models of two contexts, ensuring each context maintains its own clean domain model.

## Key Properties

- [[Model Translation]]
- [[Boundary Protection]]
- [[Adapter Implementation]]

## Related

- [[Context Mapping]] (ACL is a mapping pattern)
- [[Strangler Fig]] (ACL enables migration)

---

#ddd #anti-corruption-layer
