# MIT Intro to Deep Learning Course Notes
- Course webpage: [introtodeeplearning](http://introtodeeplearning.com/)
- My course repo: [mit_intro_to_dl_2024](https://github.com/zwimpee/mit_intro_to_dl_2024)
## Lecture 1
### 1. Introduction: What is deep learning and why now?
Deep learning is quickly becoming a ubiquitous framework on which a number of paradigm shifting technologies are being built. This is fairly well understood and is easily observable for many people. What is less clear, however, is the answer to the following question: *why now?*
We may begin to answer this (loosely) in 3 different parts:
#### 1. **Big Data**
- **Larger datasets:**
    - One does not have to go back very many years in order to see that the rate at which the  datasets being used to train deep learning models is increasing in size is itself accelerating. For example (ImageNet)[TODO: Link to ImageNet] was first released in {year imagenet was first released}, and at the time represented by far the largest curated and labeled dataset ever compiled by humans. It was not even close, in fact. Despite this massive achievment, ImageNet has gone on to be dwarfed in size by typical training datasets we deal with and construct ourselves today. 
    - The ability to scale DL capabilities appears to be deeply coupled, at least in some sense, to the ability to scale the creation of massive high quality datasets. Even the constraint that the data must be labeled has started to be relaxed due to recent advancements in unsupervised and semi/self-supervised training techniques, but it does still seem to be the case that you can never have enough raw data, and that getting more will in one way or another result in better performance.
- **Easier collection and storage:**
    - Modern file compression algorithms and efficient file formats have allowed for what previously would have required massive (literally) infrastructure to store to be manageable with low-grade consumer hardware (a 1TB dataset for a college/toy project used to would have been considered highly over-ambitous, and quite overkill, whereas that size is rather typical nowadays for any github repo you come across with a newly finetuned LLM)
#### 2. **Hardware**
- **GPUs:**
    - Rise up, gamers!!!
    - *Nvidia stock to the moon!*
- Massively parallelizable
    - <u>*CUDA kernel goes BRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRRR!*</u>
#### 3. Software
- **Improved techniques:**
    - Gradient descent algorithms
        - Manifold hypothesis
        - Higher order approximations
    - Quantization/PEFT:
        - Quantized models
        - LORA / GaLore
    - Distillation / Teacher-student training
        - Embeddings are all you need?
        - Representation theory
        - Overlap with theoretical physics / mathematics holography
    - RL/RLHF
        - DPO go BRRRRRRRRRRRRRRRRRRRRRRR!
        - Video games as training grounds for agents
        - Alignment
- **New Models:**
    - Multimodal explosion
    - From RNNs and CNNs, to Transformers, and back again
    - RAG / Sparse Vector Search Retrievers and Embeddings
    - Quantum ML / Thermodynamic computing
- **Toolboxes:**
    - <s>Tensorflow is dead, all hail PyTorch</s>
        - Pytorch is dead, all hail JAX!
### 2. The Perceptron: The structural building block of deep learning
- **TODO: Go back and fill out incomplete sections**
#### 1. Forward Propagation
A perceptron can be thought of as just a single neuron.


#### 2. Non-linear activation functions
- **Sigmoid:**
    - $f(x) = \frac{1}{1 + e^{-x}}$
    - **Pros:**
        - Smooth, differentiable
        - Monotonic
        - Bounded
    - **Cons:**
        - Vanishing gradient
        - Saturated neurons
        - Not zero-centered
- **Tanh:**
    - $f(x) = \frac{e^x - e^{-x}}{e^x + e^{-x}}$
    - **Pros:**
        - Smooth, differentiable
        - Monotonic
        - Zero-centered
    - **Cons:**
        - Vanishing gradient
        - Saturated neurons
- **ReLU:**
    - $f(x) = \max(0, x)$
    - **Pros:**
        - Simple, efficient
        - Non-saturating
        - Zero-centered
    - **Cons:**
        - Dying ReLU problem
        - Not smooth, not differentiable
