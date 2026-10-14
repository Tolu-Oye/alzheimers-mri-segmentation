# AI-Driven Alzheimer's Disease Diagnosis: Multi-Criteria Deep Learning Framework for Hippocampal Segmentation and Clinical Classification


This repository contains the core software pipeline and academic assets for an advanced, deep learning-based diagnostic framework aimed at identifying Alzheimer's Disease (AD) using structural brain Magnetic Resonance Imaging (MRI) data. 

This project bridges theoretical computer vision models and practical clinical applications. It explores state-of-the-art neural architectures to automate the highly labor-intensive process of hippocampal segmentation and perform high-accuracy patient classification.

---

## 📂 Repository Structure

The codebase is organized as follows to support clear separation between raw software code, datasets, and academic documentation:

```text
├── data/          # Link to structural MRI datasets and training cohorts
├── doc/           # Academic research paper 
├── presentation/  # Technical slide decks presenting project outcomes and architecture
├── sources/       # Grounding literature and inspiration papers
└── src/           # Main source directory containing Python implementations
    ├── Alzheimer's Disease Classification.ipynb   # Multi-class diagnostic classification model
    ├── Hippocampus Segmentation.ipynb             # U-Net/U-Net++ segmentation pipelines
    └── requirements.txt                           # Software dependencies and library versions
```

---

## 💻 Core Technical Implementations

### 1. Hippocampus Segmentation (`src/Hippocampus Segmentation.ipynb`)
This module proposes a high-precision framework for identifying Alzheimer's disease using U-Net neural network topologies. 
*   **Methodology:** We design and implement the standard **2D U-Net** and advanced nested **U-Net++** architectures. These models are engineered to isolate and segment the human hippocampus—a critical structural brain biomarker known to undergo severe atrophy in the earliest stages of AD.
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

### Installation:
```bash
# Clone the repository
git clone https://github.com/Tolu-Oye/alzheimers-mri-segmentation.git
cd alzheimers-mri-segmentation

# Install dependencies
pip install -r src/requirements.txt
```

---


**Contact:**  
**Toluwani Ayooluwa Oyewusi**
*PhD Student*
*Department of Computer Science*  
*Email:* toyewusi@ncat.edu
