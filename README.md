Here is a clean README.md content (~200 words) ready to paste into GitHub:

YOLOv26 Optimization with Slicing-Aided Hyper Inference (SAHI)

This repository contains the official implementation of our paper:

“YOLO26 Optimization with Slicing-Aided Hyper Inference for Small-Object Detection and Segmentation in Complex Green Fruit Environments.”

📌 Overview

Small-object detection in natural environments remains challenging, particularly under green-on-green camouflage where targets occupy few pixels and exhibit low contrast. This study presents the first implementation and optimization of YOLOv26 on a custom real-world orchard dataset, focusing on fine-grained anatomical segmentation of:

Calyx

Fruitlet

Peduncle (smallest and most challenging class)

We apply Slicing-Aided Hyper Inference (SAHI) as an inference-stage enhancement without modifying the core network architecture.

🚀 Key Results

Overall detection mAP@50:95 improved from 0.363 → 0.414

Overall mask mAP@50:95 improved from 0.335 → 0.384

Peduncle recall improved by 31.74%

Mask mAP@50:95 improved by 30.85%

Nano, small, and medium models retain near real-time feasibility.

📂 Repository Contents

Training scripts

SAHI inference pipeline

Pretrained YOLOv26 models

Dataset configuration files

Evaluation scripts

📖 Citation 
Updating Soon
