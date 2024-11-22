# PALM-TREE-DETECTION
try the models in this repo to detect palmtrees in you images!!!
# 🌴 Palm Tree Detection Models: PalmNet, YOLOv8, and Faster R-CNN 🌟

Welcome to the **Palm Tree Detection** project! This repository implements and evaluates three state-of-the-art models for detecting palm trees in aerial imagery: **PalmNet**, **YOLOv8**, and **Faster R-CNN**.

---

## 📚 Table of Contents
1. [Introduction](#introduction)
2. [Models Overview](#models-overview)
   - [PalmNet](#palmnet)
   - [YOLOv8](#yolov8)
   - [Faster R-CNN](#faster-r-cnn)
3. [Dataset](#dataset)
4. [Results and Comparison](#results-and-comparison)
5. [How to Use This Repository](#how-to-use-this-repository)
6. [Acknowledgements](#acknowledgements)

---

## 📖 Introduction <a name="introduction"></a>
Palm tree detection is crucial for environmental monitoring, agriculture, and forestry. This project explores different computer vision models to achieve accurate detection using a custom dataset of annotated palm tree images.

---

## 🧠 Models Overview <a name="models-overview"></a>

### 🌟 1. PalmNet: A Hybrid Model <a name="palmnet"></a>
**PalmNet** combines:
- **EfficientNet-B0** as the backbone for feature extraction.
- **BiFPN (Bidirectional Feature Pyramid Network)** and **Path Aggregation Network (PAN)** for feature fusion.
- Loss functions: 
  - **Focal Loss** for classification.
  - **CIoU Loss** for bounding box regression.
- Post-processing: **Soft-NMS** for refined predictions.

> **Pros**:
> - Optimized for aerial imagery.
> - Custom hybrid architecture tailored for palm tree detection.

> **Cons**:
> - Computationally intensive compared to YOLOv8.

---

### ⚡ 2. YOLOv8: Real-Time Object Detection <a name="yolov8"></a>
YOLOv8 is the latest version of the **You Only Look Once (YOLO)** family, known for its speed and efficiency:
- Single-stage detection model.
- Optimized for real-time detection.

> **Pros**:
> - Extremely fast and efficient.
> - Easy to deploy on edge devices.

> **Cons**:
> - Slightly less accurate than multi-stage models like PalmNet and Faster R-CNN.

---

### 🏆 3. Faster R-CNN: A Multi-Stage Detector <a name="faster-r-cnn"></a>
Faster R-CNN is a classic two-stage detection model:
- **Region Proposal Network (RPN)** generates candidate regions.
- Refined predictions using the second stage.

> **Pros**:
> - High accuracy.
> - Robust for complex datasets.

> **Cons**:
> - Slower compared to YOLOv8 and PalmNet.

---

## 🖼️ Dataset <a name="dataset"></a>
The dataset consists of aerial images annotated with palm tree bounding boxes in COCO JSON format. 

**Roboflow Dataset**: [Palm Tree Detection Dataset](https://universe.roboflow.com/nur-byq0f/palm-detection-4qh3m)

| Property        | Value                     |
|------------------|---------------------------|
| **Number of Images** | 1000+                   |
| **Annotation Format** | COCO JSON               |
| **Image Dimensions**  | Variable (resized to 512x512) |
| **Classes**           | Single class (Palm Tree) |

---

## 📊 Results and Comparison <a name="results-and-comparison"></a>
| Model         | Precision | Recall | mAP@0.5 | mAP@0.5:0.95 |
|---------------|-----------|--------|---------|--------------|
| **PalmNet**   | 0.86      | 0.84   | 0.89    | 0.53         |
| **YOLOv8**    | 0.86      | 0.86   | 0.88    | 0.54         |
| **Faster R-CNN** | 0.88   | 0.85   | 0.88    | 0.48         |

![Model Performance Comparison](https://via.placeholder.com/800x400.png?text=Model+Performance+Comparison)

---

## 🚀 How to Use This Repository <a name="how-to-use-this-repository"></a>

### Clone the Repository
```bash
git clone https://github.com/your_username/palm-tree-detection.git
cd palm-tree-detection
