# FYDP

# Leukemia Detection Using Deep Learning

This project implements an automated leukemia detection and classification system using Convolutional Neural Networks (CNNs) and transfer learning on peripheral blood smear images.

---

## Overview

The goal of this project is to assist in leukemia diagnosis by:

- Detecting abnormal white blood cells
- Classifying leukemia subtypes
- Handling class imbalance
- Providing model explainability using Grad-CAM

---

## Classes

The model classifies images into the following categories:

- Healthy
- Acute Lymphoblastic Leukemia (ALL)
- Acute Myeloid Leukemia (AML)
- Chronic Lymphocytic Leukemia (CLL)
- Chronic Myeloid Leukemia (CML)

---

## Methodology

### Image Preprocessing
- Image resizing (e.g., 224×224)
- Gaussian blur for noise reduction
- CLAHE for contrast enhancement
- Pixel normalization

Mathematical representation:

