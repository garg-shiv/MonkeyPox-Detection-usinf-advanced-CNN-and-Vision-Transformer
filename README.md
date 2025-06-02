# 🧠 Monkeypox Detection Using Advanced CNN and Vision Transformer

[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)
![Python](https://img.shields.io/badge/Python-3.8+-blue)
![Framework](https://img.shields.io/badge/TensorFlow-2.x-orange)
![Conference](https://img.shields.io/badge/ICCTRDA--2025-Accepted-brightgreen)

> 🚀 This research was accepted for publication at **ICCTRDA 2025**, Springer LNNS series, indexed in **SCOPUS, Web of Science, EI, DBLP**, and other major databases.  
> 📄 Title: _Monkeypox Detection Using Advanced CNN and Vision Transformer_  
> 🔢 Submission ID: **361**

## 📝 Abstract

In response to the global monkeypox outbreak, this project presents a multi-model deep learning pipeline for **automated detection of monkeypox** and other visually similar skin diseases using dermoscopic images. We evaluate four architectures:

- A simple CNN baseline
- A ResNet50V2-based CNN
- A custom Residual CNN with deeper convolutional blocks
- A Vision Transformer (ViT-Base-Patch16)

Using the **Mpox Skin Lesion Dataset v2.0 (MSLD)**, we applied **5-fold cross-validation** to compare spatial feature extraction via CNNs against global context modeling by Transformers.

## 🔍 Key Features

- 📊 Multi-class classification of 6 skin conditions: **Monkeypox, Chickenpox, Cowpox, HFMD, Measles, and Healthy skin**
- 🧠 Architectures implemented:
  - Simple CNN (lightweight baseline)
  - ResNet50V2 (residual learning)
  - Custom CNN with 4 residual blocks
  - ViT-Base-Patch16 (self-attention based)
- 🔁 5-Fold Cross Validation
- 🎯 Attention visualization using rollout techniques (for ViT)
- 📈 Extensive evaluation: Accuracy, F1-score, Confusion Matrix

## 📂 Dataset

- **Name**: Mpox Skin Lesion Dataset v2.0  
- **Size**: 755 images across 6 classes  
- **Source**: [Kaggle - MSLD v2.0](https://www.kaggle.com/datasets/andrewmvd/monkeypox-skin-lesion-dataset)

## 📁 Project Structure

```bash
├── cnn_pipeline.ipynb           # Contains training code for Simple CNN, ResNet50V2, Custom CNN
├── vit_pipeline.ipynb           # Vision Transformer training and attention visualization
├── data/                        # Organized dataset (after preprocessing)
├── results/                     # Accuracy graphs, confusion matrices, model weights
└── README.md                    # This file
```
⚙️ Requirements
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Key libraries used:

TensorFlow 2.x

Keras

HuggingFace Transformers (for ViT)

scikit-learn

matplotlib, seaborn

🚀 Training Instructions
1. CNN Models
Run:

```bash
Copy
Edit
jupyter notebook cnn_pipeline.ipynb
```
2. Vision Transformer (ViT)
Run:

```bash
Copy
Edit
jupyter notebook vit_pipeline.ipynb
```
Configuration
Input Image Size: 224x224

Batch Size: 32 (CNN), 16 (ViT)

Optimizers:

CNNs: Adam

ViT: AdamW + warmup + linear decay

Augmentations: Rotation, Flip, Zoom, Brightness, Contrast, Hue

📊 Results Summary
Model	Mean Accuracy
Simple CNN	35.23%
ResNet50V2-CNN	47.37%
Custom Residual CNN	54.43%
ViT-Base-Patch16	87.70%

📌 The Vision Transformer significantly outperforms CNN-based approaches, showing superior generalization and interpretability for dermoscopic analysis.

📸 Sample Visualizations

Attention Rollout and Fold-wise Accuracy of ViT

📚 Citation (BibTeX)
bibtex
Copy
Edit
@inproceedings{
  title={Monkeypox Detection Using Advanced CNN and Vision Transformer},
  author={Your Name},
  booktitle={International Conference on Communication Technology Research \& Data Analytics (ICCTRDA 2025)},
  year={2025},
  publisher={Springer LNNS}
}
📌 Acknowledgements
Springer LNNS for conference proceedings.

MSLD v2.0 Dataset from Kaggle.

HuggingFace & Keras for model backbones.

📄 License
This project is licensed under the MIT License.

