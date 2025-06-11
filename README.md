# 🌳 Deforestation Detection in the Amazon using U-Net (Sentinel-1 & Sentinel-2)

This repository contains code and documentation for detecting deforestation in the Amazon rainforest using a U-Net deep learning model trained on multi-source satellite data from Sentinel-1 (SAR) and Sentinel-2 (optical).

---

## 📌 Overview

Deforestation is one of the most critical environmental issues, especially in tropical regions like the Amazon. Remote sensing data provides a scalable solution to monitor and detect land cover change over time.

This project uses a U-Net model with combined Sentinel-1 and Sentinel-2 imagery to identify and segment deforested regions in the Amazon.

---

## 🛰️ Data Description


### 📁 Source : https://www.kaggle.com/datasets/akhilchibber/deforestation-detection-dataset

### 🟡 Sentinel-2 (Optical)
- Bands used: B2 (Blue), B3 (Green), B4 (Red), B8 (NIR)
- Resolution: 10m

### ⚫ Sentinel-1 (SAR)
- Bands used: VV, VH
- Resolution: 10m

### 📌 Labels
- Binary segmentation mask:  
  - `0`: Forest  
  - `1`: Deforested area

## 🧠 Model Architecture

- **Architecture**: U-Net
- **Input Channels**: 6 (Sentinel-2: 4 bands + Sentinel-1: 2 bands)
- **Loss Function**: Binary Cross-Entropy
- **Metrics**: Accuracy

## 📊 Results

- **Accuracy**: 0.94
- **Loss**: 0.16

### 📦 Requirements

```bash
python>=3.8
tensorflow>=2.x or pytorch>=1.x
numpy
opencv-python
matplotlib
rioxarray
patchify
