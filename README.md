# ComputerVision-Assignment
# Feature Detection and Corner Detection

## Overview
This project implements **feature detection** and **corner detection** algorithms, including **SIFT feature matching**, **Harris corner detection**, and **Shi-Tomasi corner detection**. The goal is to analyze how different parameter values affect feature detection accuracy and precision.

## Implemented Techniques
### 1. SIFT Feature Matching
- **Description:** Detects and matches key points between images using Scale-Invariant Feature Transform (SIFT).
- **Parameters Tuned:**
  - **Initial Ratio Threshold:** 0.75 → **Changed to:** 0.80
  - **Observation:**
    - Increasing the ratio threshold resulted in more matches but also introduced false matches.
    - Lowering it to 0.70 reduced false matches but also missed valid key points.

### 2. Harris Corner Detection
- **Description:** Detects corners in an image using eigenvalues of gradient matrices.
- **Parameters Tuned:**
  - **Initial Sensitivity Factor (k):** 0.04 → **Changed to:** 0.05
  - **Observation:**
    - Increasing the sensitivity factor detected fewer corners, missing some edges.
    - Reducing it to 0.03 detected more corners but introduced noise.
  - **Initial Block Size:** 3 → **Changed to:** 4
  - **Observation:**
    - Larger block size detected more robust corners but missed finer details.
    - Reducing it to 2 detected more corners but increased noise.

### 3. Shi-Tomasi Corner Detection
- **Description:** Identifies and tracks good feature points in an image.
- **Parameters Tuned:**
  - **Initial Quality Level:** 0.01 → **Changed to:** 0.015
  - **Observation:**
    - Increasing the quality level reduced the number of detected corners, keeping only the strongest ones.
    - Lowering it to 0.005 detected more corners but included false detections.
  - **Initial Minimum Distance:** 10 → **Changed to:** 8
  - **Observation:**
    - Reducing the minimum distance resulted in more clustered corner detections, leading to redundancy.
    - Increasing it to 12 spaced out the detected corners but missed some key points.
