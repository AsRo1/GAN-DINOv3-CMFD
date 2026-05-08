# GAN-DINOv3-CMFD: A Hybrid Deep Learning Approach for Copy-Move Forgery Detection

##  Project Overview
This repository contains the official implementation of **GAN-DINOv3-CMFD**, a deep learning-based hybrid framework for digital image copy-move forgery detection. 

The framework combines:
* **Generative Adversarial Networks (GANs)** to generate plausible forged areas and supplement limited forgery training sets.
* **DINOv3 (Distillation with No Labels, version 3)**, a self-supervised Vision Transformer (ViT), to extract high-level global and local features without manual annotations.
* **Spectral Clustering** to separate DINOv3 embeddings into forged and original areas, enabling robust and explainable forgery localization.

This research was presented at the **2025 IEEE 17th International Conference on Computational Intelligence and Communication Networks (CICN)** and achieved an **88.6% F1-score** on the CoMoFoD dataset.

##  Authors
* **Abhay Singh** (Department of Computer Science and Engineering, MNNIT Allahabad)
* **Dr. Anuja Dixit** (Department of Computer Science and Engineering, MNNIT Allahabad)

**DOI:** [10.1109/CICN67655.2025.11367879](https://doi.org/10.1109/CICN67655.2025.11367879)

##  Dataset
The model is trained and evaluated using the **CoMoFoD Dataset**. 
* Original and forged image variants are processed iteratively.
* Binary masks are utilized alongside the images to train the model for precise pixel-level localization.

## 🚀 Setup & Installation

### Prerequisites
Ensure you have the following dependencies installed in your Python 3 environment. 

```bash
pip install torch torchvision timm
pip install tensorflow opencv-python scikit-learn pandas tqdm matplotlib
