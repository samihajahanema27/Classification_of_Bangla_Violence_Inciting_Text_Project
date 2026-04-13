# 🧠 Classification of Bangla Violence-Inciting Text

A **Transformer-Based Hybrid Approach** for fine-grained classification of Bangla social media text into:

- Violence  
- Passive Violence  
- Non-Violence  

---

## 📌 Overview

This project proposes a **hybrid ensemble framework** combining:

### Transformer models:
- BanglaBERT  
- XLM-RoBERTa  
- mT5  

### Rule-based features:
- 15 handcrafted linguistic features  

The system improves detection of **implicit and passive violence**, a challenging problem in **low-resource languages like Bangla**.

---

## 🚀 Key Contributions

- 📊 Built a **balanced dataset (29,565 samples)**  
- 🧩 Designed a **two-stage hybrid architecture**  
- ⚙️ Implemented three fusion strategies:
  - Weighted Ensemble  
  - Confidence-Based Routing  
  - Stacking Meta-Learner  
- 🏆 Achieved **F1-score: 0.8211 (state-of-the-art improvement)**  

---

## 🏗️ Methodology

### 🔹 Stage 1: Feature Extraction

**Transformer outputs:**
- Probability vectors (3 classes × 3 models = 9 features)

**Rule-based extractor:**
- 15 linguistic features (keywords, patterns, statistics)

➡️ Combined into a **24-dimensional feature vector**

---

### 🔹 Stage 2: Fusion Strategies

| Strategy | Description |
|----------|------------|
| Weighted Ensemble | Class-wise weighted averaging |
| Confidence Routing | Threshold-based model selection (τ = 0.7) |
| Stacking Meta-Learner | Random Forest (200 trees, depth=10) |

---

## 📊 Results

| Model | F1 Score |
|------|--------|
| BanglaBERT | 0.8112 |
| XLM-RoBERTa | 0.7528 |
| mT5 | 0.4832 |
| Rule-Based | 0.4652 |
| **Stacking Meta-Learner** | **0.8211** |

---

## 📁 Dataset

Combined from:
- Bangla Hate Speech & Emotion Dataset  
- Bengali Abusive Language Dataset  

- Final size: **29,565 samples**  
- Balanced across **3 classes**

---

## 🧪 Per-Class Performance

| Class | Best F1 |
|------|--------|
| Non-Violence | ~0.90 |
| Passive Violence | ~0.73 |
| Violence | ~0.80 |

---

## ⚠️ Challenges

- Detecting **implicit / passive violence**  
- Code-mixed and informal Bangla text  
- Cultural and contextual nuances  

---

## 📷 Example Output

Confusion matrix for confidence routing:

![Confusion Matrix](Figures/results/cm_confidence_routing.pdf)

---

## 🛠️ Tech Stack

- Python  
- PyTorch / Transformers  
- Scikit-learn  
- Bangla NLP preprocessing tools  

---

## 📌 Future Work

- Domain-adaptive pretraining  
- Larger transformer models  
- Dialect-aware training  
- Explainable AI integration  

---


## 👩‍💻 Authors

- Samiha Jahan Ema
- Antu Chowdhury  
- Farhan Ershad  
- Umme Humaira  

---

## 📜 License

This project is for **academic and research purposes**.

---

## ⭐ Acknowledgement

Inspired by recent advances in **transformer-based NLP** and **low-resource language research**.
