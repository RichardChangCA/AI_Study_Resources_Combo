<b>Unsupervised Learning & Semi-Supervised Learning & Self-Supervised Learning</b>

1. Medium with Youtube, What is Self-Supervised Learning? | Will machines ever be able to learn like humans? https://medium.com/what-is-artificial-intelligence/what-is-self-supervised-learning-will-machines-be-able-to-learn-like-humans-d9160f40cdd1

2. CS294-158 UC Berkeley Deep Unsupervised Learning

<b>Lecture 1: Introduction</b>

Unsupervised Learning: Rapidly advancing field thanks to compute; deep learning engineering practices; datasets; lot of people working on it. Not just an academic interest topic: production level impact(example: BERT is in use for Google Search and Assistant). What is true now may not be true even a year from now(example: self-supervised pre-training was way worse than supervised in computer vision tasks like detection/segmentation last year. Now it is better). Language Modelling(GPT), Image Generation(conditional GANs), Language pre-training(BERT), vision pre-training(CPC/MoCo) starting to work really well. Good time to learn these well and make very impactful contributions. Autoregressive Density Modelling, Flows, VAEs, UL for RL, etc. have huge room for improvement. Great time to work on them. 

<b>Lecture 2: Autoregressive Models</b>

Autoregressive model is an expressive Bayes net structure with neural network conditional distributions yields an expressive model for p(x) with tractable maximum likelihood training. Masked Autoencoder for Distribution Estimation(MADE). Masked Attention: A recurring problem for convolution: limited receptive field —> hard to capture long-range dependencies. 
