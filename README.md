# AbDev

**AbDev** is a predictive modeling framework for monoclonal antibody (mAb) biophysical properties.  
It integrates deep learning–derived spatial descriptors (DeepSP) with machine learning models to predict 12 critical developability-related properties directly from antibody variable region sequences.

---

## Overview

AbDev combines:

- **DeepSP** – a deep learning-based model for generating spatial properties from antibody sequences  
- A descriptor engineering pipeline  
- Machine learning models trained to predict experimentally measured biophysical properties  

This framework enables rapid in silico screening of antibody candidates prior to experimental validation.

---

## Pipeline Workflow

### 1️⃣ Feature Preparation

Prepare a CSV file named:

```
Sequence_Info.csv
```

This file must contain the variable region sequences of the mAbs to be analyzed.

---

### 2️⃣ Generate Spatial Properties (DeepSP)

Run:

```
DeepSP.ipynb
```

DeepSP generates **30 spatial descriptors** from antibody sequences.

Output:

```
DeepSP_descriptors_anarci2_Abdev.csv
```

---

### 3️⃣ Predict Biophysical Properties (AbDev)

Run:

```
AbDev.ipynb
```

Output:

```
Prediction_Result.csv
```

This file contains predictions for **12 biophysical properties**, including developability-relevant metrics.

---

## 🔄 Update: Migration from ANARCI to ANARCII

AbDev has transitioned from **ANARCI** to **ANARCII** for antibody sequence numbering.

Install via:

```bash
pip install anarcii
```

### Why this change?
- pip installable
- Improved compatibility with modern Python environments  
- Simplified installation (no legacy HMMER dependency)  
- Active maintenance  

### Important Note

Due to differences in numbering logic and backend implementation, minor variations in IMGT residue assignments may occur.

These changes may propagate to:

- Descriptor calculations  
- Feature engineering steps  
- Downstream prediction outputs  

For strict reproducibility of earlier results, ensure the same numbering backend is used.

---

## Environment Requirements

- TensorFlow == 2.12.0  
- ANARCII  

Example setup:

```bash
pip install tensorflow==2.12.0 anarcii
```

---

## Reproducibility

To reproduce published results:

1. Use the specified TensorFlow version (2.12.0)  
2. Ensure consistent antibody numbering backend  
3. Regenerate spatial descriptors before prediction  

---

## Citation

If you use DeepSP:

> Kalejaye, L., Wu, I.E., Terry, T., & Lai, P.K.  
> *DeepSP: Deep Learning-Based Spatial Properties to Predict Monoclonal Antibody Stability*  
> Computational and Structural Biotechnology Journal, 23:2220–2229, 2024.  
> https://www.csbj.org/article/S2001-0370(24)00173-9/fulltext  

If you use AbDev:

> Wu, I.E., Kalejaye, L., & Lai, P.K.  
> *Machine Learning Models for Predicting Monoclonal Antibody Biophysical Properties from Molecular Dynamics Simulations and Deep Learning-Based Surface Descriptors*  
> Molecular Pharmaceutics, 2024.  
> https://pubs.acs.org/doi/10.1021/acs.molpharmaceut.4c00804  

---
