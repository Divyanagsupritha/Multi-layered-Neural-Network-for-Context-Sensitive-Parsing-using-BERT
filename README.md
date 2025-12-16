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
![Architecture Diagram](Image/NLP_Architecture.png)

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
