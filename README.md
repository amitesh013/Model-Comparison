# 🎯 Bullseye Target Detection: YOLOv8n vs Optimized YOLOv12n

A computer vision project focused on detecting bullseye targets under challenging real-world conditions such as low light, smoke, partial occlusion, and damaged targets. This work presents a comparative analysis between a baseline YOLOv8n model and an optimized YOLOv12n architecture enhanced with custom modules for circular target detection.

## 🚀 Key Features

* 🎯 Accurate bullseye target detection
* 🧠 Custom RSAM (Radial Shape-Aware Module) for circular pattern awareness
* ⚡ Lightweight GhostNetV2 backbone for efficient feature extraction
* 🔄 BiFPN neck for improved multi-scale feature fusion
* 📍 Geometric center detection for precise target localization
* 📈 Improved recall and mAP scores compared to the baseline model
* 🏹 Designed for real-world target detection scenarios

## 📂 Dataset

The dataset was sourced from Roboflow Universe and contains images of bullseye targets captured under varying conditions.

| Split      | Images |
| ---------- | ------ |
| Training   | 1,509  |
| Validation | 168    |
| Test       | 168    |
| Total      | 1,845  |

### Dataset Validation

Before object detection training, a MobileNetV2 classifier was used to validate dataset quality and class separability.

✅ MobileNetV2 Test Accuracy: **95.63%**

## 🏗️ Model Architecture

### YOLOv8n (Baseline)

* CSPDarknet Backbone
* PANet Neck
* CIoU Loss
* 3.0M Parameters
* 8.1 GFLOPs

### YOLOv12n (Optimized)

* GhostNetV2 Backbone
* BiFPN Feature Fusion
* RSAM Attention Module
* SIoU Loss Function
* Geometric Center Detection
* 2.57M Parameters
* 6.3 GFLOPs

## 📊 Performance Comparison

| Metric       | YOLOv8n    | YOLOv12n Optimized |
| ------------ | ---------- | ------------------ |
| mAP@0.5      | 0.8797     | **0.8995**         |
| mAP@0.5:0.95 | 0.7997     | **0.8131**         |
| Precision    | **0.9714** | 0.9426             |
| Recall       | 0.8478     | **0.8929**         |
| Parameters   | 3.0M       | **2.57M**          |
| GFLOPs       | 8.1        | **6.3**            |

## 🏆 Key Achievements

* 📈 +2.3% improvement in mAP@0.5
* 📈 +1.7% improvement in mAP@0.5:0.95
* 🎯 +5.3% improvement in Recall
* ⚡ 14.4% fewer parameters
* 🚀 22.2% reduction in computational cost
* 🧠 83% reduction in backbone parameters using GhostNetV2

## 🛠️ Tech Stack

* Python
* PyTorch
* Ultralytics YOLO
* OpenCV
* NumPy
* Roboflow
* Google Colab

## 🔮 Future Work

* Multi-ring bullseye scoring
* Real-time video tracking using BoT-SORT
* TensorRT/ONNX optimization

