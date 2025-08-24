# DeepCLSMOTE_LOSS

Project Future Extensions
This document outlines the planned extensions and improvements for this project, focusing on enhancing model performance and applicability, with the goal of submitting the work to PAKDD 2026.

1. Deep Learning Model Enhancements
1.1 Update the Loss Function
We plan to explore and integrate advanced loss functions to improve the learning process, specifically focusing on Contrastive Learning. The goal is to better separate minority classes from majority classes in the feature space.

Current Loss Function (Proposed):

Goal: Minimize the reconstruction error and the distance between instances and their corresponding class centroids.

Proposed Formula:

ข้อมูลโค้ด

$Minimize\ Loss = MSE(x, x_i) + MSE(c_i, c_{i}^{main}) + MSE^{-1}(c_i, c_j)$
Future Loss Functions (Extensions):

Self-Contrastive Learning Loss:

Goal: Minimize the distance of an instance to its positive centroid while maximizing its distance from other centroids.

Proposed Formula:

ข้อมูลโค้ด

$Minimize\ Loss = MSE(x, x_i) + NT-XentLoss(c_i, c_{i}^{main})$
Note: NT-Xent Loss refers to Normalized Temperature-Scaled Cross-Entropy Loss.

Supervised Contrastive Learning Loss:

Goal: Maximize the agreement between positive pairs (instances from the same class) and minimize the agreement between negative pairs (instances from different classes).

Proposed Formula:

ข้อมูลโค้ด

$Minimize\ Loss = MSE(x, x_i) + SupConLoss(c_i, c_{i}^{main})$
1.2 Explore Advanced Deep Learning Models
We will investigate the use of cutting-edge deep learning architectures to improve feature extraction and model performance:

Vision Transformer (ViT): Utilizing ViT to capture long-range dependencies in image data, which can be beneficial for complex feature representation.

Mamba: Exploring the Mamba architecture as a potential alternative, known for its efficiency and strong performance in sequence modeling, which can be adapted for image classification.

1.3 Application to Medical Image Benchmark Datasets
To validate the model's effectiveness in real-world scenarios, we will apply the proposed extensions to several medical image benchmark datasets, which are often highly imbalanced:

Breast Cancer Images

Brain Tumor Images

Lung Cancer Images

1.4 Refine DeepCLSMOTE with Multi-Centroids
We will enhance the DeepCLSMOTE algorithm by using multiple centroids for each class. This approach aims to better represent the diversity within each class, especially for complex or multi-modal data distributions, leading to more accurate synthetic data generation.

Submission Plan
We are planning to submit the extended work to the PAKDD 2026 conference. For more information, please visit the official conference website: https://www.pakdd2026.org.
