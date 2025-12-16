# Multi-layered-Neural-Network-for-Context-Sensitive-Parsing-using-BERT
## 📄 Research-Based NLP Project
This repository contains the **implementation of our research work**:

> **“Multi-layered Neural Network for Context-Sensitive Parsing using BERT”**

The project presents a **deep neural dependency parser** that combines **BERT-based contextual embeddings** with **BiLSTM sequence modeling** to perform **context-sensitive syntactic parsing**.

---

## 🔍 Problem Statement
Traditional dependency parsers often struggle with:
- Context sensitivity
- Long-range dependencies
- Ambiguous sentence structures

This project addresses these challenges by integrating **contextualized word representations (BERT)** with **multi-layer neural networks**, enabling more accurate interpretation of syntactic relationships in natural language.

---

## 🎯 Objectives
- Build a **context-sensitive dependency parser**
- Predict **syntactic head indices** for each token
- Capture **long-range and coordinated dependencies**
- Evaluate performance on a standard linguistic benchmark
- Provide interpretable dependency tree outputs

---

## 📚 Dataset
- **Universal Dependencies (UD) – English Web Treebank**
- Format: `.conllu`
- Contains:
  - Tokens
  - POS tags
  - Dependency heads
  - Dependency relations

---

## 🏗️ System Architecture
The model follows a **multi-layer neural architecture**:
<p align="center">
  <img src="Image/NLP_Architecture.png" alt="Model Architecture" width="400">
</p>


1. **Tokenization**
   - `BertTokenizerFast`
   - Preserves word–token alignment

2. **Contextual Embeddings**
   - Pre-trained `bert-base-cased`
   - 768-dimensional embeddings

3. **Sequence Modeling**
   - Bi-directional LSTM (BiLSTM)
   - Captures forward & backward dependencies

4. **Prediction Layer**
   - Linear regression layer
   - Predicts dependency head indices

---
## 📊 Results and Evaluation

The proposed model was trained and evaluated on the **Universal Dependencies English Web Treebank** dataset for **15 epochs**.

### 🔹 Quantitative Results
- **Training Loss**
  - Initial loss: **14.4520**
  - Final loss: **1.6555**
  - Indicates stable convergence and effective learning

- **Head Prediction Accuracy**
  - Achieved **66% accuracy**
  - Demonstrates strong syntactic structure learning using contextual embeddings

<p align="center">
  <img src="Images/training_loss.png" alt="Training Loss Curve" width="500">
</p>

---

### 🔹 Qualitative Results (Dependency Tree Visualization)

<p align="center">
  <img src="Images/dependency_example1.png" width="500">
</p>

**Example Sentence:**  
*“He ran to the store before it closed quickly.”*

- Correctly links long-range dependencies
- Captures adverbial modification
- Preserves syntactic hierarchy

---

<p align="center">
  <img src="Images/dependency_example2.png" width="500">
</p>

**Example Sentence:**  
*“If it rains tomorrow, we will stay indoor and watch movies.”*

- Handles conditional clauses
- Captures coordinated verbs
- Maintains subject–verb consistency

---

## 📈 Dataset Analysis

<p align="center">
  <img src="Images/head_distribution.png" width="500">
</p>

- Dataset shows **imbalanced head index distribution**
- Majority of dependencies lie in lower-indexed heads
- Model generalizes well despite imbalance

---

## ✅ Conclusion

This project successfully demonstrates a **context-sensitive deep neural dependency parser** by combining:
- **BERT contextual embeddings**
- **BiLSTM sequence modeling**
- **Linear regression prediction layers**

The steady decrease in training loss and **66% head prediction accuracy** confirm the effectiveness of integrating **context-aware embeddings with deep neural architectures** for syntactic parsing.

The qualitative visualizations further highlight the model’s ability to handle **complex sentence structures**, including coordination, subordination, and long-range dependencies.

---

## 🔮 Future Work
- Extend to **fully labeled dependency parsing**
- Integrate **biaffine attention mechanisms**
- Evaluate on **multilingual UD datasets**
- Optimize for **real-time and low-resource environments**

---

