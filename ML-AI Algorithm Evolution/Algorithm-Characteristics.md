# Algorithm Characteristics

**This table gives you an easy way to understand how the major AI and machine-learning algorithms actually work. It shows what each algorithm is good at, what its weaknesses are, why it was created, and how it connects to the models that came before and after it. Think of it as a fast cheat sheet that helps you pick the right algorithm, understand the logic behind it, and see how today’s modern AI systems evolved from simpler methods.**

| Algorithm | How It Learns | Fits Best With | Limitations | Why It Exists | Predecessor | Downstream Dependent |
|-----------|----------------|----------------|-------------|----------------|-------------|------------------------|
| Linear Regression | Minimizes squared error (OLS) | Continuous numeric data | Sensitive to outliers, assumes linearity | Quantify variable relationships | — | Ridge, Lasso, Logistic Regression |
| Ridge Regression | L2 penalty on weights | Multicollinear numeric data | Requires tuning lambda | Stabilize coefficients, reduce overfitting | Linear Regression | Elastic Net |
| Lasso Regression | L1 penalty on weights | Sparse data, feature selection | Can drop relevant features | Embedded feature selection | Ridge | Elastic Net |
| Elastic Net | Combination of L1 + L2 | High-dimensional sparse data | Complex tuning | Balance bias-variance + sparsity | Ridge + Lasso | Linear SVM, Logistic Regression |
| Logistic Regression | Sigmoid-based probability estimation | Binary classification | Linear boundary assumption | Foundation classifier | Linear Regression | Softmax, SVM |
| Decision Tree | Recursive impurity reduction | Mixed data types | Overfits without pruning | Human-readable rules | ID3 / CART | Random Forest, Gradient Boosting |
| Random Forest | Bagged ensemble of trees | Tabular nonlinear data | Low interpretability, slower inference | Reduce tree variance | Decision Tree | Gradient Boosted Trees |
| Gradient Boosted Trees | Sequential boosting of weak learners | Structured/tabular data | Complex tuning, overfits | Maximize accuracy | Random Forest | XGBoost, LightGBM |
| KNN | Distance-based voting | Small numeric datasets | Slow on large sets | Simple instance-based learning | — | SVM, CNN (conceptually) |
| SVM | Maximize margin | Structured small datasets | Expensive on large datasets | High-dimensional separability | Logistic Regression | Kernel SVM |
| Naive Bayes | Simple conditional probability | Text, categorical data | Independence assumption | Fast baseline classifier | — | Bayesian Networks |
| K-Means | Iterative centroid optimization | Numeric, well-separated data | Sensitive to K, initialization | Simple clustering | — | GMM, DBSCAN |
| GMM | EM with Gaussian mixtures | Continuous probabilistic data | Local minima risk | Soft clustering | K-Means | HMM |
| Hierarchical Clustering | Agglomerative/divisive merging | Small datasets | Scaling limitations | Multi-level clustering | — | Dendrogram analysis |
| PCA | Eigen-decomposition | High-dimensional numeric data | Linear only | Dimensionality reduction | Linear algebra | Autoencoders |
| LDA | Projects to maximize class separation | Labeled numeric/categorical | Gaussian assumption | Supervised compression | PCA | Neural embeddings |
| Perceptron | Weight updates from classification errors | Linearly separable data | Fails on non-linear data | First neuron model | Logistic Regression | MLP |
| MLP | Backpropagation | Structured, semi-structured data | Overfitting, black-box | Universal function approximation | Perceptron | CNN, RNN |
| CNN | Convolutions for spatial features | Images, spatial data | Needs large datasets | Spatial hierarchy modeling | MLP | Vision Transformers |
| RNN | Sequential recurrence | Time series, text | Vanishing gradients | Temporal dependency modeling | MLP | LSTM, GRU, Transformers |
| Autoencoder | Reconstruction loss minimization | High-dimensional unlabeled data | Can learn identity function | Latent representation learning | PCA | VAE, GAN |
| Transformer | Self-attention | Text, sequences, multimodal | Compute heavy | Parallel sequence processing | RNN | LLMs, Diffusion Models |
| GAN | Generator vs discriminator adversarial training | Image synthesis | Unstable training | Generative creativity | Autoencoder | Diffusion, StyleGAN |
| Reinforcement Learning | Policy learning from reward | Decision/control tasks | Sample inefficient | Learn from environment | Supervised Learning | RLHF, Agents |
| Evolutionary Algorithms | Genetic mutation and selection | Search + optimization | Slow convergence | Explore large solution spaces | Optimization theory | Neuroevolution |
| Bayesian Networks | Directed probabilistic dependencies | Uncertain structured data | Expensive inference | Causal modeling | Naive Bayes | Dynamic Bayesian Networks |
| Hopfield Network | Energy minimization | Associative memory | Very low capacity | Memory retrieval | Perceptron | RBM |
| Self-Organizing Map | Competitive learning | Unlabeled high-dimensional data | Limited scaling | Topology mapping | K-Means | Representation learning |
| RBM | Bipartite energy model | Binary / numeric unsupervised | Hard to train | Discover hidden structure | Hopfield | DBN |
| Deep Belief Network | Stacked RBMs | Unlabeled hierarchical data | Complex training | Deep feature learning | RBM | Deep Autoencoders |
