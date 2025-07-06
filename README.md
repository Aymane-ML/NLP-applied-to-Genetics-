# NLP-applied-to-Genetics-

# 🧬 EIAV DNA Sequence Clustering via 3-mer Analysis (NLP for Genomics)

### 📌 Project Overview

This project is part of a broader effort to develop an **AI system for genomic sequence analysis**, applying techniques directly inspired by **Natural Language Processing (NLP)**. The core idea is to extract **vector representations** of DNA sequences from the **EIAV (Equine Infectious Anemia Virus)** using **3-mer decomposition**, and then apply unsupervised learning techniques to cluster the sequences based on biological similarity.

Although the current notebook focuses on **EIAV**, the same pipeline has also been tested on **HIV-1**, **HIV-2**, and **SIV** sequences as part of the same research.

---

### 🧠 NLP-Inspired Approach for DNA

This project adopts a clear **NLP-based methodology** applied to genomic data:

- 📚 **Tokenization** of DNA sequences into **3-mers**, just like trigrams in NLP.
- 📊 **Bag-of-3-mers** model (analogous to Bag-of-Words).
- 💡 **Word2Vec** embeddings trained on the 3-mers to capture local nucleotide context.
- 🔗 **Node2Vec** embeddings learned from graph representations of sequence similarity or co-occurrence.
- 🧩 **Unsupervised clustering** (KMeans) on the embedded sequences.

This highlights how concepts from NLP and representation learning can be transferred to **understand the “language of DNA”** and detect structure in biological sequences.

---

### 🔍 Data Collection

All DNA sequences were collected via **automated web scraping from NCBI GenBank**, enabling scalable and reproducible acquisition of viral genomes.

---

### ⚙️ Pipeline Overview

1. **FASTA Parsing**  
   DNA sequences are loaded from NCBI GenBank FASTA files using Biopython.

2. **3-mer Tokenization**  
   Each sequence is split into overlapping 3-mers (64 possible combinations).

3. **Feature Engineering**
   - Bag-of-3-mers frequency matrix  
   - **Word2Vec** embeddings of 3-mers  
   - **Node2Vec** embeddings of sequence graphs  

4. **Dimensionality Reduction**  
   **PCA** and **t-SNE** are used to reduce high-dimensional data for visualization.

5. **Unsupervised Clustering**  
   **KMeans** clustering is applied to group sequences by their vector representation. The elbow method helps determine the number of clusters.

6. **Visualization & Interpretation**  
   Visual inspection of clusters and 2D embeddings to detect sequence patterns and similarity.

---

### 🧪 Tools & Libraries

- **Python 3**
- **Biopython** – for FASTA file parsing
- **Pandas / NumPy** – data manipulation
- **Gensim** – Word2Vec training
- **Node2Vec** – graph embeddings
- **NetworkX** – graph construction
- **Scikit-learn** – clustering, PCA, t-SNE
- **Matplotlib / Seaborn** – plotting

---

### 🎯 Applications

- **DNA sequence representation** using NLP-inspired models
- **Alignment-free classification** of viral sequences
- **Detection of genetic similarity and viral strain clusters**
- Foundation for AI systems that learn from raw genomic data
- Bridging **NLP, graph learning, and genomics**

---

### Author

Aymane Mimoun

MSc in Applied Mathematics
Project conducted during a Data Scientist Researcher internship at AP-HP (2024)
