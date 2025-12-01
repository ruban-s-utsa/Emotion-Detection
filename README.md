# Emotion & Sentiment Detection in Video Conferencing  
### A Comparative Study of EECNN, EECNN-ResNet, PM-ViT, and POSTER  
**Author:** Ruban Sampath · Group 7 · UTSA – Computer Vision  
**Semester:** Fall 2025  

---

## 📌 Project Overview  
Video conferencing has become a core part of business communication.  
In sales calls, customer sentiment and emotional engagement strongly influence deal outcomes — yet these signals are rarely measured or analyzed.

This project investigates **state-of-the-art emotion recognition models** and evaluates their performance on both **benchmark datasets (RAF-DB, AffectNet)** and **real video call frames**.

We compare four modern architectures:

- **EECNN** – Lightweight attention CNN  
- **EECNN-ResNet** – Custom hybrid ResNet-based model  
- **POSTER** – Pyramid Cross-Fusion Transformer (best model)  
- **PM-ViT** – Progressive Modulation Vision Transformer  

The goal is to determine which model is **most accurate**, **most stable**, and **most practical** for analyzing emotional cues in video conferencing, especially in the context of **sales engagement analytics**.

---

## 🌐 Project Webpage  
A full project webpage including abstract, results, visualizations, and demos:

👉 **[Project Webpage (Google Sites)](ADD YOUR WEBSITE LINK HERE)**

---

## 🖼 Poster  
The final 1-slide research poster used for presentation:

<img src="/Poster.png" width="1100">

---

## 📚 Datasets  
The models were trained/evaluated on three datasets:

- **RAF-DB** (Primary Benchmark)  
- **AffectNet subset** (Used for PM-ViT)  
- **Sales Call Frames** (Real-world generalization testing)

Dataset preprocessing scripts are available in the `data/` and `notebooks/` folders.

---

## 🧠 Models Evaluated  
### **1. POSTER (Best Overall)**
- Accuracy: **90.22%** on RAF-DB  
- Strongest across all 7 emotion classes  
- Fast convergence (10 epochs)  
- Excellent per-class F1

### **2. EECNN-ResNet (Best Real-World Robustness)**
- Accuracy: **83.70%**  
- Highly stable on real video calls  
- Strong generalization under occlusion, lighting variation, and non-frontal faces  

### **3. EECNN**
- Accuracy: **67.18%**  
- Fastest and lightest model  
- Performs well on occlusions but weaker overall accuracy  

### **4. PM-ViT (AffectNet)**
- Accuracy: **63.30%**  
- Best diversity/generalization  
- Trained on large-scale in-the-wild faces  

---

## 📊 Results Summary  

### **Model Accuracy Comparison**
| Model | Accuracy |
|-------|----------|
| **POSTER** | **90.22%** |
| **EECNN-ResNet** | **83.70%** |
| **EECNN** | **67.18%** |
| **PM-ViT** | **63.30%** |

---

### **PER-CLASS PERFORMANCE (POSTER – Best Model)**

| Emotion | Precision | Recall |
|---------|-----------|--------|
| Happy | 96.45% | 96.29% |
| Neutral | 87.45% | 89.12% |
| Sad | 86.71% | 88.70% |
| Surprise | 89.16% | 89.97% |
| Anger | 87.10% | 83.33% |
| Disgust | 77.48% | 73.12% |
| Fear | 75.38% | 66.22% |

---

## 🖥 Sales Call Emotion Analysis  
We applied the trained models on real sales call frames extracted from Zoom/Teams recordings.

Observations:
- EECNN-ResNet and POSTER were **most stable** under low-light and partial-face conditions.  
- Models consistently detected **neutral**, **happy**, and **surprise** states.  
- Emotion changes over time aligned with conversation patterns, enabling **engagement timelines**.  

Include your images/demos here:


---

## 🚀 Best Model Checkpoints
Link -> https://drive.google.com/drive/folders/1TU0g_nf5phi0p5BcdsvIMy75kC9gEImG?usp=sharing

---

🧩 Future Work
- Add video-level temporal modeling (LSTMs, GRUs, Video Transformers)
- Train on more real-world sales call datasets
- Build a multi-modal system including audio sentiment
  
🙏 Acknowledgements
- UTSA Computer Vision Course
- RAF-DB and AffectNet dataset creators
- POSTER and PM-ViT original authors
- Google Colab (T4 GPU)
