# 🧠 GitHub Repository Description (Main README Intro)

### 🔷 Mixture-of-Modality Experts (MoME) — BraTS nnU-Net Pipeline

This repository provides a **modular and reproducible deep learning pipeline** for brain tumor segmentation using the BraTS dataset, built on top of **nnU-Net** and extended experimentation with the **Mixture-of-Modality Experts (MoME)** framework.

The project focuses on:

* BraTS 2021 multimodal MRI segmentation (FLAIR, T1, T1ce, T2)
* Automated dataset conversion to nnU-Net format
* Data validation and integrity checks
* nnU-Net preprocessing pipeline setup
* Baseline training using stock nnU-Net
* Experimental support for MoME-based architecture integration

This repository is designed for **research experimentation, reproducibility, and fast prototyping** in medical image segmentation tasks.

---

### 📦 Dataset

The dataset used in this project is:

* BraTS 2021

You can access it here:

* Official BraTS dataset: [https://www.med.upenn.edu/cbica/brats2021/](https://www.med.upenn.edu/cbica/brats2021/)

> ⚠️ Note: Dataset is not included in this repository due to licensing restrictions. Only preprocessing scripts are provided.

---

### ⚙️ Frameworks Used

* nnU-Net v2
* PyTorch
* MoME (Mixture of Modality Experts – experimental)
* nibabel, numpy
* Google Colab / Linux environment

---

### 🚀 Key Features

* Fully automated BraTS → nnU-Net conversion
* Label remapping for compatibility
* Dataset validation pipeline
* nnU-Net planning & preprocessing automation
* Stock nnU-Net training baseline
* Modular design for MoME integration

---

# 📘 Cell-wise Documentation (for GitHub or Notebook)

You can paste these as **Markdown under each cell** in your notebook or README.

---

## 🟦 Cell 1 — Mount Drive & Dataset Extraction

Mounts Google Drive and extracts the BraTS dataset from a compressed ZIP file.
It ensures the dataset is only extracted once to avoid redundant processing and speeds up repeated experiments.

---

## 🟦 Cell 2 — Dependency Installation (MoME + nnU-Net Setup)

Installs all required dependencies including:

* MoME framework (editable install)
* nnU-Net v2 (clean environment setup)
* medical imaging libraries (nibabel, antspyx)

Also ensures Python environment consistency by refreshing system paths.

---

## 🟦 Cell 3 — nnU-Net Environment Configuration

Defines and sets up the required nnU-Net directory structure:

* Raw dataset directory
* Preprocessed data directory
* Training results directory

These environment variables are required for nnU-Net pipeline execution.

---

## 🟦 Cell 4 — BraTS Dataset Conversion (nnU-Net Format)

Converts BraTS 2021 dataset into nnU-Net compatible structure:

* Renames modalities into nnU-Net format (_0000 to _0003)
* Remaps segmentation labels (4 → 3)
* Generates dataset.json metadata file

This step ensures compatibility with nnU-Net training pipeline.

---

## 🟦 Cell 5 — Dataset Integrity Verification

Performs sanity checks on:

* dataset.json correctness
* image/label file counts
* segmentation label validity

Ensures dataset is correctly formatted before training.

---

## 🟦 Cell 6 — nnU-Net Planning & Preprocessing

Runs nnU-Net automated pipeline:

* dataset fingerprinting
* patch size estimation
* normalization strategy selection
* preprocessing pipeline generation

This is a required step before training.

---

## 🟦 Cell 7 — MoME Trainer Registration & Fixes

Modifies and patches nnU-Net utility functions to ensure compatibility with MoME integration.
Includes:

* network builder alignment
* function signature fixes
* dynamic architecture compatibility

This enables experimental MoME-based architecture support.

---

## 🟦 Clean nnU-Net Installation (Baseline Reset)

Removes modified or broken nnU-Net versions and installs the official stable release.
Ensures reproducible baseline results for comparison with MoME experiments.

---

## 🟦 Cell 8 — Model Training (Baseline nnU-Net)

Trains a 3D full-resolution nnU-Net model on BraTS dataset using:

* standard nnUNetTrainer
* stock architecture (baseline model)
* GPU-based training pipeline

This serves as the **benchmark model** for comparison.

---

## 🟦 Cell 9 — Save Results to Google Drive

Automatically exports trained models, logs, and results to Google Drive for:

* checkpoint preservation
* experiment tracking
* reproducibility

---

# 📌 Suggested GitHub Repo Structure

You can structure your repo like this:

```
MoME-BraTS-nnUNet/
│
├── notebooks/
│   └── pipeline.ipynb
│
├── scripts/
│   ├── dataset_conversion.py
│   ├── validation.py
│   ├── train.py
│
├── configs/
│
├── README.md
└── requirements.txt
```

---
