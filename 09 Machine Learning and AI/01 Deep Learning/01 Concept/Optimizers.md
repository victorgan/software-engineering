# Optimizers

> <- Back to [[Neural Network Fundamentals]]

Algorithms that update model weights based on gradients to minimize the loss function. The choice of optimizer and learning rate schedule significantly affects training speed and final performance.

## Key Types

- **SGD** -- stochastic gradient descent, simple but effective with momentum
- **Adam** -- adaptive learning rates per parameter, default choice for many tasks
- **AdamW** -- Adam with decoupled weight decay, used in Transformers
- **Learning Rate Scheduling** -- cosine annealing, warmup, step decay, one-cycle

## Related

- [[Backpropagation]] (provides gradients to optimizer)
- [[Loss Functions]] (what optimizer minimizes)

---

#deep-learning #optimizers #training
