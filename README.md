# CNN-Powered Emotion Classification with Explainable AI  

Facial Emotion Recognition (FER) using **ResNet50** + **Grad-CAM** Explainability on the FER2013 dataset.

---

## 📌 Project Overview
This project focuses on building an emotion classification model using **deep learning** while also ensuring **interpretability** using **Explainable AI (XAI)** techniques.

**Goal:**  
Identify which facial regions contribute most to specific emotion predictions.

---

## ❓ Problem Statement
How can we classify facial emotions using deep learning *and* understand the reasoning behind the model’s predictions?

---

## 🧠 Why Interpretability?
Most deep learning FER systems work like black boxes. We aim to merge **accuracy + transparency** to:  

- Build trust in predictions  
- Detect model bias and failure cases  
- Visualize what the model “sees” (via Grad-CAM heatmaps)

---

## 🛠️ Methodology / Pipeline
*(Include your pipeline image or steps here if available)*

---

## 📂 Dataset – FER2013

| Property          | Details                      |
|-------------------|------------------------------|
| Images            | 48×48 grayscale face images |
| Classes           | 7 emotions (Angry, Disgust, Fear, Happy, Sad, Surprise, Neutral) |
| Train Samples     | 28,709                      |
| Test Samples      | 3,589                       |
| Source            | Kaggle                      |

[FER2013 Dataset](https://www.kaggle.com/datasets/msambare/fer2013)

---

## 🧬 Model Architecture

- **Backbone:** ResNet50 pretrained on VGGFace2  
- **Loss Functions:**  
  - Stage 1: Triplet Loss → Learning face embeddings  
  - Stage 2: Cross Entropy → Classifying FER2013 emotions  
- **Output:** 512-dim embeddings → fully connected classifier

---

## ⚙️ Training Strategy

| Stage | Objective | Details |
|--------|-----------|---------|
| 1️⃣ Triplet Loss | Learn robust face embeddings | Trained on ~200K images |
| 2️⃣ Cross-Entropy | Fine-tune for emotion classification | Applied class weighting to fix imbalance |
| 🛡️ Regularization | Prevent overfitting | Data augmentation, dropout |

---

## 🔍 Explainability (XAI)

We apply **Grad-CAM** to visualize which parts of the face influence the model's decisions.

- Highlights facial regions most responsible for each emotion  
- Helps detect errors or biases  
- Bridges AI predictions with human reasoning

---

## 📊 Results

| Metric | Validation | Test |
|--------|------------|------|
| Accuracy | **81.35%** | **80.12%** |
| F1 Score | **0.8136** | **0.8015** |
| Loss | 0.5234 | 0.5388 |

⚠ Class imbalance reduces prediction confidence for minority classes.

---

## 🚀 Future Work

- 💡 Use **diffusion-based inpainting** to modify facial expressions controllably  
- ✨ Employ saliency maps to **edit emotions while preserving identity**  
- 🌍 Expand dataset and improve generalization across cultures

---

## 📁 Repository

🔗 Project GitHub: [https://github.com/ziadnasser19/emotion-guided-inpainting](https://github.com/ziadnasser19/emotion-guided-inpainting)

---

## 👤 Connect with the Team

| Name | LinkedIn |
|------|----------|
| Moataz Mohamed | [LinkedIn](https://www.linkedin.com/in/moataz-m-ali-73045b277/) |
| Ziad Nasser | [LinkedIn](https://www.linkedin.com/in/ziad-nasser-96a016279/) |
| Mostafa Bahaa | [LinkedIn](https://www.linkedin.com/in/mostafa-bahaa-32765a221/) |
| Engy Elsarta | [LinkedIn](https://www.linkedin.com/in/engy-elsarta-6a6a06283/) |
| Aseel Janazira | [LinkedIn](https://www.linkedin.com/in/aseel-janazira-98a20333b/) |


Supervised by: Julius Amegadzie  
Project Mentor: Efstathia Soufleri

