# Problem Statement
Identifying archaeological mounds using traditional methods such as field surveys and manual analysis of LiDAR data is time-consuming and often constrained by physical and geographical factors. While LiDAR data and Digital Elevation Models (DEMs) have been used in the past, they present challenges such as a high false positive rate and difficulty distinguishing between mounds and man-made structures.

# Proposed Solution
We developed a machine learning-based solution using Digital Terrain Model (DTM) data, which eliminates buildings and other structures to reduce false positives. By leveraging the YOLO (You Only Look Once) object detection framework, combined with transfer learning and data augmentation, the solution aims to efficiently and accurately identify archaeological mounds from DTM imagery.

# Results Achieved
Precision: 57.3% of the detected objects were true positives.

Recall: 55.9% of actual mounds were successfully identified.

The balance between precision and recall indicates robust performance in identifying and detecting mounds.

Metrics such as training and validation loss, as well as precision and recall scores, showed consistent improvement throughout training.

# Tech Stack
   # Tools and Platforms:
Quantum Geographic Information System (QGIS): Used for preprocessing DTM data and applying the hillshade function.

LabelImg: For image annotation and labeling.

# Frameworks and Libraries:
YOLOv5: The primary model used for object detection.

OpenCV (cv2): Used for image processing during the prediction phase.

Python: For scripting, model development, and data manipulation.

Pandas, NumPy: Libraries for data handling and manipulation.

# Model Training:
YOLOv5s.yaml: Configuration for the YOLOv5 model architecture.

Stochastic Gradient Descent (SGD): Optimizer with a learning rate of 0.01 for training.

Data Augmentation: Techniques such as image rotation, blur, grayscale conversion, and CLAHE were applied to enhance the model’s generalization ability.

# Future Enhancements
Dataset Expansion: Increase the number of samples using Generative Adversarial Networks (GANs) to improve model performance.

Statewide Predictions: Scale the model to predict mounds across the entire state of Indiana.

Probability Mapping: Generate a probability map to provide confidence levels for predictions at each location.

# Conclusion
By integrating machine learning with DTM data, the proposed solution significantly reduces the time and effort required for mound detection. Future improvements to the model and dataset are expected to further enhance accuracy, potentially contributing to large-scale archaeological research and heritage management in Indiana.
