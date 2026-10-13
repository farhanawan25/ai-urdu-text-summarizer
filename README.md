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
Input Text
↓
Sentence Segmentation
↓
Tokenization
↓
Stop Word Filtration
↓
TF-IDF Calculation
↓
Similarity Matrix Computation
↓
Agglomerative Hierarchical Clustering
↓
Compute Centroid in Each Cluster
↓
Rank Sentences by Proximity to Centroid
↓
Summary

---


---

## 📊 Results

Evaluated on **BBC Urdu news articles** against human-written reference summaries using **ROUGE-1** and **ROUGE-2**.

| Metric | Best Single-Doc Score | Average Across 25 Docs |
|---|---|---|
| ROUGE-1 F-measure | 0.62 | ~0.46 |
| ROUGE-2 F-measure | 0.33 | — |

The system achieved **~46% average accuracy** across 25 documents compared to human summaries, outperforming baseline extractive approaches.

---

## 🗂 Repository Structure
├── Urdu Text Summarizer.ipynb # Main implementation
├── Urdu DataSet/ # Urdu news articles (BBC)
├── Computer Generated Summaries/ # Output summaries
├── comp summary _/ # Comparison summaries
└── Research paper published version.pdf # Conference paper


---

## 🚀 How to Run

```bash
pip install -r requirements.txt
jupyter notebook "Urdu Text Summarizer.ipynb"

🔮 Future Work
Extend from single-document to multi-document summarization

Adapt the framework to other low-resource languages

Integrate additional preprocessing steps for Urdu morphology

---

📖 Citation
If you use this work, please cite:
@inproceedings{khan2024unsupervised,
  title={Unsupervised Learning for Extractive Urdu Document Text Summarization: A Clustering Approach},
  author={Khan, Atif and Ajmal, Obaid and Awan, Farhan Ahmad and Wahid, Fazal},
  booktitle={2nd International Conference on Computing Technologies, Tools and Applications},
  year={2024}
}

---

👤 Author
Farhan Ahmad Awan

---

### 🎯 What This README Does for You

1. **Establishes credibility** — "Published in..." at the top signals this is real research, not a toy project.
2. **Explains the problem** — anyone (recruiter, researcher) understands *why* Urdu summarization matters.
3. **Shows the pipeline** — the ASCII diagram makes the method instantly scannable.
4. **Provides results** — numbers from your paper make it concrete.
5. **Includes citation** — critical for academic work; other researchers can cite you properly.
6. **Links the paper** — the PDF in the repo is a strong asset.

### 📌 How to Add It

```powershell
cd "C:\Users\Farhan\Desktop\Text Summarizer-20261012T092022Z-1-001\Text Summarizer"
notepad README.md
