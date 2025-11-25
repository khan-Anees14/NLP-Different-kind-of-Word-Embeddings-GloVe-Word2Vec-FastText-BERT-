# 📘 Multi‑Label Text Classification — Embedding Model Comparison  
GPU‑Trained Models: **GloVe | Word2Vec | FastText | BERT**

---

## 📌 Overview  
This repository compares four embedding approaches for multi‑label text classification.  
All models were trained on GPU and evaluated using standard metrics.

---

## 🧠 Model Architectures  

### **1. GloVe / Word2Vec / FastText (MLP Classifier)**  
- Input: 50–300‑D embeddings  
- Layers: Linear → ReLU → Dropout → Linear  
- Loss: BCEWithLogitsLoss  
- Optimizer: Adam  

### **2. BERT (Transformer Encoder)**  
- Base model: `bert-base-uncased`  
- Tokenizer: WordPiece  
- Fine‑tuned classification head  

---

## 📊 Training Curves (Synthetic)  
Accuracy improves fastest in BERT, slowest in GloVe.

![Training Curve Placeholder](metrics/training_curve.png)

---

## 🧪 Evaluation Metrics (GPU Results — Synthetic)  

| Model | Accuracy | Precision | Recall | F1 | AUC |
|------|----------|-----------|--------|----|-----|
| **GloVe** | 0.82 | 0.80 | 0.78 | 0.79 | 0.86 |
| **Word2Vec** | 0.84 | 0.82 | 0.81 | 0.81 | 0.88 |
| **FastText** | 0.87 | 0.85 | 0.84 | 0.84 | 0.91 |
| **BERT** | **0.93** | **0.91** | **0.90** | **0.90** | **0.96** |

---

## 🔍 Confusion Matrices  
(Not actual figures — placeholder descriptions)

- **GloVe:** High confusions for similar topics  
- **FastText:** Better generalization due to subword info  
- **BERT:** Clean diagonal matrix with minimal error  

---

## 🏁 Conclusion  
- Classical embeddings perform decently  
- FastText handles out‑of‑vocabulary tokens better  
- **BERT significantly outperforms all others** due to contextual embeddings  

---

