# AI-Driven Alzheimer's Disease Diagnosis: Multi-Criteria Deep Learning Framework for Hippocampal Segmentation and Clinical Classification

[![License: MIT](https://img.shields.io/badge/License-MIT-blue.svg)](https://opensource.org/licenses/MIT)
[![Python 3.9.16](https://img.shields.io/badge/python-3.9.16-blue.svg)](https://www.python.org/downloads/release/python-3916/)
[![PyTorch](https://img.shields.io/badge/PyTorch-2.1.0-EE4C2C.svg?style=flat&logo=PyTorch)](https://pytorch.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-FF6F00.svg?style=flat&logo=TensorFlow)](https://www.tensorflow.org/)

This repository contains the core software pipeline and academic assets for an advanced, deep learning-based diagnostic framework aimed at identifying Alzheimer's Disease (AD) using structural brain Magnetic Resonance Imaging (MRI) data. 

This project bridges theoretical computer vision models and practical clinical applications. It explores state-of-the-art neural architectures to automate the highly labor-intensive process of hippocampal segmentation and perform high-accuracy patient classification.

---

## 📂 Repository Structure

The codebase is organized as follows to support clear separation between raw software code, datasets, and academic documentation:

```text
├── data/          # Structural MRI datasets and training cohorts
├── doc/           # Academic research paper detailing our novel methodologies
├── presentation/  # Technical slide decks presenting project outcomes and architecture
├── sources/       # Grounding literature, inspiration papers, and clinical reference materials
└── src/           # Main source directory containing Python implementations
    ├── Alzheimer's Disease Classification.ipynb   # Multi-class diagnostic classification model
    ├── Hippocampus Segmentation.ipynb             # U-Net/U-Net++ segmentation pipelines
    └── requirements.txt                           # Software dependencies and library versions
```

---

## 💻 Core Technical Implementations

### 1. Hippocampus Segmentation (`src/Hippocampus Segmentation.ipynb`)
This module proposes a high-precision framework for identifying Alzheimer's disease using U-Net neural network topologies. 
*   **Methodology:** We design and implement standard **3D U-Net** and advanced nested **U-Net++** architectures. These models are engineered to isolate and segment the human hippocampus—a critical structural brain biomarker known to undergo severe atrophy in the earliest stages of AD.
*   **Objective:** To enhance the segmentation accuracy and structural boundary detection of the hippocampus, reducing manual radiological tracing bottlenecks.
*   **Framework:** Built on **PyTorch**.
*   **Libraries Utilized:**
    *   `OpenCV (cv2)` & `PIL` (Image processing and raw slice handling)
    *   `Pandas` & `NumPy` (Metadata management, structural voxel array manipulation)
    *   `Matplotlib` (Visualization of segmentation masks and training loss curves)
    *   `PyTorch` & `Torchvision` (Neural network construction, optimizer setup, and backpropagation)
    *   `TQDM` (Progress bar tracking for model training epochs)

### 2. Multi-Class Disease Classification (`src/Alzheimer's Disease Classification.ipynb`)
To complement structural segmentation, this module implements a complete deep learning classification pipeline.
*   **Methodology:** This system leverages a fine-tuned **InceptionV3** convolutional neural network to classify patient MRI scans into clinically recognized diagnostic stages.
*   **Ground-Truth Class Labels:**
    1.  *Non-Demented* (Healthy Control)
    2.  *Very Mild Demented* (Early Stage)
    3.  *Mild Demented* (Moderate Stage)
    4.  *Moderate Demented* (Advanced Stage)
*   **Objective:** To output reliable class probability predictions and analyze hyperparameter configurations (learning rates, layer freezing, optimizer weights, and batch sizes) for peak classification metrics.
*   **Framework:** Built on **TensorFlow / Keras**.
*   **Libraries Utilized:**
    *   `os` (Local directory path management)
    *   `numpy` & `matplotlib` (Matrix manipulation and ROC/AUC curves plotting)
    *   `distutils` (System and package configuration)
    *   `scikit-learn` & `imblearn` (Data splitting, confusion matrix calculation, and handling severe class imbalances)
    *   `tensorflow` & `tensorflow_addons` (InceptionV3 model loading, fine-tuning, and metric evaluations)

---

## 🛠️ Requirements & Setup Guide

To run the notebooks and reproduce the results, ensure you have **Python 3.9.16** installed. You can install all required libraries using the provided `requirements.txt` file.

### Complete Software Dependencies:
As specified in `src/requirements.txt`:
*   **Python version:** `3.9.16`
*   **OpenCV (cv2) version:** `4.7.0`
*   **Pandas version:** `2.0.0`
*   **NumPy version:** `1.23.5`
*   **Matplotlib version:** `3.7.1`
*   **PyTorch (torch) version:** `2.1.0.dev20230413`
*   **Torchvision version:** `0.16.0.dev20230413`
*   **PIL version:** `9.4.0`
*   **tqdm version:** `4.65.0`

### Installation:
```bash
# Clone the repository
git clone https://github.com/Tolu-Oye/alzheimers-mri-segmentation.git
cd alzheimers-mri-segmentation

# Install dependencies
pip install -r src/requirements.txt
```

---

## 🚀 Active Project Goals & Ph.D. Research Roadmap

This repository serves as the baseline software foundation for my ongoing doctoral research. Moving forward, my primary scientific milestones and project goals are:

*   **Phase 1: Ingest Clinical-Grade Registries (Active Setup)**  
    We are currently developing modular PyTorch data-loaders to ingest raw 3D T1-weighted MPRAGE scans from our newly approved federal and institutional databases:
    *   **ADNI (Alzheimer's Disease Neuroimaging Initiative)**
    *   **OASIS-1 and OASIS-2 (Open Access Series of Imaging Studies)**
*   **Phase 2: Standardized Metric Validation**  
    We plan to run our U-Net/U-Net++ segmentation pipelines on these massive cohorts, calculating standard clinical-grade benchmarks against manual expert-traced ground-truths:
    *   *Dice Similarity Coefficient (DSC)* (Aiming for $\ge 0.88$)
    *   *95th percentile Hausdorff Distance (HD95)* (Aiming for $\le 2.0\text{ mm}$)
*   **Phase 3: Multi-Criteria Decision-Making (MCDM) Integration**  
    We will integrate our peer-reviewed **Multi-Criteria Decision-Making (MCDM)** evaluation models directly into the pipeline. This mathematical engine will automatically analyze and rank deep learning configurations based on the optimal balance between segmentation accuracy, parameter footprint, GPU VRAM constraints, and edge computational latency.
*   **Phase 4: Clinical Interface Web Portal**  
    We plan to build a lightweight, secure web application (using Streamlit or Gradio) that will allow independent clinical partners and academic radiologists to drop in anonymous 3D MRI scans and immediately inspect automated hippocampal segmentations and volumetric reports.

---

## 🤝 Citation and Academic Collaboration

This repository is maintained in the spirit of open science. We welcome inquiries regarding academic collaboration, clinical testing, or methodological extensions.

If you are using this code or referencing our roadmap, please cite our corresponding publications:
1.  **"Multi-Criteria Evaluation Framework for Deep Learning Architectures in Medical Image Segmentation"**
2.  **"Integrated Fuzzy MCDM Framework for Evaluating AI-Assisted Healthcare Delivery Models for Aging Populations"**

**Contact:**  
**Toluwani Ayooluwa Oyewusi**  
*Department of Computer Science*  
*Email:* toyewusi@ncat.edu
