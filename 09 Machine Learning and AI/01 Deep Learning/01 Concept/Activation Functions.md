# Activation Functions

> <- Back to [[Neural Network Fundamentals]]

Nonlinear functions applied to neuron outputs. Without them, stacking layers would only compute linear transformations. The choice of activation affects training dynamics and model capacity.

## Key Types

- **ReLU** -- max(0, x), most common, simple but can "die" (zero gradients)
- **Sigmoid** -- maps to (0, 1), used in binary output layers
- **Tanh** -- maps to (-1, 1), zero-centered
- **GELU** -- smooth ReLU variant, used in Transformers
- **Swish** -- x * sigmoid(x), self-gated
- **Softmax** -- converts logits to probability distribution (multi-class output)

## Related

- [[Perceptron]] (activation applied to weighted sum)
- [[Backpropagation]] (gradients flow through activations)

---

#deep-learning #activation-functions
