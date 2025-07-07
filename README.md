# Sheep Classification Images 🐑

This repository contains my solution for the **Kaggle Sheep Classification Challenge 2025**, where the goal is to classify images of sheep based on their breed and other visual characteristics.

## Background 🧠

The sheep industry plays an important role in global agriculture, and accurate classification of sheep breeds and features (such as wool type, color, and size) is essential for herd management, breeding, health tracking, and market prediction. 
With the advancement of machine learning and computer vision, automating the process of sheep classification has become more feasible and efficient. This competition simulates a real-world livestock classification task, where participants must build image classifiers capable of recognizing different sheep attributes from raw image data.

## Objective 🎯 

To build a robust deep learning model that classifies sheep images into the correct categories, improving the accuracy and efficiency of sheep management in practical agricultural contexts.

---

## 📂 Dataset Overview

The dataset provided by the competition includes:

- `train/`: A folder containing labeled sheep images for training.
- `test/`: A folder with unlabeled sheep images for final evaluation.
- `train.csv`: Metadata and labels for each training image.
- `sample_submission.csv`: Template for Kaggle submission.

### 🖼️ Input:
- RGB images of sheep from various angles and lighting conditions.

### 🏷️ Target:
- Multi-class label indicating the sheep's breed or classification group.

---

## 🧪 Approach

1. **Data Preprocessing**
   - Image resizing and normalization
   - Data augmentation (horizontal flip, rotation, brightness, etc.)
   - Stratified split for validation

2. **Modeling**
   - Used transfer learning with pretrained CNN architectures:
     - ResNet50
     - EfficientNetB3
     - ConvNeXt
   - Fine-tuned using cross-entropy loss
   - Implemented early stopping, learning rate scheduling, and mixed-precision training

3. **Ensembling**
   - Averaged predictions from multiple models for better generalization

4. **Evaluation**
   - Main metric: Accuracy
   - Evaluated both on public and private leaderboard via Kaggle submission

---

## 📊 Results

| Model           | Public Score | Private Score |
|----------------|--------------|---------------|
| Ensemble (Best) | **0.69616**  | **0.86996**   |

✅ The final submission achieved a **private leaderboard accuracy of 86.996%**, showing strong generalization and robustness on the hidden test set.

---
