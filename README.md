# train-llama4
Building LLaMA 4 from Scratch with Python
LLaMA 4 has already faced criticism, as some Reddit users claimed that it couldn’t perform tasks that models already 6 months old can do. Though it is a separate debate, LLaMA 4, in its series, is a new step after Mistral that showcases the strengths of MoE-based models.

In this blog, we are going to create the LLaMA 4 MoE architecture step by step in jupyter notebook from scratch to understand how it is actually created.

Following is the output of our trained 2.2 million-parameter LLaMA MoE on a tiny English dataset for 3000 Epochs (Colab T4 GPU).

Input: Alice

Output: Alice 'without pictures or conversation?'
So she was considering in her own mind (as well as she could, for the
hot day made her feel very sleepy and stupid), whether the pleasure
of making a daisy-chain wo ...

Table of Contents
Llama 4 MoE Architecture Overview
Setting Up the Stage
Define the Training Corpus
Character-Level Tokenization
Encode the Corpus
Define Hyperparameters
Data Preparation for Training
Batching Strategy (Random Sampling)
Model Component Initialization
Rotary Positional Embedding (RoPE) Precomputation
RMSNorm Layers Initialization
Attention Layers Initialization (MHA)
Mixture-of-Experts (MoE) Layers Initialization
Final Output Layer Initialization
Causal Mask Precomputation
Training Setup
Define Loss Function
Training the Model
Text Generation
The Generation Loop
Decode Generated Sequence
Save Model State (Optional)
Conclusion
