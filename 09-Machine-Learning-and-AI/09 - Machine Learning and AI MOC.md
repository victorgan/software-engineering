# 09 — Machine Learning & AI MOC

> ← Back to [[Software Engineering - Map of Content]]

Teaching machines to learn from data. Increasingly core to software engineering — not just for ML specialists, but for every engineer building modern products.

---

## [[ML Fundamentals]]

### Learning Types
- **Supervised Learning** — Labeled data, learn input → output mapping
  - **Classification** — Discrete outputs (spam/not spam, image labels)
  - **Regression** — Continuous outputs (price prediction, temperature)
- **Unsupervised Learning** — No labels, discover structure in data
  - **Clustering** — K-Means, DBSCAN, hierarchical, Gaussian mixture models
  - **Dimensionality Reduction** — PCA, t-SNE, UMAP, autoencoders
  - **Anomaly Detection** — Isolation Forest, one-class SVM
- **Semi-Supervised Learning** — Small labeled + large unlabeled dataset
- **Self-Supervised Learning** — Generate labels from data itself (masked language modeling, contrastive learning)
- **Reinforcement Learning** — Agent, environment, reward signal, policy optimization
  - **Key Concepts** — States, actions, rewards, Q-learning, policy gradient
  - **RLHF** — Reinforcement Learning from Human Feedback (used to train LLMs)

### Classical ML Algorithms
- **Linear Models** — Linear regression, logistic regression, regularization (L1/Lasso, L2/Ridge)
- **Decision Trees** — Splits, information gain, Gini impurity, pruning
- **Ensemble Methods** — Random Forest, Gradient Boosting (XGBoost, LightGBM, CatBoost)
- **Support Vector Machines** — Kernel trick, margin maximization
- **K-Nearest Neighbors** — Instance-based, distance metrics
- **Naive Bayes** — Probabilistic, strong independence assumption, good for text
- **Bayesian Methods** — Prior/posterior, Gaussian processes, probabilistic programming

### Model Evaluation
- **Train/Validation/Test Split** — Holdout method, cross-validation (k-fold, stratified)
- **Classification Metrics** — Accuracy, Precision, Recall, F1-Score, AUC-ROC, confusion matrix
- **Regression Metrics** — MSE, RMSE, MAE, R², adjusted R²
- **Bias-Variance Tradeoff** — Underfitting (high bias) vs overfitting (high variance)
- **Regularization** — L1, L2, dropout, early stopping, data augmentation
- **Hyperparameter Tuning** — Grid search, random search, Bayesian optimization (Optuna)
- **Feature Importance** — SHAP values, permutation importance, feature selection

### Feature Engineering
- **Numerical Features** — Scaling (standardization, normalization), binning, log transforms
- **Categorical Features** — One-hot encoding, label encoding, target encoding, embeddings
- **Text Features** — TF-IDF, bag of words, n-grams, word embeddings
- **Time Features** — Lag features, rolling statistics, cyclical encoding
- **Feature Selection** — Correlation analysis, mutual information, recursive feature elimination
- **Feature Stores** — Centralized feature repository (Feast, Tecton, Hopsworks)

---

## [[Deep Learning]]

### Neural Network Fundamentals
- **Perceptron** — Weighted sum + activation, basic building block
- **Activation Functions** — ReLU, Sigmoid, Tanh, GELU, Swish, Softmax
- **Backpropagation** — Chain rule, gradient computation, weight updates
- **Loss Functions** — Cross-entropy, MSE, hinge loss, contrastive loss
- **Optimizers** — SGD, Adam, AdamW, learning rate scheduling (cosine, warmup)
- **Batch Normalization** — Normalize activations, stabilize training
- **Layer Normalization** — Normalize across features (used in Transformers)
- **Dropout** — Regularization by randomly dropping neurons during training
- **Residual Connections** — Skip connections, enable very deep networks (ResNet)

### Convolutional Neural Networks (CNNs)
- **Convolution Layers** — Filters/kernels, feature maps, stride, padding
- **Pooling** — Max pooling, average pooling, global average pooling
- **Architectures** — LeNet, AlexNet, VGG, ResNet, EfficientNet, ConvNeXt
- **Applications** — Image classification, object detection (YOLO, Faster R-CNN), segmentation

### Recurrent Neural Networks (RNNs)
- **Vanilla RNN** — Sequential processing, vanishing gradient problem
- **LSTM (Long Short-Term Memory)** — Gates (forget, input, output), cell state
- **GRU (Gated Recurrent Unit)** — Simplified LSTM
- **Bidirectional RNNs** — Process sequence in both directions
- **Applications** — Time series, speech (largely superseded by Transformers)

### Transformers
- **Self-Attention** — Query, Key, Value matrices, attention scores
- **Multi-Head Attention** — Parallel attention with different projections
- **Positional Encoding** — Inject sequence order information
- **Encoder-Decoder Architecture** — Original Transformer (Vaswani et al., 2017)
- **Encoder-Only** — BERT, RoBERTa — bidirectional, good for classification/NER
- **Decoder-Only** — GPT, LLaMA, Claude — autoregressive, text generation
- **Encoder-Decoder** — T5, BART — sequence-to-sequence tasks
- **Scaling Laws** — Model size, data size, compute — predictable performance scaling
- **Flash Attention** — IO-aware attention, reduced memory, faster training
- **Mixture of Experts (MoE)** — Sparse activation, conditional computation

### Generative Models
- **GANs (Generative Adversarial Networks)** — Generator vs discriminator, adversarial training
- **VAEs (Variational Autoencoders)** — Latent space, reconstruction + KL divergence loss
- **Diffusion Models** — Gradually denoise, state-of-the-art image generation (Stable Diffusion, DALL-E)
- **Autoregressive Models** — Generate token by token (GPT, LLMs)
- **Flow Models** — Invertible transformations, exact likelihood

### Training at Scale
- **Data Parallelism** — Replicate model, split data across GPUs
- **Model Parallelism** — Split model across GPUs (tensor, pipeline parallelism)
- **Mixed Precision Training** — FP16/BF16 + FP32, faster with minimal accuracy loss
- **Gradient Accumulation** — Simulate larger batch sizes
- **Distributed Training** — DeepSpeed, FSDP, Megatron-LM
- **Frameworks** — PyTorch, JAX, TensorFlow, Keras

---

## [[Natural Language Processing]]

### Text Processing Pipeline
- **Tokenization** — Word-level, subword (BPE, WordPiece, SentencePiece, Unigram)
- **Vocabulary** — Token-to-ID mapping, special tokens ([CLS], [SEP], [PAD])
- **Embeddings** — Word2Vec, GloVe, FastText, contextual embeddings (BERT, GPT)

### Language Model Applications
- **Text Classification** — Sentiment analysis, topic categorization, intent detection
- **Named Entity Recognition (NER)** — Extract entities (people, places, organizations)
- **Question Answering** — Extractive (span selection), generative (free-form answer)
- **Summarization** — Extractive vs abstractive summarization
- **Machine Translation** — Sequence-to-sequence, multilingual models
- **Text Generation** — Creative writing, code generation, dialogue systems

### Large Language Models (LLMs)
- **Foundation Models** — GPT-4, Claude, LLaMA, Gemini, Mistral
- **Prompt Engineering** — Zero-shot, few-shot, chain-of-thought, system prompts
- **In-Context Learning** — Learning from examples in the prompt
- **Retrieval-Augmented Generation (RAG)** — Retrieve relevant documents, inject into context
  - **Vector Databases** — Pinecone, Weaviate, Chroma, Milvus, pgvector
  - **Embedding Models** — Sentence transformers, OpenAI embeddings
  - **Chunking Strategies** — Fixed-size, semantic, recursive splitting
  - **Retrieval Methods** — Dense retrieval, sparse (BM25), hybrid
- **Fine-Tuning** — Full fine-tuning, LoRA, QLoRA, adapter methods
- **RLHF / Constitutional AI** — Alignment techniques, reward models
- **Agent Frameworks** — LangChain, LlamaIndex, AutoGPT, function calling, tool use
- **Evaluation** — Perplexity, BLEU, ROUGE, human evaluation, benchmarks (MMLU, HumanEval)
- **Inference Optimization** — Quantization (INT8, INT4), KV-cache, speculative decoding, vLLM

---

## [[MLOps]]

### Model Lifecycle
- **Experiment Tracking** — MLflow, Weights & Biases, Neptune, CometML
- **Model Registry** — Version models, stage transitions (dev → staging → production)
- **Reproducibility** — Seed fixing, environment pinning, data versioning (DVC)

### Model Serving
- **Batch Inference** — Offline predictions on batches of data
- **Real-Time Inference** — Online prediction APIs, low latency requirements
- **Serving Frameworks** — TorchServe, TensorFlow Serving, Triton Inference Server, BentoML
- **Model Optimization** — ONNX runtime, TensorRT, quantization, pruning, distillation
- **Edge Deployment** — TensorFlow Lite, Core ML, ONNX Mobile

### Data Management for ML
- **Data Versioning** — DVC, LakeFS, Delta Lake
- **Data Labeling** — Label Studio, Scale AI, Amazon SageMaker Ground Truth
- **Data Validation** — Schema validation, distribution drift detection, Great Expectations
- **Synthetic Data** — Generated training data, privacy preservation

### Model Monitoring
- **Data Drift** — Input distribution changes over time
- **Concept Drift** — Relationship between input and output changes
- **Model Performance Degradation** — Accuracy decay, latency increase
- **Monitoring Tools** — Evidently AI, Arize, WhyLabs, NannyML
- **Retraining Triggers** — Scheduled, performance-based, drift-based

### ML Infrastructure
- **GPU Management** — CUDA, GPU scheduling, multi-GPU training
- **ML Platforms** — SageMaker, Vertex AI, Azure ML, Databricks
- **Pipeline Orchestration** — Kubeflow, Airflow, Prefect, Metaflow
- **Cost Management** — Spot instances, auto-scaling, right-sizing GPU instances

---

#ml #ai #deep-learning #nlp #llm #mlops
