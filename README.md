# 🧠 Neuromorphic-Inspired Medical Image Segmentation

Lightweight U-Net architecture for retinal vessel segmentation, optimized for neuromorphic crossbar array deployment. Published at **IEEE APSCON 2025**.

## Overview

Standard segmentation architectures (e.g., Attention U-Net) are computationally prohibitive for neuromorphic hardware. This project proposes a lightweight U-Net variant that achieves competitive segmentation quality with 40% reduced compute, making it suitable for resource-constrained edge deployment.

## Key Results

- **Dice score: 0.86** on retinal vessel segmentation
- **40% compute reduction** compared to Attention U-Net
- Custom lightweight architecture with skip connections
- Published at IEEE APSCON 2025

## Model Architecture

```
Custom Lightweight U-Net (mynet_model)
├── Input: 256 × 256 × 3 (retinal fundus image)
├── Encoder blocks with skip connections from input
├── Concatenation at each level
├── Decoder with Conv2DTranspose
├── Batch Normalization + ReLU
└── Output: 256 × 256 × 1 (vessel segmentation mask, Sigmoid)
```

## Training

- **Loss:** Dice Coefficient Loss
- **Metrics:** Dice Coefficient
- **Optimizer:** Adam
- **Dataset:** FIVES (Retina vessel segmentation dataset)
- **Checkpoint:** Best `val_dice_coeff` saved automatically

## Files

```
├── Retina_Vessel_Segmentation.ipynb   # Full training notebook
└── README.md
```

## Publication

**"Retina Vessel Segmentation Using Lightweight U-net Like Model Optimized for Neuromorphic Crossbar Array"**  
IEEE APSCON 2025 — [View Paper](https://ieeexplore.ieee.org/document/11144381)

## Tech Stack

Python · TensorFlow · Keras · OpenCV · Dice Loss · Medical Imaging

## Usage

Run on [Kaggle](https://www.kaggle.com/) with GPU T4:
1. Upload notebook
2. Attach dataset: `retina-segmentation-data` (FIVES)
3. Select GPU T4 accelerator
4. Run All

## Author

**Birva Oza**  
M.Tech in Machine Learning — Dhirubhai Ambani Institute of Information and Communication Technology, Gandhinagar, Gujarat, India

- [Portfolio](https://birvaoza-portfolio.vercel.app)
- [LinkedIn](https://linkedin.com/in/birvaoza01)
