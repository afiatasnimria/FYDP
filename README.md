# 🧬 Automated Leukemia Detection & Multi-Class Classification

A deep learning-based framework for automated detection and classification of leukemia from Peripheral Blood Smear (PBS) images using Convolutional Neural Networks (CNNs) and Transfer Learning.

---

## 📌 Project Motivation

Leukemia diagnosis through microscopic examination is:

- Time-intensive  
- Expert-dependent  
- Prone to subjective interpretation  

This project aims to develop a robust AI-assisted diagnostic system that:

- Detects abnormal white blood cells  
- Classifies leukemia into 5 categories  
- Handles class imbalance  
- Provides model interpretability using Grad-CAM  

---

## 🧪 Classification Categories

Let the class set be:

C = {c₁, c₂, c₃, c₄, c₅}

| Class | Description |
|-------|------------|
| c₁ | Healthy |
| c₂ | Acute Lymphoblastic Leukemia (ALL) |
| c₃ | Acute Myeloid Leukemia (AML) |
| c₄ | Chronic Lymphocytic Leukemia (CLL) |
| c₅ | Chronic Myeloid Leukemia (CML) |

---

## 🧠 Methodology

### 1️⃣ Image Preprocessing

Raw input image X is transformed as:

X' = T(X)

Preprocessing includes:

- Image resizing (224×224)
- Gaussian noise reduction
- CLAHE contrast enhancement
- Pixel normalization

---

### 2️⃣ Data Augmentation

To improve generalization:

X̃ᵢ = Aᵢ(X)

Applied transformations:

- Rotation  
- Horizontal & vertical flip  
- Zoom  
- Translation  

---

### 3️⃣ CNN Feature Extraction

Feature representation at layer l:

F(l) = σ(W(l) * F(l−1) + b(l))

Where:
- W(l) = Convolutional weights  
- b(l) = Bias  
- σ = Activation (ReLU)  
- * = Convolution operation  

---

### 4️⃣ Transfer Learning

Model parameters initialized as:

θ = θ_pretrained + Δθ

Pre-trained architectures:
- ResNet
- MobileNet

This improves convergence on small medical datasets.

---

### 5️⃣ Loss Function (Class Imbalance Handling)

Weighted Categorical Cross-Entropy:

L = − Σ w_k y_k log(ŷ_k)

Where:
- w_k = class weight  
- y_k = true label  
- ŷ_k = predicted probability  

---

## 📊 Evaluation Metrics

| Metric | Formula |
|--------|---------|
| Accuracy | (TP + TN) / (TP + TN + FP + FN) |
| Precision | TP / (TP + FP) |
| Recall | TP / (TP + FN) |
| F1-Score | 2 × (Precision × Recall) / (Precision + Recall) |
| G-Mean | √(Sensitivity × Specificity) |

---

## 🔬 Explainability (XAI)

Grad-CAM is used to generate heatmaps highlighting the regions influencing the model's decision.

This improves clinical trust and interpretability.

---

## 📂 Project Structure

leukemia-detection/
│
├── dataset/
├── models/
├── train.py
├── evaluate.py
├── gradcam.py
├── utils.py
├── requirements.txt
└── README.md


---

## 🚀 Installation

```bash
git clone https://github.com/your-username/leukemia-detection.git
cd leukemia-detection
pip install -r requirements.txt
