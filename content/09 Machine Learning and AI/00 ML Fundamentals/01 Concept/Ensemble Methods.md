# Ensemble Methods

> <- Back to [[Classical ML Algorithms]]

Combining multiple models to produce better predictions than any single model. The most consistently winning approach in tabular data competitions and production systems.

## Key Properties

- [[Bagging]]
- [[Boosting]]

## Types

- **Random Forest** -- bagging + feature randomization over decision trees
- **Gradient Boosting** -- sequential trees, each correcting prior errors
  - **XGBoost** -- optimized gradient boosting, regularization
  - **LightGBM** -- histogram-based, leaf-wise growth, fast
  - **CatBoost** -- native categorical feature handling

## Related

- [[Decision Trees]] (base learner)
- [[Bias-Variance Tradeoff]] (ensembles reduce variance)

---

#ml #ensemble-methods #random-forest #gradient-boosting
