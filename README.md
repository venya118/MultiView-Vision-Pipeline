# MultiView-Vision-Pipeline

# Project Overview
A comprehensive end-to-end Computer Vision pipeline implementing traditional low level processing, 3D spatial reconstruction via stereo or epipolar geometry, classical feature extraction, machine learning classification, and motion tracking.

# Objective of the project
The goal of MultiView-Vision-Pipeline is to build a modular classical computer vision system without relying on heavy deep-learning frameworks. It processes an input pair of stereo images and video frames through a 4-stage pipeline:
Preprocessing: Enhances contrast and removes noise using spatial filters.   
Features & Geometry: Detects scale-invariant keypoints (SIFT) and estimates 3D depth geometry using Epipolar constraints (Fundamental Matrix/RANSAC).
Segmentation & Reduction: Clusters image regions via K-Means and simplifies descriptor dimensions using PCA.   
Motion Analysis: Tracks moving objects across frames using Farneback Optical Flow.   

# Project Structure Overview
MultiView-Vision-Pipeline/
│
├── data/
│   ├── left.png
│   └── right.png
│
├── src/
│   ├── part1_preprocess.py  # Image enhancement & filtering
│   ├── part2_geometry.py    # Epipolar geometry & SIFT
│   ├── part3_pattern.py     # Segmentation & PCA
│   └── part4_motion.py      # Optical flow motion tracking
│
├── main.py                  # Main execution script
├── requirements.txt         # Dependencies
└── README.md                # Documentation

# Author
Venya Rajput
