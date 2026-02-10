# Compensating Actions

> <- Back to [[Saga Pattern]]

Undo operations that reverse the effects of a previously completed step. For example, if order fulfillment fails: refund payment (compensate for charge), release reserved inventory (compensate for reservation). Compensating actions must be idempotent and may not perfectly undo the original action.

#distributed-systems #patterns #transactions
