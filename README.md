# RANSAC-based Image Stitching

## Description

This project implements **image stitching using RANSAC-based affine and homography transformations** to create panoramas. The objective is to construct wide-angle images by **aligning and blending multiple images with overlapping fields of view** while ensuring robust feature matching and transformation estimation.

## Features

- **Affine Transformation-based Stitching** (Part A)
- **Homography Transformation-based Stitching** (Part B)
- **SIFT Keypoint Detection and Feature Matching**
- **RANSAC-based Robust Transformation Estimation**
- **Mosaic Creation and Image Warping**
- **Least-Squares Optimization for Final Transformation**

## Technologies Used

- **Python**
- **NumPy**
- **Matplotlib**
- **Torch**
- **Kornia**
- **OpenCV**
- **SciPy**
- **Scikit-Image**

## Installation

```bash
pip install numpy matplotlib torch kornia opencv-python scipy scikit-image
```

## Project Tasks

### **Part A: Affine Transformation-Based Stitching**

1. **Preprocess Images:** Convert to grayscale.
2. **Detect Keypoints & Extract Descriptors:** Use **SIFT** to find image features.
3. **Feature Matching:** Compute **Euclidean distances** between feature descriptors.
4. **Prune Matches:** Select the best matches based on a distance threshold.
5. **Estimate Affine Transformation using RANSAC:** Identify the best transformation model.
6. **Compute Optimal Transformation:** Use **least-squares refinement**.
7. **Generate the Panorama:** Warp images and blend them into a mosaic.

### **Part B: Homography-Based Stitching**

1. **Preprocess Images:** Convert to grayscale.

2. **Detect Keypoints & Extract Descriptors:** Use **SIFT** to find image features.

3. **Feature Matching:** Compute **Euclidean distances** between feature descriptors.

4. **Prune Matches:** Select the best matches based on a distance threshold.

5. **Estimate Homography Transformation using RANSAC:** Identify the best transformation model with a minimum of four correspondences.

6. **Solve the Homogeneous System using SVD:** Use **Singular Value Decomposition (SVD)** to compute the transformation matrix.

7. **Generate the Panorama:** Warp images and blend them into a mosaic.

8. **Test on a Custom Image Set** and visualize the stitched result.

## Visualizations

- **SIFT Keypoints & Matches:** Display detected keypoints and feature correspondences.
- **Inlier vs. Outlier Matches:** Show RANSAC-selected matches.
- **Warped Images & Final Panorama:** Compare input images and the final stitched mosaic.

