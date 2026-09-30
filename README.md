# SeaDronesSee
DAY-1
#Research Paper:
1. SeaDronesSee: A Maritime Benchmark for Detecting Humans in Open Water
L. A. Varga, B. Kiefer, M. Messmer, A. Zell. IEEE/CVF WACV 2022 (a conference paper, but it is the only source for the dataset).
Link: https://openaccess.thecvf.com/content/WACV2022/html/Varga_SeaDronesSee_A_Maritime_Benchmark_for_Detecting_Humans_in_Open_Water_WACV_2022_paper.html
What we take: the dataset itself, meaning its classes, image splits, annotation format and altitude and camera-angle metadata. We also take the benchmark evaluation setup and the argument that land-based detectors need maritime UAV training data.

2. YoloOW: A Spatial Scale Adaptive Real-Time Object Detection Neural Network for Open Water Search and Rescue From UAV Aerial Imagery
J. Xu, X. Fan, H. Jian, C. Xu, W. Bei, Q. Ge, T. Zhao. IEEE Transactions on Geoscience and Remote Sensing, 2024.
Link: https://ieeexplore.ieee.org/document/10517350/
What we take: the state-of-the-art result to compare our detector against, and the reasoning that fixed-scale features miss objects of very different sizes in open-water UAV images. Its reliance on large input sizes supports our resolution and tiling experiments.

3. Optimizing Drone-Captured Maritime Rescue Image Object Detection Through Dataset Rebalancing Under Sample Constraints
B. Zhao, J. Li, J. Zhao, L. Yu, X. Zhang, J. Liu. The Visual Computer, vol. 41, no. 13, 2025 (Springer).
Link: https://doi.org/10.1007/s00371-025-04098-y
What we take: evidence that SeaDronesSee has class imbalance and uneven train/validation splits, which justifies our dev-split protocol and class-balanced tile sampling. It also tells us to report per-class results carefully and to consider a rebalanced split as an extra sensitivity check.

4. Modular YOLOv8 Optimization for Real-Time UAV Maritime Rescue Object Detection
B. Zhao, Y. Zhou, R. Song, L. Yu, X. Zhang, J. Liu. Scientific Reports, vol. 14, art. 24492, 2024 (Springer Nature).
Link: https://doi.org/10.1038/s41598-024-75807-1
What we take: a SeaDronesSee analysis of dataset bias and rare classes, and its reporting style (overall AP50-95, per-class AP50, speed). We also take the idea of adding a stride-4 (P2) feature level for small objects. It uses the original six-class version, so we don't compare its numbers directly with our v2 results.

5. ESOD: Efficient Small Object Detection on High-Resolution Images
K. Liu, Z. Fu, S. Jin, Z. Chen, F. Zhou, R. Jiang, Y. Chen, J. Ye. IEEE Transactions on Image Processing, vol. 34, 2025.
Link: https://doi.org/10.1109/TIP.2024.3501853
What we take: the justification for processing large images as patches instead of shrinking them, which is the core of our tiling experiments. We also take the idea of spending computation only on regions likely to contain objects, and a conceptual comparison to SAHI.   
