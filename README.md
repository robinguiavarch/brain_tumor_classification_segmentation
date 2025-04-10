# 🧠 Brain Tumor Analysis with Deep Learning

This repository contains two main Jupyter notebooks, each focusing on a different task in the medical imaging analysis of brain tumors using MRI scans:

- `Brain_tumor_classification.ipynb` → **Tumor classification**
- `Brain_tumor_segmentation.ipynb` → **Tumor segmentation with uncertainty quantification**

---

## 🧠 Brain Tumor Classification with Calibration, Uncertainty, and Explainability

This project focuses on **classification performance, model calibration, uncertainty quantification**, and **explainability** for brain tumor detection from MRI scans.  
We trained various **ResNet architectures** on a multi-class classification task to distinguish between three tumor types and healthy cases. Beyond raw accuracy, our work analyzes the **confidence calibration** of the models (via ECE and Temperature Scaling), estimates **predictive uncertainty** using Monte Carlo Dropout, and provides **visual explanations** through GradCAM to highlight the most relevant brain regions driving the classification.

### 🗂️ Dataset  
- Source: [Brain Tumor Classification - Kaggle](https://www.kaggle.com/datasets/sartajbhuvaji/brain-tumor-classification-mri/data)  
- 3264 JPEG MRI scans (1 per patient)  
- 4 classes:
  - `0`: No tumor
  - `1`: Glioma tumor
  - `2`: Meningioma tumor
  - `3`: Pituitary tumor  
- Splits:
  - **Train set**: 2870 images (note: unbalanced)
  - **Test set**: 394 images

---

## 🧠 Brain Tumor Segmentation with Uncertainty Quantification

This project focuses on **calibration and uncertainty quantification** in the context of brain tumor segmentation using MRI scans.  
The core of our work is not just the segmentation itself, but the analysis and comparison of **model confidence** and **epistemic uncertainty** using both standard CNNs and Bayesian Neural Networks (BNNs).

### 🗂️ Dataset  
- Source: [BraTS 2021 - Kaggle](https://www.kaggle.com/datasets/dschettler8845/brats-2021-task1/data)  
- 1251 volumetric MRI scans (NIfTI format: `.nii.gz`)  
- 4 modalities per scan: `T1`, `T1Gd`, `T2`, `FLAIR`  
- Segmentation masks include 4 classes:
  - `0`: Background / No tumor
  - `1`: Necrotic core
  - `2`: Peritumoral edema
  - `3`: Enhancing tumor (converted from original class 4)  
- Volume shape: `240 x 240 x 155`

---

## 👥 Authors

- Candice Bouquin-Renoux  
- Sarah Garcia  
- Robin Guiavarch
