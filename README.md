# Multi-Object Apparel Detection and Instance Segmentation

An end-to-end fashion visual recognition system built on the DeepFashion2 dataset for apparel classification, object detection, and instance segmentation. The project explores transfer learning and training-from-scratch approaches across multiple deep learning architectures and compares their effectiveness on real-world fashion images.

## Overview

Fashion e-commerce platforms require automated systems capable of understanding clothing items within images. This project addresses three key computer vision tasks:

- Multi-label Apparel Classification
- Clothing Object Detection
- Instance Segmentation
- Model Explainability through Feature Map Visualization

The system is trained and evaluated on the DeepFashion2 dataset, focusing on the five most frequent apparel categories.

## Dataset

### DeepFashion2

Selected Categories:

- Short Sleeve Top
- Long Sleeve Top
- Trousers
- Shorts
- Skirt

Dataset preprocessing included:

- Category filtering
- Annotation pruning
- Stratified train-validation split
- Class imbalance handling
- Data augmentation

## Features

### Classification

Implemented and compared:

- EfficientNet-B2
- ResNet50
- MobileNetV3
- Transfer Learning vs Training From Scratch
- TensorFlow and PyTorch implementations

### Detection

- Bounding box localization of clothing items
- Multi-object recognition

### Segmentation

- Pixel-level garment segmentation
- Instance-aware clothing extraction

### Explainability

- Intermediate feature map visualization
- Activation heatmaps
- Error analysis and failure case inspection

## Data Augmentation

Training images were augmented using:

- Horizontal Flip
- Rotation
- Brightness Adjustment
- Contrast Adjustment
- Zoom Transformations

## Model Training

### Transfer Learning

- ImageNet pretrained backbones
- Frozen backbone warm-up
- Gradual fine-tuning
- Differential learning rates
- Early stopping
- Learning rate scheduling

### Training From Scratch

- Random weight initialization
- Full-network optimization
- Comparative performance benchmarking

## Best Performing Model

### ResNet50 (PyTorch Transfer Learning)

| Metric | Score |
|----------|---------|
| Macro F1 | 0.8511 |
| Micro F1 | 0.8639 |
| Macro Precision | 0.8072 |
| Micro Precision | 0.8263 |
| Macro Recall | 0.9030 |
| Micro Recall | 0.9050 |
| Macro ROC-AUC | 0.9669 |

## Tech Stack

### Frameworks

- PyTorch
- TensorFlow / Keras

### Computer Vision

- OpenCV
- DeepFashion2

### Deep Learning Models

- EfficientNet-B2
- ResNet50
- MobileNetV3

### Utilities

- NumPy
- Pandas
- Matplotlib
- Scikit-Learn

## Results

Key findings:

- Transfer learning consistently outperformed training from scratch.
- ResNet50 Transfer Learning achieved the best overall performance.
- Class weighting significantly improved minority class recall.
- Feature visualization confirmed meaningful garment-focused attention maps.
- Deep residual architectures generalized better on fashion-specific tasks.

## Future Improvements

- Expand to all DeepFashion2 categories.
- Deploy as a web application.
- Integrate real-time fashion retrieval.
- Add attribute prediction (color, sleeve type, style).
- Experiment with Vision Transformers (ViT).
