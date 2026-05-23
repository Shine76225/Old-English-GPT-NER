# Old-English-GPT-NER

This repository contains the implementation and experimental results for the thesis:

**“Named Entity Recognition in Old English: Direct, Translation-based, and Retrieval-Augmented Approaches”**

The project focuses on personal name extraction from Old English historical texts using multiple approaches based on large language models, retrieval augmentation, and neural named entity recognition systems.

---

# Project Overview

Extracting named entities from Old English texts is challenging due to:

- archaic vocabulary
- inconsistent spelling
- limited annotated resources
- domain differences from Modern English

To address these challenges, this research investigates and compares multiple approaches for Old English person name extraction.

---

# Implemented Approaches

## 1. Direct NER

A RoBERTa-based token classification model fine-tuned on annotated Old English NER data.

### Features
- Token-level sequence labeling
- RoBERTa fine-tuning
- Precision / Recall / F1-score evaluation
- Out-of-domain testing on ChronicleA

### Folder
```text
Direct-NER/
```

---

## 2. Translation-Based NER

A pipeline-based approach that:

1. Fine-Tune mBART-large model and translates Old English text into Modern English
2. Applies Modern English NER models
3. Extracts person entities from translated text

### Folder
```text
Translation-Based-NER/
```

---

## 3. Retrieval-Augmented GPT-NER

GPT-4.1 based retrieval-augmented named entity recognition using multiple retrieval strategies.

### Implemented Retrieval Methods
- Zero-shot
- Random Retrieval
- Sentence Similarity Retrieval
- Entity-Level Retrieval
- Hybrid Retrieval
- Self-Verification

### Folder
```text
Retrieval-Augmented-GPT-NER/
```

---

# Dataset

The project uses manually annotated Old English datasets for person name extraction.

Additionally, an out-of-domain evaluation dataset based on ChronicleA historical texts was constructed and used for generalization testing.

---

# Evaluation Metrics

The following evaluation metrics are used:

- Precision
- Recall
- F1-score

---

# Repository Structure

```text
Old-English-GPT-NER/
│
├── Datasets/
├── Direct-NER/
├── Translation-Based-NER/
├── Retrieval-Augmented-GPT-NER/
│
└── README.md
```

---

# Retrieval-Augmented Methods

| Method | Description |
|---|---|
| Zero-shot | No retrieved examples |
| Random Retrieval | Randomly selected demonstrations |
| Sentence Retrieval | Sentence embedding similarity retrieval |
| Entity Retrieval | Entity-level embedding retrieval |
| Hybrid Retrieval | Combination of sentence and entity retrieval |
| Self-Verification | Verification stage for reducing false positives |

---

# Experimental Workflow

1. Prepare Old English datasets
2. Construct retrieval examples
3. Generate GPT-4.1 predictions
4. Apply self-verification
5. Evaluate using Precision, Recall, and F1-score
6. Perform out-of-domain testing on ChronicleA

---

# Technologies Used

- Python
- PyTorch
- Hugging Face Transformers
- RoBERTa
- GPT-4.1
- Sentence Transformers
- Google Colab

---

# Research Contributions

This work provides:

- A comparative study of multiple Old English NER approaches
- Retrieval-augmented GPT-based NER experiments for Old English historical texts
- Hybrid Retrieval method ny combining sentence embeddig and entity embedding for Old English named entity extraction
- Out-of-domain evaluation on ChronicleA historical texts

---

# Author

Shine Khant Aung  
Master Student  
Novosibirsk State University
