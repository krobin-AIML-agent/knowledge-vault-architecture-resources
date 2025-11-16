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

**(No formal Read: Gauss/Legendre original method predates modern publishing)**

- Why it emerged: Quantify relationships between variables
- What it does: Fits a straight line minimizing squared error
- Analogy: Drawing the best possible line through scattered points

**Polynomial Regression (1805–1900s)**

**(No single foundational Read: extension of classical regression)**

- Why it emerged: Linear lines were too simple
- What it does: Models curved relationships
- Analogy: Using a bendable wire instead of a straight ruler

**Ridge Regression (1970)**

**Read: Hoerl & Kennard: “Ridge Regression: Biased Estimation for Nonorthogonal Problems”
https://doi.org/10.1080/00401706.1970.10488634**

- Why it emerged: Linear regression fails with correlated variables
- What it does: Adds L2 penalty to stabilize coefficients
- Analogy: Tightening guitar strings to reduce vibrations

**Lasso Regression (1996)**

**Read: Tibshirani: “Regression Shrinkage and Selection via the Lasso”
https://doi.org/10.1111/j.2517-6161.1996.tb02080.x**

- Why it emerged: Need built-in feature selection
- What it does: Uses L1 penalty to eliminate irrelevant features
- Analogy: Packing only essentials in a small suitcase

**Elastic Net (2005)**

**Read: Zou & Hastie: “Regularization and Variable Selection via the Elastic Net”
https://doi.org/10.1111/j.1467-9868.2005.00503.x**

- Why it emerged: Ridge and Lasso each solve different problems
- What it does: Combines L1 and L2
- Analogy: Using a filter and stabilizer at the same time

## Classification Algorithms
**Logistic Regression (1958)**

**Read: Cox: “The Regression Analysis of Binary Sequences”
https://doi.org/10.2307/2333501**

- Why it emerged: Need probability for binary classes
- What it does: Sigmoid boundary
- Analogy: Dimmer switch between 0 and 1

**Support Vector Machine SVM (1963)**

**Read: Cortes & Vapnik: “Support-Vector Networks”
https://doi.org/10.1007/BF00994018**

- Why it emerged: Need large-margin classifier
- What it does: Maximizes class separation
- Analogy: Building the widest possible fence

**Kernel SVM (1990s)**

**Read: Vapnik: Statistical Learning Theory (1998)
https://www.wiley.com/en-us/Statistical+Learning+Theory-p-9780471030034**

- Why it emerged: Data often not linearly separable
- What it does: Uses kernels for nonlinear boundaries
- Analogy: Lifting data into 3D so a flat slice separates it

**Naive Bayes (1960s)**

**Read: Maron: “Automatic Indexing: An Experimental Inquiry”
https://doi.org/10.1145/321062.321071**

- Why it emerged: Fast probabilistic classification
- What it does: Uses independence assumptions
- Analogy: A doctor diagnosing symptoms independently

**K Nearest Neighbors KNN (1967)**

**Read: Cover & Hart: “Nearest Neighbor Pattern Classification”
https://ieeexplore.ieee.org/document/1053964**

- Why it emerged: Example-based classification
- What it does: Votes from nearest neighbors
- Analogy: You resemble your closest friends

**Decision Tree (1984)**

**Read: Breiman et al.: Classification and Regression Trees
https://www.amazon.com/dp/0412048418**

- Why it emerged: Need interpretable rules
- What it does: Uses branching if-else logic
- Analogy: A decision flowchart

**Random Forest (2001)**

**Read: Breiman: “Random Forests”
https://doi.org/10.1023/A:1010933404324**

- Why it emerged: Trees overfit easily
- What it does: Trains many trees and averages
- Analogy: Asking many people instead of one

**Gradient Boosted Trees (1997–1999)**

**Read: Friedman: “Greedy Function Approximation: A Gradient Boosting Machine”
https://doi.org/10.1214/aos/1013203451**

- Why it emerged: Correct residual errors sequentially
- What it does: Boosts weak learners into strong ones
- Analogy: A tutor correcting mistakes step-by-step

**XGBoost (2016)**

**Read: Chen & Guestrin: “XGBoost: A Scalable Tree Boosting System”
https://doi.org/10.1145/2939672.2939785**

- Why it emerged: Need fast, regularized boosting
- What it does: Highly optimized GBM
- Analogy: Formula-1 version of boosting

**LightGBM (2017)**

**Read: Ke et al.: “LightGBM: A Highly Efficient Gradient Boosting Decision Tree”
https://Reads.nips.cc/Read/6907-lightgbm-a-highly-efficient-gradient-boosting-decision-tree**

- Why it emerged: Boosting must scale to massive datasets
- What it does: Uses histogram buckets
- Analogy: Sorting items into bins instead of comparing all

**CatBoost (2017)**

**Read: Dorogush et al.: “CatBoost: Unbiased Boosting with Categorical Features”
https://arxiv.org/abs/1810.11363**

- Why it emerged: Categorical features need native handling
- What it does: Ordered boosting and encoding
- Analogy: A model fluent in categorical languages

### 1.2 Unsupervised Learning
## Clustering Algorithms
**K Means Clustering (1957)**

**Read: MacQueen: Some Methods for Classification and Analysis of Multivariate Observations
https://projecteuclid.org/euclid.bsmsp/1200512992**

- Why it emerged: Need simple clustering
- What it does: Groups data into K clusters
- Analogy: Organizing grocery aisles

**Gaussian Mixture Models GMM (1977)**

**Read: Dempster, Laird & Rubin: EM Algorithm
https://doi.org/10.1111/j.2517-6161.1977.tb01600.x**

- Why it emerged: Clusters overlap and have soft boundaries
- What it does: Mixtures of Gaussian distributions
- Analogy: People belonging to multiple communities

**Hierarchical Clustering (1960s)**

**Read: Johnson: Hierarchical Clustering Schemes
https://doi.org/10.1080/01621459.1967.10502022**

- Why it emerged: Need multi-level clustering
- What it does: Builds hierarchical cluster trees
- Analogy: Family tree of groups

**DBSCAN (1996)**

**Read: Ester et al.: Density-Based Spatial Clustering of Applications with Noise
https://www.aaai.org/Reads/KDD/1996/KDD96-037.pdf**

- Why it emerged: Need density-aware clustering and noise detection
- What it does: Finds clusters based on density
- Analogy: Identifying conversation groups at a party

**Self Organizing Map SOM (1982)**

**Read: Kohonen: Self-Organized Formation of Topologically Correct Feature Maps
https://doi.org/10.1007/BF00337288**

- Why it emerged: Neural visualization of topology
- What it does: Competitive learning grid
- Analogy: Compressing a world map into a small 2D sheet

## Dimensionality Reduction
**Principal Component Analysis PCA (1901)**

**Read: Pearson: On Lines and Planes of Closest Fit
https://doi.org/10.1080/14786440109462720**

- Why it emerged: Reduce redundancy in high-dimensional data
- What it does: Projects onto principal directions
- Analogy: Compressing a song into MP3

**Linear Discriminant Analysis LDA (1936)**

**Read: Fisher: The Use of Multiple Measurements in Taxonomic Problems
https://doi.org/10.1111/j.1469-1809.1936.tb02137.x**

- Why it emerged: PCA doesn’t use class labels
- What it does: Maximizes class separation
- Analogy: Organizing books into labeled categories

**t SNE (2008)**

**Read: van der Maaten & Hinton: Visualizing Data using t-SNE
https://www.jmlr.org/Reads/volume9/vandermaaten08a/vandermaaten08a.pdf**

- Why it emerged: Nonlinear visualization needed
- What it does: Preserves local neighborhoods
- Analogy: Drawing a city map showing neighborhoods

**UMAP (2018)**

**Read: McInnes, Healy, Melville: UMAP: Uniform Manifold Approximation and Projection
https://arxiv.org/abs/1802.03426**

- Why it emerged: Faster, better global structure than t SNE
- What it does: Learns manifolds
- Analogy: A more accurate world atlas

### 1.3 Probabilistic Models
## Bayesian Networks (1980s)

**Read: Judea Pearl: Bayesian Networks: A Model of Self-Activated Memory
https://doi.org/10.1016/B978-0-08-051998-3.50010-4**

- Why it emerged: Model conditional dependencies
- What it does: Directed graphical models
- Analogy: Spider web of cause and effect

**Dynamic Bayesian Networks (1990s)**

**Read: Dean & Kanazawa: A Model for Reasoning about Persistence and Causation
https://doi.org/10.1016/0004-3702(89)90086-2**

- Why it emerged: Add time dependence
- What it does: Temporal Bayesian networks
- Analogy: Cause effect chains across movie frames

**Hidden Markov Models HMM (1960s)**

**Read: Rabiner: A Tutorial on Hidden Markov Models and Selected Applications
https://ieeexplore.ieee.org/document/18626**

- Why it emerged: Need hidden sequential states
- What it does: Probabilistic transition model
- Analogy: Hidden weather states affecting daily conditions

### 1.4 Energy Based Models
**Hopfield Network (1982)**

**Read: Hopfield: Neural Networks and Physical Systems with Emergent Collective Computational Abilities
https://doi.org/10.1073/pnas.79.8.2554**

- Why it emerged: Associative memory
- What it does: Stores patterns as energy minima
- Analogy: Retrieving a memory from a partial cue

**Restricted Boltzmann Machine RBM (1986)**

**Read: Smolensky: Information Processing in Dynamical Systems
https://psycnet.apa.org/record/2002-04103-011**

- Why it emerged: Learn hidden structure
- What it does: Bipartite energy model
- Analogy: A two way mirror discovering hidden features

**Deep Belief Network DBN (2006)**

**Read: Hinton, Osindero, Teh: A Fast Learning Algorithm for Deep Belief Nets
https://doi.org/10.1162/neco.2006.18.7.1527**

- Why it emerged: Pretraining deep networks before ReLU era
- What it does: Stacked RBMs
- Analogy: Stacking windows for deeper insight

## 2. Deep Learning Models
### 2.1 Core Neural Networks
**Perceptron (1958)**

**Read: Rosenblatt: The Perceptron: A Probabilistic Model for Information Storage and Organization in the Brain
https://psycnet.apa.org/record/1959-09865-001**

- Why: First artificial neuron
- Analogy: A single yes or no decision unit

**Multilayer Perceptron MLP (1986)**

**Read: Rumelhart, Hinton & Williams: Learning Representations by Back-Propagating Errors
https://www.nature.com/articles/323533a0**

- Why: Need non linear functions
- Analogy: Layers of decisions

**Feedforward Neural Network (1980s)**

**Read: Same foundational work as Backpropagation (Rumelhart et al., 1986)**
https://www.nature.com/articles/323533a0**

- Why: Simple one direction computation
- Analogy: A conveyor belt of information

**Deep Neural Network DNN (2000s)**

**(No single Read: evolution of deeper feedforward models + GPUs; references rooted in backpropagation and CNN scaling)**

- Why: Learn hierarchical features
- Analogy: Layered conveyor belts

### 2.2 Vision Architectures
**Convolutional Neural Network CNN (1998)**

**Read: LeCun et al.: Gradient-Based Learning Applied to Document Recognition
http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf**

- Why: Capture spatial structure
- Analogy: Sliding window detecting edges

**LeNet (1998)**

**Read: LeCun et al.: First CNN for handwritten digit recognition
http://yann.lecun.com/exdb/publis/pdf/lecun-98.pdf**

**AlexNet (2012)**

**Read: Krizhevsky, Sutskever, Hinton: ImageNet Classification with Deep Convolutional Neural Networks
https://Reads.nips.cc/Read/4824-imagenet-classification-with-deep-convolutional-neural-network**

**VGG (2014)**

**Read: Simonyan & Zisserman: Very Deep Convolutional Networks for Large-Scale Image Recognition
https://arxiv.org/abs/1409.1556**

**ResNet (2015)**

**Read: He et al.: Deep Residual Learning for Image Recognition
https://arxiv.org/abs/1512.03385**

**EfficientNet (2019)**

**Read: Tan & Le: EfficientNet: Rethinking Model Scaling for CNNs
https://arxiv.org/abs/1905.11946**

Each improves depth, width, efficiency, or performance.

**Vision Transformer ViT (2020)**

**Read: Dosovitskiy et al.: An Image is Worth 16×16 Words
https://arxiv.org/abs/2010.11929**

- Why: Apply attention to image patches
- Analogy: Reading an image like reading text

### 2.3 Sequence Models
**Recurrent Neural Network RNN (1986)**

**Read: Rumelhart, Hinton, Williams: foundational recurrent backpropagation
https://www.nature.com/articles/323533a0**

- Why: Need memory across sequences
- Analogy: Remembering previous words in a sentence

**Long Short Term Memory LSTM (1997)**

**Read: Hochreiter & Schmidhuber
https://www.bioinf.jku.at/publications/older/2604.pdf**

- Why: Fix vanishing gradients
- Analogy: A notebook that remembers selectively

**Gated Recurrent Unit GRU (2014)**

**Read: Cho et al.: Learning Phrase Representations using RNN Encoder–Decoder for Statistical Machine Translation
https://arxiv.org/abs/1406.1078**

- Why: Simplify LSTM
- Analogy: A compact memory unit

**Encoder Decoder Models (2014)**

**Read: Sutskever et al.: Sequence to Sequence Learning with Neural Networks
https://arxiv.org/abs/1409.3215**

Why: Translate sequences
Analogy: Read a sentence, then rewrite it

### 2.4 Transformers
**Transformer (2017)**

**Read: Vaswani et al.: Attention is All You Need
https://arxiv.org/abs/1706.03762**

- Why: Remove sequential bottleneck
- Analogy: A team reading the entire text at once

**BERT (2018)**

**Read: Devlin et al.: BERT: Pre-training of Deep Bidirectional Transformers
https://arxiv.org/abs/1810.04805**

**GPT Series (2018–2024)**
- GPT-1 (2018): Improving Language Understanding by Generative Pre-Training
https://openai.com/research/language-unsupervised
- GPT-2 (2019): Better Language Models and Their Implications
https://openai.com/research/better-language-models
- GPT-3 (2020): Language Models are Few-Shot Learners
https://arxiv.org/abs/2005.14165
- GPT-4 (2023)
https://openai.com/research/gpt-4
- GPT-4o (2024)
https://openai.com/o4

**Claude (2023–2025)**

**Reads: Anthropic Research
https://www.anthropic.com/index/#research**

**T5 (2019)**

**Read: Raffel et al.: Exploring the Limits of Transfer Learning with a Unified Text-to-Text Transformer
https://arxiv.org/abs/1910.10683**

**LLaMA (2023)**

**Read: Touvron et al.: LLaMA: Open and Efficient Foundation Language Models
https://ai.facebook.com/research/publications/llama-open-and-efficient-foundation-language-models/**

Transformers dominate all modern deep learning.

### 2.5 Deep Reinforcement Learning
**Deep Q Network DQN (2013)**

**Read: Mnih et al.: Playing Atari with Deep Reinforcement Learning
https://arxiv.org/abs/1312.5602** 

- Analogy: A gamer improving through trial and error

**Actor Critic (1990s)**

**Read: Konda & Tsitsiklis: Actor–Critic Algorithms
https://dspace.mit.edu/handle/1721.1/2989**

- Analogy: Actor performs, critic scores

**PPO and A3C (2016–2017)**

- Read: Schulman et al.: Proximal Policy Optimization Algorithms
https://arxiv.org/abs/1707.06347
- Read: Mnih et al.: Asynchronous Methods for Deep Reinforcement Learning
https://arxiv.org/abs/1602.01783

- Analogy: Many actors learning in parallel

**RLHF (2022)**

**Read: Christiano et al.: Deep Reinforcement Learning from Human Preferences
https://arxiv.org/abs/1706.03741**

- Analogy: Training models with human thumbs up or down

## 3. Generative Models
### 3.1 Autoencoder Based
**Autoencoder AE (1986)**

**Read: Hinton & Salakhutdinov: Reducing the Dimensionality of Data with Neural Networks
https://www.science.org/doi/10.1126/science.1127647**

- Analogy: Zipping and unzipping data

**Denoising Autoencoder (2008)**

**Read: Vincent et al.: Extracting and Composing Robust Features with Denoising Autoencoders
https://www.microsoft.com/en-us/research/wp-content/uploads/2016/02/dae.pdf**

- Analogy: Cleaning a noisy image

**Variational Autoencoder VAE (2013)**

**Read: Kingma & Welling: Auto-Encoding Variational Bayes
https://arxiv.org/abs/1312.6114**

- Analogy: Sampling new ideas from imagination

### 3.2 Adversarial Models
**Generative Adversarial Network GAN (2014)**

**Read: Goodfellow et al.: Generative Adversarial Nets
https://arxiv.org/abs/1406.2661**

- Analogy: Counterfeiter versus detective

**StyleGAN (2018)**

**Read: Karras et al.: A Style-Based Generator Architecture for Generative Adversarial Networks
https://arxiv.org/abs/1812.04948**

**BigGAN (2018)**

**Read: Brock, Donahue, Simonyan: Large Scale GAN Training for High Fidelity Natural Image Synthesis
https://arxiv.org/abs/1809.11096**

CycleGAN (2017)

**Read: Zhu et al.: Unpaired Image-to-Image Translation using Cycle-Consistent Adversarial Networks
https://arxiv.org/abs/1703.10593**

### 3.3 Diffusion Models
- Denoising Diffusion Probabilistic Model DDPM (2015 theory, 2020 practical)

**Read: Ho, Jain, Abbeel: Denoising Diffusion Probabilistic Models
https://arxiv.org/abs/2006.11239**

- Latent Diffusion Model LDM (2022)

**Read: Rombach et al.: High-Resolution Image Synthesis with Latent Diffusion Models
https://arxiv.org/abs/2112.10752**

- Stable Diffusion

  **Read: Based on LDM implementation
https://stability.ai/blog/stable-diffusion-public-release**

- Imagen

  **Read: Saharia et al.: Photorealistic Text-to-Image Diffusion Models with Deep Language Understanding
https://arxiv.org/abs/2205.11487**

- DALL E 2 (2021–2022)

**Read: Ramesh et al.: Hierarchical Text-Conditional Image Generation with CLIP Latents
https://arxiv.org/abs/2204.06125**

- Analogy: Destroy an image with noise then learn to reverse it

### 3.4 Autoregressive Generators
**PixelRNN (2016)**

**Read: van den Oord et al.: Pixel Recurrent Neural Networks
https://arxiv.org/abs/1601.06759**

**PixelCNN (2016)**

**Read: van den Oord et al.: Conditional Image Generation with PixelCNN Decoders
https://arxiv.org/abs/1606.05328**

- Analogy: Painting pixel by pixel

**GPT, Claude, Gemini (2018–present)**

- Analogy: Predicting the next word forever

### 3.5 Flow Models
**Normalizing Flows (2014)**

**Read: Rezende & Mohamed: Variational Inference with Normalizing Flows
https://arxiv.org/abs/1505.05770**

**RealNVP (2017)**

**Read: Dinh et al.: Density Estimation Using Real NVP
https://arxiv.org/abs/1605.08803**

**Glow (2018)**

**Read: Kingma & Dhariwal: Glow: Generative Flow with Invertible 1×1 Convolutions
https://arxiv.org/abs/1807.03039**
- Analogy: A perfect reversible blender
