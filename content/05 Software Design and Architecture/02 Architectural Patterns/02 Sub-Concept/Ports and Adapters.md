# Ports and Adapters

> <- Back to [[Hexagonal Architecture]]

Ports are interfaces defined by the domain that describe how it interacts with the outside world. Adapters are implementations that connect the domain to specific technologies (database adapters, HTTP adapters, message queue adapters). The domain depends only on ports, never on adapters.

#property #hexagonal #ports-adapters
