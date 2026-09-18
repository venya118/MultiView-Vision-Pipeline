# MultiView-Vision-Pipeline


# Project Overview
A comprehensive end-to-end Computer Vision pipeline implementing traditional low level processing, 3D spatial reconstruction via stereo or epipolar geometry, classical feature extraction, machine learning classification, and motion tracking.


# Objective of the project
The goal of MultiView-Vision-Pipeline is to build a modular classical computer vision system without relying on heavy deep-learning frameworks. It processes an input pair of stereo images and video frames through a 4-stage pipeline:

Preprocessing: Enhances contrast and removes noise using spatial filters.   

Features & Geometry: Detects scale-invariant keypoints (SIFT) and estimates 3D depth geometry using Epipolar constraints.

Segmentation & Reduction: Clusters image regions via K-Means and simplifies descriptor dimensions using PCA.   

Motion Analysis: Tracks moving objects across frames using Farneback Optical Flow.   


# Project Structure Overview
Separation of Concerns (SoC): Distinct operational stages—such as low-level image processing, multi-camera geometry, pattern analysis, and motion tracking—are isolated in individual source files rather than merged into a single script.

Modularity and Reusability: Grouping functions by domain (e.g., part1_preprocess.py, part2_geometry.py) allows individual modules to be tested, debugged, or imported independently without executing the entire pipeline.   

Maintainability & Scalability: Separating data storage (data/), core algorithms (src/), and top-level execution scripts (main.py) prevents working directories from becoming cluttered as new vision algorithms or datasets are integrated.

Reproducibility: Including environment definitions (requirements.txt) and unified documentation (README.md) ensures that the pipeline can be deployed, rebuilt, and executed consistently across different execution environments.


# Author
Venya Rajput
