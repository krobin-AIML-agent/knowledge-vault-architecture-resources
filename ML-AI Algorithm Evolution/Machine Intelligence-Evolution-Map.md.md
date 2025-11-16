# Table of Contents

## 1. Machine Learning Models
- [1.1 Supervised Learning](#11-supervised-learning)
  - [Regression Algorithms](#regression-algorithms)
  - [Classification Algorithms](#classification-algorithms)
- [1.2 Unsupervised Learning](#12-unsupervised-learning)
  - [Clustering Algorithms](#clustering-algorithms)
  - [Dimensionality Reduction](#dimensionality-reduction)
- [1.3 Probabilistic Models](#13-probabilistic-models)
- [1.4 Energy Based Models](#14-energy-based-models)

## 2. Deep Learning Models
- [2.1 Core Neural Networks](#21-core-neural-networks)
- [2.2 Vision Architectures](#22-vision-architectures)
- [2.3 Sequence Models](#23-sequence-models)
- [2.4 Transformers](#24-transformers)
- [2.5 Deep Reinforcement Learning](#25-deep-reinforcement-learning)

## 3. Generative Models
- [3.1 Autoencoder Based](#31-autoencoder-based)
- [3.2 Adversarial Models](#32-adversarial-models)
- [3.3 Diffusion Models](#33-diffusion-models)
- [3.4 Autoregressive Generators](#34-autoregressive-generators)
- [3.5 Flow Models](#35-flow-models)

---

## 1. Machine Learning Models
### 1.1 Supervised Learning
## Regression Algorithms
**Linear Regression** (1805)

- Why it emerged: Quantify relationships between variables
- What it does: Fits a straight line minimizing squared error
- Analogy: Drawing the best possible line through scattered points

**Polynomial Regression (1805–1900s)**

- Why it emerged: Linear lines were too simple
- What it does: Models curved relationships
- Analogy: Using a bendable wire instead of a straight ruler

**Ridge Regression (1970)**

- Why it emerged: Linear regression fails with correlated variables
- What it does: Adds L2 penalty to stabilize coefficients
- Analogy: Tightening guitar strings to reduce vibrations

**Lasso Regression (1996)**

- Why it emerged: Need built-in feature selection
- What it does: Uses L1 penalty to eliminate irrelevant features
- Analogy: Packing only essentials in a small suitcase

**Elastic Net (2005)**

- Why it emerged: Ridge and Lasso each solve different problems
- What it does: Combines L1 and L2
- Analogy: Using a filter and stabilizer at the same time

## Classification Algorithms
**Logistic Regression (1958)**

- Why it emerged: Need probability for binary classes
- What it does: Sigmoid boundary
- Analogy: Dimmer switch between 0 and 1

**Support Vector Machine SVM (1963)**

- Why it emerged: Need large-margin classifier
- What it does: Maximizes class separation
- Analogy: Building the widest possible fence

**Kernel SVM (1990s)**

- Why it emerged: Data often not linearly separable
- What it does: Uses kernels for nonlinear boundaries
- Analogy: Lifting data into 3D so a flat slice separates it

**Naive Bayes (1960s)**

- Why it emerged: Fast probabilistic classification
- What it does: Uses independence assumptions
- Analogy: A doctor diagnosing symptoms independently

**K Nearest Neighbors KNN (1967)**

- Why it emerged: Example-based classification
- What it does: Votes from nearest neighbors
- Analogy: You resemble your closest friends

**Decision Tree (1984)**

- Why it emerged: Need interpretable rules
- What it does: Uses branching if-else logic
- Analogy: A decision flowchart

**Random Forest (2001)**

- Why it emerged: Trees overfit easily
- What it does: Trains many trees and averages
- Analogy: Asking many people instead of one

**Gradient Boosted Trees (1997–1999)**

- Why it emerged: Correct residual errors sequentially
- What it does: Boosts weak learners into strong ones
- Analogy: A tutor correcting mistakes step-by-step

**XGBoost (2016)**

- Why it emerged: Need fast, regularized boosting
- What it does: Highly optimized GBM
- Analogy: Formula-1 version of boosting

**LightGBM (2017)**

- Why it emerged: Boosting must scale to massive datasets
- What it does: Uses histogram buckets
- Analogy: Sorting items into bins instead of comparing all

**CatBoost (2017)**

- Why it emerged: Categorical features need native handling
- What it does: Ordered boosting and encoding
- Analogy: A model fluent in categorical languages

### 1.2 Unsupervised Learning
## Clustering Algorithms
**K Means Clustering (1957)**

- Why it emerged: Need simple clustering
- What it does: Groups data into K clusters
- Analogy: Organizing grocery aisles

**Gaussian Mixture Models GMM (1977)**

- Why it emerged: Clusters overlap and have soft boundaries
- What it does: Mixtures of Gaussian distributions
- Analogy: People belonging to multiple communities

**Hierarchical Clustering (1960s)**

- Why it emerged: Need multi-level clustering
- What it does: Builds hierarchical cluster trees
- Analogy: Family tree of groups

**DBSCAN (1996)**

- Why it emerged: Need density-aware clustering and noise detection
- What it does: Finds clusters based on density
- Analogy: Identifying conversation groups at a party

**Self Organizing Map SOM (1982)**

- Why it emerged: Neural visualization of topology
- What it does: Competitive learning grid
- Analogy: Compressing a world map into a small 2D sheet

## Dimensionality Reduction
**Principal Component Analysis PCA (1901)**

- Why it emerged: Reduce redundancy in high-dimensional data
- What it does: Projects onto principal directions
- Analogy: Compressing a song into MP3

**Linear Discriminant Analysis LDA (1936)**

- Why it emerged: PCA doesn’t use class labels
- What it does: Maximizes class separation
- Analogy: Organizing books into labeled categories

**t SNE (2008)**

- Why it emerged: Nonlinear visualization needed
- What it does: Preserves local neighborhoods
- Analogy: Drawing a city map showing neighborhoods

**UMAP (2018)**

- Why it emerged: Faster, better global structure than t SNE
- What it does: Learns manifolds
- Analogy: A more accurate world atlas

### 1.3 Probabilistic Models
## Bayesian Networks (1980s)

- Why it emerged: Model conditional dependencies
- What it does: Directed graphical models
- Analogy: Spider web of cause and effect

**Dynamic Bayesian Networks (1990s)**

- Why it emerged: Add time dependence
- What it does: Temporal Bayesian networks
- Analogy: Cause effect chains across movie frames

**Hidden Markov Models HMM (1960s)**

- Why it emerged: Need hidden sequential states
- What it does: Probabilistic transition model
- Analogy: Hidden weather states affecting daily conditions

### 1.4 Energy Based Models
**Hopfield Network (1982)**

- Why it emerged: Associative memory
- What it does: Stores patterns as energy minima
- Analogy: Retrieving a memory from a partial cue

**Restricted Boltzmann Machine RBM (1986)**

- Why it emerged: Learn hidden structure
- What it does: Bipartite energy model
- Analogy: A two way mirror discovering hidden features

**Deep Belief Network DBN (2006)**

- Why it emerged: Pretraining deep networks before ReLU era
- What it does: Stacked RBMs
- Analogy: Stacking windows for deeper insight

## 2. Deep Learning Models
### 2.1 Core Neural Networks
**Perceptron (1958)**

- Why: First artificial neuron
- Analogy: A single yes or no decision unit

**Multilayer Perceptron MLP (1986)**

- Why: Need non linear functions
- Analogy: Layers of decisions

**Feedforward Neural Network (1980s)**

- Why: Simple one direction computation
- Analogy: A conveyor belt of information

**Deep Neural Network DNN (2000s)**

- Why: Learn hierarchical features
- Analogy: Layered conveyor belts

### 2.2 Vision Architectures
**Convolutional Neural Network CNN (1998)**

- Why: Capture spatial structure
- Analogy: Sliding window detecting edges

LeNet (1998)
AlexNet (2012)
VGG (2014)
ResNet (2015)
EfficientNet (2019)

Each improves depth, width, efficiency, or performance.

**Vision Transformer ViT (2020)**

- Why: Apply attention to image patches
- Analogy: Reading an image like reading text

### 2.3 Sequence Models
**Recurrent Neural Network RNN (1986)**

- Why: Need memory across sequences
- Analogy: Remembering previous words in a sentence

**Long Short Term Memory LSTM (1997)**

- Why: Fix vanishing gradients
- Analogy: A notebook that remembers selectively

**Gated Recurrent Unit GRU (2014)**

- Why: Simplify LSTM
- Analogy: A compact memory unit

**Encoder Decoder Models (2014)**

Why: Translate sequences
Analogy: Read a sentence, then rewrite it

### 2.4 Transformers
**Transformer (2017)**

- Why: Remove sequential bottleneck
- Analogy: A team reading the entire text at once

BERT (2018)
GPT Series (2018–2024)
Claude (2023–2025)
T5 (2019)
LLaMA (2023)

Transformers dominate all modern deep learning.

### 2.5 Deep Reinforcement Learning
**Deep Q Network DQN (2013)**

- Analogy: A gamer improving through trial and error

**Actor Critic (1990s)**

- Analogy: Actor performs, critic scores

**PPO and A3C (2016–2017)**

- Analogy: Many actors learning in parallel

**RLHF (2022)**

- Analogy: Training models with human thumbs up or down

## 3. Generative Models
### 3.1 Autoencoder Based
**Autoencoder AE (1986)**

- Analogy: Zipping and unzipping data

**Denoising Autoencoder (2008)**

- Analogy: Cleaning a noisy image

**Variational Autoencoder VAE (2013)**

- Analogy: Sampling new ideas from imagination

### 3.2 Adversarial Models
**Generative Adversarial Network GAN (2014)**

- Analogy: Counterfeiter versus detective

StyleGAN (2018)
BigGAN (2018)
CycleGAN (2017)

### 3.3 Diffusion Models
- Denoising Diffusion Probabilistic Model DDPM (2015 theory, 2020 practical)

- Latent Diffusion Model LDM (2022)

- Stable Diffusion, Imagen, DALL E 2 (2021–2022)

- Analogy: Destroy an image with noise then learn to reverse it

### 3.4 Autoregressive Generators
**PixelRNN (2016)**
**PixelCNN (2016)**

- Analogy: Painting pixel by pixel

**GPT, Claude, Gemini (2018–present)**

- Analogy: Predicting the next word forever

### 3.5 Flow Models
**Normalizing Flows (2014)**
**RealNVP (2017)**
**Glow (2018)**

- Analogy: A perfect reversible blender
