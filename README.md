# Topic Discovery and Document Recommendation Using NMF

Discovering hidden topics in 18,000+ newsgroup documents using Non-negative Matrix Factorization (NMF) and building a content-based recommender system.

---

## Overview

When faced with thousands of documents, manually identifying topics is impossible. This project uses NMF to automatically discover hidden topics from raw text and recommend similar documents based on their topic mixtures.

**Dataset:** [20 Newsgroups](http://qwone.com/~jason/20Newsgroups/) — 18,846 posts across 20 newsgroup categories (built into scikit-learn)

---

## Approach

1. **Text preprocessing** — TF-IDF vectorization with custom stop words to remove email header noise
2. **Topic discovery** — NMF with 5 components to find hidden topics
3. **Topic inspection** — top words per component reveal interpretable topics
4. **Document recommendation** — cosine similarity on NMF features finds similar documents
5. **Visualization** — t-SNE confirms clear topic separation in 2D

---

## Topics Discovered

| Topic | Top Words | Interpretation |
|-------|-----------|---------------|
| 0 | game, team, hockey, baseball, players | Sports |
| 1 | windows, drive, dos, card, scsi | Computer Hardware |
| 2 | god, jesus, bible, christian, faith | Religion |
| 3 | key, clipper, chip, encryption, escrow | Encryption / Security |
| 4 | people, gun, government, israel, state | Politics / Guns |

---

## Key Results

- NMF discovered 5 meaningful topics from raw text with **zero labels**
- t-SNE visualization shows **clear separation** between topic clusters
- Recommender system correctly identifies similar documents based on topic mix
- Custom stop words were essential — email header junk (edu, com, nntp, host) dominated topics before removal

---

## Tools & Libraries

- Python 3
- scikit-learn (NMF, TF-IDF, t-SNE, Normalizer)
- matplotlib, numpy

---

## How to Run

```bash
git clone https://github.com/MohamedChaker-bha/topic-discovery-nmf.git
cd topic-discovery-nmf
pip install scikit-learn matplotlib numpy
jupyter notebook topic_discovery_nmf.ipynb
```

The dataset downloads automatically from scikit-learn on first run (~14MB).

---

## Author

**Mohamed Chaker Iben Hadj Amor**  
Data Engineering Student · FSB, Tunisia  
[LinkedIn](https://www.linkedin.com/in/ice-whaley-22a740411/) · [GitHub](https://github.com/MohamedChaker-bha)
