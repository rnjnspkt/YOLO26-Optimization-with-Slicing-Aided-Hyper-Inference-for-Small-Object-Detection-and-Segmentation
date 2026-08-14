# Comparing and Optimizing YOLOv8, YOLOv11, and YOLOv26 for Small-Object Detection and Segmentation in Orchards

This repository contains the official implementation, training configurations, and experimental resources associated with our paper:

**“Comparing and Optimizing Ultralytics YOLOv8, YOLOv11, and YOLOv26 for Small-Object Detection and Segmentation in Orchards.”**

<img width="6350" height="15748" alt="jpegarchs" src="https://github.com/user-attachments/assets/22d20123-4c47-44e8-9735-f3956cc998f7" />

**Figure: Cross-generation experimental framework for comparing and optimizing YOLOv8, YOLOv11, and YOLOv26 for fine-grained small-object detection and instance segmentation.**

## 📌 Overview

Small-object detection and instance segmentation remain challenging in complex natural environments, particularly when target objects occupy only a small number of pixels, exhibit low foreground–background contrast, and are affected by occlusion and dense spatial clustering.

This study presents a comprehensive cross-generation evaluation of three Ultralytics YOLO families:

- **YOLOv8**
- **YOLOv11**
- **YOLOv26**

For each YOLO generation, five segmentation model scales are investigated:

- Nano (**n**)
- Small (**s**)
- Medium (**m**)
- Large (**l**)
- Extra-large (**x**)

This results in **15 architecture–scale combinations** evaluated using the same real-world orchard dataset and experimental framework.

The study focuses on fine-grained detection and instance segmentation of three early-stage apple fruitlet anatomical structures:

- **Calyx**
- **Fruitlet**
- **Peduncle**

Among these classes, the peduncle represents a particularly challenging small-object perception problem because of its thin geometry, limited pixel footprint, partial occlusion, and visual similarity to surrounding stems and vegetation.
<img width="1681" height="935" alt="ChatGPT Image Aug 13, 2026, 07_17_29 PM" src="https://github.com/user-attachments/assets/3b443048-c1d5-4aff-8c74-b8120a72b6dd" />


**Figure: Early-stage green apple fruitlets and their anatomical structures under complex green-on-green orchard conditions.**

## 🔬 Experimental Design

Each YOLO generation and model scale is investigated using two complementary training configurations.

### 1. Conventional Training

The conventional configuration uses an input resolution of:

**640 × 640 pixels**

This configuration provides the standardized baseline for evaluating cross-generation and scale-dependent performance.

### 2. Small-Object-Focused Optimization

A second configuration uses:

**960 × 960 pixels**

The higher input resolution is designed to preserve greater spatial information for small and fine anatomical structures during model training. Additional training controls, including scale and mosaic augmentation settings, are used to support small-object learning.

The experimental design therefore enables systematic analysis of the interaction among:

**YOLO Generation × Model Scale × Training Strategy**

This framework allows us to determine whether small-object-focused optimization provides consistent benefits across different YOLO generations and computational capacities.

## 🚀 Evaluation

The trained models are evaluated using detection, instance-segmentation, and computational-efficiency measures, including:

- Precision
- Recall
- F1-score
- Box mAP@50
- Box mAP@50:95
- Mask mAP@50
- Mask mAP@50:95
- Number of layers
- Model parameters
- GFLOPs
- Model size
- Preprocessing time
- Inference time
- Postprocessing time
- Training duration
- Training convergence behavior

Class-wise performance is additionally evaluated for **calyx, fruitlet, and peduncle** to determine how model generation, capacity, and training resolution influence anatomical structures with substantially different spatial characteristics.

## 🎯 Research Questions

The experimental framework is designed to answer four principal questions:

1. How do **YOLOv8, YOLOv11, and YOLOv26** compare for fine-grained small-object detection and instance segmentation under identical orchard conditions?

2. How does increasing model capacity from **nano to extra-large** influence detection accuracy, segmentation quality, and computational requirements?

3. Does **960 × 960 small-object-focused training** improve the perception of small anatomical structures compared with conventional **640 × 640 training**?

4. Which combination of **YOLO generation, model scale, and training strategy** provides the most favorable accuracy–efficiency trade-off for robotic orchard perception?

## 🌱 Application to Robotic Fruit Thinning

The dataset represents a challenging perception problem encountered during early-stage green fruit development.

Unlike conventional orchard-vision studies that primarily detect complete fruits, this work investigates anatomical-level perception of the **fruitlet, calyx, and peduncle**.

Accurate recognition of these structures is particularly relevant to robotic fruit thinning and selective manipulation, where understanding fruit attachment anatomy can provide more actionable information than whole-fruit localization alone.

The green-on-green orchard environment also provides a representative benchmark for broader small-object vision problems involving:

- Low foreground–background contrast
- Small pixel footprints
- Dense object clustering
- Partial occlusion
- Fine or elongated structures
- Complex natural backgrounds

## 📂 Repository Contents

This repository provides resources for reproducing the cross-generation experiments, including:

- YOLOv8-seg training scripts
- YOLOv11-seg training scripts
- YOLOv26-seg training scripts
- Conventional 640 × 640 training configurations
- Small-object-focused 960 × 960 training configurations
- Dataset configuration files
- Model evaluation scripts
- Training and validation outputs
- Selected trained model checkpoints
- Cross-generation performance comparisons

## 🧠 Model Configurations

A total of **15 YOLO architecture–scale combinations** are investigated:

| Generation | Model Variants |
|---|---|
| YOLOv8 | YOLOv8n, YOLOv8s, YOLOv8m, YOLOv8l, YOLOv8x |
| YOLOv11 | YOLOv11n, YOLOv11s, YOLOv11m, YOLOv11l, YOLOv11x |
| YOLOv26 | YOLOv26n, YOLOv26s, YOLOv26m, YOLOv26l, YOLOv26x |

Each architecture–scale combination is investigated under the conventional and small-object-focused training configurations.

## 📖 Citation

Citation information will be added following publication of the associated manuscript.

**Status:** Manuscript under revision.
