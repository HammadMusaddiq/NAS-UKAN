# 🧬 NAS-UKAN: Neural Architecture Search for U-KAN-based Biomedical Image Segmentation

NAS-UKAN is a sampling-based **Neural Architecture Search (NAS)** framework built on the **Kolmogorov–Arnold Network (U-KAN)** backbone for high-precision, efficient biomedical image segmentation.  
Instead of relying on fixed architectures, NAS-UKAN automatically discovers dataset-specific model configurations using a composite score:

NAS-UKAN achieves state-of-the-art segmentation results across BUSI, GlaS, and CVC-ClinicDB datasets with significantly reduced computational cost.

---

## 📌 Project Status
🚧 **Training code will be released after paper acceptance.**  

---

## 📷 NAS-UKAN Architecture

> `![NAS-UKAN Architecture](architecture.png)`  
>  
> *Figure: Overall architecture integrating U-KAN backbone with sampling-based NAS.*

---

## ⭐ Key Features

- **KAN-based segmentation backbone (U-KAN)** enabling strong nonlinear representation learning  
- **Sampling-based NAS** that explores dataset-specific configurations  
- **Lightweight yet accurate**:  
  - *22.1% FLOPs reduction* (14.02 → 10.93 GFLOPs) vs. Seg-UKAN  
  - Slight model-size increase (6.85M → 7.76M parameters)  
- **Generalizes across modalities**: ultrasound, histology, colonoscopy  
- **Superior performance** compared to U-Net, U-Net++, U-NeXt, U-Mamba, Seg-UKAN, and more  
- Modular design inspired by the original **U-KAN** implementation

---

## 📦 Dataset Information

NAS-UKAN supports three biomedical image segmentation datasets:

### **1. BUSI (Breast Ultrasound Dataset)**
🔗 https://www.kaggle.com/datasets/aryashah2k/breast-ultrasound-images-dataset

### **2. GlaS (Gland Segmentation) Dataset**
🔗 https://warwick.ac.uk/fac/cross_fac/tia/data/glascontest

### **3. CVC-ClinicDB (Polyp Segmentation)**
🔗 https://www.dropbox.com/scl/fi/ky766dwcxt9meq3aklkip/CVC-ClinicDB.rar?rlkey=61xclnrraadf1niqdvldlds93&e=4&dl=0

---

## 🗂️ Processed Data (No Additional Preprocessing Required)

We use the **processed data provided in the official U-KAN repository**.  
You can directly download the processed BUSI, GlaS, and CVC datasets and place them in the `inputs/` directory.

---

## 📊 Quantitative Results

### **Performance comparison on BUSI, GlaS, and CVC datasets**

| **Method**              | **BUSI IoU** | **BUSI Dice** | **GlaS IoU** | **GlaS Dice** | **CVC IoU** | **CVC Dice** |
|-------------------------|--------------|----------------|--------------|----------------|-------------|--------------|
| U-Net                   | 57.22±4.74   | 71.91±3.54     | 86.66±0.91   | 92.79±0.56     | 83.79±0.77  | 91.06±0.47   |
| Att-U-Net               | 55.18±3.61   | 70.22±2.88     | 86.84±1.19   | 92.09±0.65     | 84.52±0.51  | 91.46±0.25   |
| U-Net++                 | 57.41±4.77   | 72.11±3.99     | 88.30±0.94   | 93.53±0.84     | 85.91±0.73  | 92.86±0.55   |
| U-NeXt                  | 59.06±1.63   | 73.08±1.32     | 84.51±0.97   | 91.55±0.73     | 84.32±0.48  | 93.86±0.17   |
| Rolling-U-Net           | 61.00±0.64   | 74.67±1.24     | 86.42±0.90   | 92.67±0.58     | 87.52±1.32  | 90.48±0.83   |
| U-Mamba                 | 61.81±1.23   | 76.50±2.07     | 87.01±0.92   | 93.30±0.42     | 87.66±0.37  | 96.01±0.39   |
| Seg-UKAN                | 63.38±2.83   | 76.40±2.20     | 87.64±0.32   | 93.70±1.16     | 85.03±0.51  | 91.98±0.29   |
| **NAS-UKAN (--no-kan)** | **64.35±1.86** | **77.22±1.92** | **89.72±0.64** | **94.50±0.32** | **87.06±0.52** | **96.01±0.15** |
| **NAS-UKAN (Ours)** ⭐  | **67.01±1.42** | **79.10±1.52** | **90.13±0.22** | **94.84±0.12** | **87.27±0.74** | **93.20±0.49** |

---

## 🚀 Usage

Training, NAS search, and full pipeline code will be released after paper acceptance.  

---

## 🙏 Acknowledgements

This work builds upon the excellent **U-KAN** implementation provided by the CUHK-AIM Group.

🔗 Official U-KAN repository:  
https://github.com/CUHK-AIM-Group/U-KAN

We gratefully acknowledge their contributions and open-source support.

---



