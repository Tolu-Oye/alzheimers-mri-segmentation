# AI-Driven Alzheimer's MRI Segmentation Pipeline: Research Prototype & Technical Roadmap

This repository houses the computational code, research documentation, and development roadmap for an artificial intelligence system optimized for high-precision, automated segmentation of the human hippocampus from 3D structural MRI scans. 

The core of this project focuses on applying and optimizing deep convolutional networks (**3D U-Net** and nested **U-Net++** architectures) to serve as automated diagnostic aids for identifying early-stage neurodegeneration associated with Alzheimer's Disease (AD).

---

## 📂 Current Repository Structure

The repository is organized to maintain complete transparency, linking functional computational prototypes directly with academic research documentation:

```text
├── data/          # Baseline structural MRI datasets and preprocessing pipelines
├── doc/           # Academic research reports and drafts documenting model design and findings
├── presentation/  # Technical slide decks and visualizations presenting model performance
├── sources/       # Core literature, mathematical foundations, and peer-reviewed inspiration
└── src/           # Core computational codebase and scripts
    ├── Alzheimer's Disease Classification.ipynb   # Exploratory network training for AD classification
    ├── Hippocampus Segmentation.ipynb            # Active 3D U-Net and U-Net++ segmentation prototypes
    └── requirements.txt                          # Python library dependencies (PyTorch, SimpleITK, etc.)
```

---

## 🛠️ Current Technical Implementation

The files currently hosted in the `/src/` folder represent the verified academic prototypes developed during advanced graduate-level computer vision research at the Illinois Institute of Technology:

1. **`Hippocampus Segmentation.ipynb`**: 
   * A functional PyTorch-based Jupyter Notebook that constructs, compiles, and trains 3D U-Net and nested U-Net++ segmentation pipelines.
   * Features localized loss functions designed to address spatial class imbalance (as the hippocampus occupies <0.5% of the total 3D brain volume).
   * Generates spatial overlap metrics comparing automated segmentations against base annotations.
2. **`Alzheimer's Disease Classification.ipynb`**:
   * Experimental modeling utilizing deep convolutional feature extractors to classify structural brain changes along the clinical spectrum (Cognitively Normal vs. Alzheimer's).
3. **`requirements.txt`**:
   * Outlines the complete computational environment, utilizing industry-standard libraries including `torch` (PyTorch), `torchvision`, `SimpleITK` (for medical image processing), `nibabel` (for NIfTI file operations), and `numpy`.

---

## 📈 Research Expansion & Technical Roadmap (Ph.D. Phase)

To transition this codebase from a highly successful academic prototype into a mature, clinically validated diagnostic platform, we are actively executing a multi-phase engineering and research roadmap. 

This expansion directly leverages our newly approved **Data Use Agreements (DUAs)** with major federal and institutional clinical registries.

```
                  [ CURRENT PHASE ]                                            [ EXPANSION ROADMAP ]
┌──────────────────────────────────────────────────┐        ┌──────────────────────────────────────────────────┐
│             Academic Prototypes                  │        │          Clinical Scaling & Validation           │
│  • Single-slice Jupyter Notebooks (U-Net)        │        │  • Modular Python Pipelines (src/preprocessing/) │
│  • Course-level baseline datasets                │ ───═─> │  • Multi-Cohort Ingestion (ADNI & OASIS 1 & 2)   │
│  • Basic spatial overlap metrics                 │        │  • Dice Score & Hausdorff HD95 Benchmarks        │
│  • Isolated academic reports                     │        │  • Interactive Streamlit Clinical Web Demo       │
└──────────────────────────────────────────────────┘        └──────────────────────────────────────────────────┘
```

### Phase 1: Modularization and Dataset Ingestion (Active)
* **Goal**: Refactor current Jupyter notebooks (`.ipynb`) into robust, modular Python modules (`.py` files) structured for high-throughput batch execution.
* **Data Integration**: Build customized pipeline dataloaders (`src/data_loaders/`) specifically engineered to ingest and preprocess clinical scans from our recently approved external databases:
  * **Alzheimer's Disease Neuroimaging Initiative (ADNI)** (T1-weighted structural MRI MPRAGE scans).
  * **Open Access Series of Imaging Studies (OASIS-1 & OASIS-2)** (Cross-sectional and longitudinal cohorts).

### Phase 2: Standardized Clinical Benchmarking
* **Goal**: Generate rigorous, publishable performance evaluations that meet medical-imaging peer-review standards.
* **Execution**: Implement and track strict clinical-grade validation metrics comparing model outputs directly against expert manual ground-truth segmentations:
  * **Dice Similarity Coefficient (DSC)**: Target spatial overlap score of $\ge 0.88$.
  * **Hausdorff Distance (HD95)**: Target boundary distance error of $\le 2.0\text{ mm}$.
  * **Intersection over Union (IoU)**: Target index of $\ge 0.79$.

### Phase 3: Integration of Multi-Criteria Decision-Making (MCDM) Evaluation
* **Goal**: Bridge the gap between computational accuracy and real-world clinical deployment constraints.
* **Execution**: Implement our peer-reviewed, published MCDM mathematical model (`src/evaluation/`) to analyze the complex trade-offs of deploying deep learning models in resource-constrained clinic environments:
  $$\text{Model Suitability Score} = w_1(\text{Accuracy}) - w_2(\text{Inference Latency}) - w_3(\text{VRAM Footprint})$$

### Phase 4: Interactive Clinician Interface (Streamlit Demo)
* **Goal**: Enable direct, zero-code software evaluation by clinical partners and radiologists.
* **Execution**: Construct a lightweight, local web dashboard (`app/clinical_demo.py`) utilizing Streamlit. The application will allow clinical researchers to drag-and-drop a 3D NIfTI MRI volume, scroll through 3D slice planes, visualize the automated hippocampal segmentation overlay in real-time, and generate download-ready volumetric progression reports.

---

## 🤝 Open Science & Academic Collaboration

This pipeline is maintained as an open-source, public-interest asset to accelerate the development of reliable, non-invasive early-screening technologies. 

We actively welcome stars, forks, and clinical collaboration inquiries from machine learning engineers, neuroscientists, and radiologists.

For technical inquiries or data-sharing collaborations, please contact:
* **Toluwani Ayooluwa Oyewusi**
* *Department of Computer Science*
* *Email:* [Your Email Address]
