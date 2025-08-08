# 🧬 A Comparative Study of Cellular Automata and Alternative Algorithms in Medical Imaging

This repository contains the implementation, analysis, and comparison of cellular automata (CA)-based algorithms and enhanced image processing techniques for breast cancer detection through mammogram analysis.

📄 [**Read the full paper here**](./Final%20Paper%20(Saruultugs%20and%20Kushal).pdf)

---

## Overview

This study replicates the 2007 CA-based medical image processing method by Wongthanavasu and Tangvoraphonkchai and compares it against a new tumor detection pipeline using modern techniques like CLAHE, median filtering, adaptive thresholding, and Canny edge detection.

The goal is to enhance both image quality and computational performance for more accurate tumor detection in mammographic images.

---

## ⚙ Methods

### Cellular Automata (CA)-Based Method (Replicated)

1. **Gray-Level Edge Detection**: Enhances pixel intensity differences using CA rules.
2. **Binary Edge Detection**: Thresholds the grayscale edge map to isolate edges.
3. **Noise Filtering**: Removes high-frequency noise using CA filtering.
4. **Spot Detection**: Identifies white spots indicative of tumors via edge subtraction and thresholding.

### Enhanced Detection Pipeline (Proposed)

1. **Preprocessing**:
   - Grayscale conversion
   - Artificial salt-and-pepper noise addition
   - Median filtering for denoising
   - CLAHE (Contrast Limited Adaptive Histogram Equalization)

2. **Segmentation**:
   - Adaptive thresholding
   - Canny edge detection

3. **Tumor Region Identification**:
   - Intensity-based region isolation
   - Connected component analysis
   - Region filtering based on size thresholds

---

## 🖼Results

### CA Method
- Effective in structural edge detection.
- Struggles with subtle intensity variations (e.g. benign tumors).
- Limited robustness under real-world noise.

### Proposed Pipeline
- Robust noise handling with CLAHE and filtering.
- Successfully detects both malignant and benign tumors.
- Enhanced segmentation accuracy and region labeling.

> 🧪 See `figures/` or the [paper](./Final%20Paper%20(Saruultugs%20and%20Kushal).pdf) for visual comparisons.

---

## 📊 Evaluation

| Metric | CA-Based Method | Proposed Method |
|--------|------------------|-----------------|
| Tumor Detection Accuracy | Low for subtle tumors | High |
| Noise Robustness | Weak | Strong |
| Image Clarity | Moderate | Improved |
| Segmentation | Basic | Advanced |

