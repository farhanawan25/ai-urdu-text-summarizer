# Unsupervised Learning for Extractive Urdu Document Text Summarization

A domain-independent extractive text summarization system for Urdu using **Hierarchical Agglomerative Clustering** — no labeled data required.

> 📄 **Published in:** 2nd International Conference on Computing Technologies, Tools and Applications (ICCTTA)
> 👥 **Authors:** Atif Khan, Obaid Ajmal, Farhan Ahmad Awan, Fazal Wahid
> 🏫 **Affiliation:** Department of Computer Science, Islamia College Peshawar, Pakistan

---

## 📌 Overview

Urdu is spoken by millions across Pakistan, India, and Bangladesh, yet it remains under-resourced in NLP. Most summarization research focuses on English, leaving Urdu with few computational tools.

This project implements **EUTS (Extract Urdu Text Summarizer)** — an unsupervised, domain-independent approach that:
- Segments Urdu text into sentences
- Tokenizes and removes Urdu stop words
- Represents sentences as TF-IDF feature vectors
- Groups similar sentences via **Agglomerative Hierarchical Clustering**
- Selects the most representative sentence (closest to cluster centroid) from each group
- Orders selected sentences as they appeared in the original document

Because it's unsupervised, it works **without annotated datasets or pre-trained models** — a key advantage for low-resource languages.

---

## ⚙️ Methodology
