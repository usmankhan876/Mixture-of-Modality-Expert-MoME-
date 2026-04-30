# 🧠 Mixture-of-Modality Experts (MoME) — nnU-Net Pipeline for BraTS

This repository presents a **reproducible deep learning pipeline** built on top of nnU-Net for multimodal medical image segmentation. It includes dataset conversion, validation, preprocessing, and training orchestration, with experimental integration of Mixture-of-Modality Experts (MoME) for multimodal learning research.

---

## 📌 Overview

The project provides a modular pipeline for:

* BraTS 2021 multimodal MRI dataset processing
* Conversion to nnU-Net compatible format
* Dataset integrity validation
* Automated nnU-Net preprocessing and planning
* Baseline training using stock nnU-Net
* Experimental support for MoME-based architectures

The framework is designed for **reproducible research and rapid experimentation in medical image segmentation tasks**.

---

## 📦 Dataset

* BraTS 2021 multimodal MRI dataset

Official source:
[https://www.med.upenn.edu/cbica/brats2021/](https://www.med.upenn.edu/cbica/brats2021/)

> ⚠️ The dataset is not included due to licensing restrictions. Only preprocessing and conversion scripts are provided.

---

## ⚙️ Frameworks & Libraries

* nnU-Net v2
* PyTorch
* MoME (experimental integration)
* nibabel, numpy
* Google Colab / Linux environment

---

## 🚀 Key Features

* Automated BraTS → nnU-Net conversion pipeline
* Label remapping for nnU-Net compatibility
* Dataset validation and sanity checks
* Fully automated preprocessing pipeline
* Baseline nnU-Net training setup
* Modular design for experimental MoME integration

---

## 📘 Pipeline Components

### 1. Dataset Setup

Mounts storage and extracts BraTS dataset for processing.

### 2. Environment Setup

Installs dependencies and configures nnU-Net environment variables.

### 3. Dataset Conversion

Transforms BraTS dataset into nnU-Net format and remaps labels.

### 4. Validation

Performs integrity checks on images, labels, and metadata.

### 5. Preprocessing

Runs nnU-Net planning and preprocessing pipeline.

### 6. Training

Trains baseline 3D nnU-Net model for benchmarking.

### 7. Experimentation

Supports integration of MoME-based architectural modifications.

---

## 📁 Suggested Repository Structure

```text
MoME-BraTS-nnUNet/
│
├── notebooks/
├── scripts/
├── configs/
├── results/
├── README.md
└── requirements.txt
```

---

## 🎯 Research Goal

This project aims to support **reproducible multimodal learning experiments** and provide a clean baseline for comparing standard nnU-Net with MoME-enhanced architectures in medical image segmentation.

---
