# Problem Statement
Identifying archaeological mounds using traditional methods such as field surveys and manual analysis of LiDAR data is time-consuming and often constrained by physical and geographical factors. While LiDAR data and Digital Elevation Models (DEMs) have been used in the past, they present challenges such as a high false positive rate and difficulty distinguishing between mounds and man-made structures.

# Proposed Solution
We developed a machine learning-based solution using Digital Terrain Model (DTM) data, which eliminates buildings and other structures to reduce false positives. By leveraging the YOLO (You Only Look Once) object detection framework, combined with transfer learning and data augmentation, the solution aims to efficiently and accurately identify archaeological mounds from DTM imagery.

# Results Achieved
- **Precision**: 57.3% of detected objects were true positives.
- **Recall**: 55.9% of actual mounds were successfully identified.
- Balanced precision and recall indicate good detection accuracy.
- Consistent reduction in training and validation loss throughout model training.

# Tech Stack

## Tools and Platforms:
- **Quantum Geographic Information System (QGIS)**: Preprocessing DTM data, applying hillshade function.
- **LabelImg**: Annotating and labeling images.

## Frameworks and Libraries:
- **YOLOv5**: Object detection framework.
- **OpenCV (cv2)**: Image processing library for prediction.
- **Python**: Used for scripting and model development.
- **Pandas, NumPy**: For data handling and manipulation.

## Model Training:
- **YOLOv5s.yaml**: Configuration for YOLOv5 architecture.
- **Stochastic Gradient Descent (SGD)**: Optimizer with a learning rate of 0.01.
- **Data Augmentation**: Techniques such as image rotation, blur, grayscale conversion, and CLAHE applied.
 
# Future Enhancements
- **Dataset Expansion**: Implement GANs to increase dataset size.
- **Statewide Predictions**: Deploy the model across all of Indiana.
- **Probability Mapping**: Generate confidence maps for mound predictions.

# Conclusion
By integrating machine learning with DTM data, the proposed solution significantly reduces the time and effort required for mound detection. Future improvements to the model and dataset are expected to further enhance accuracy, potentially contributing to large-scale archaeological research and heritage management in Indiana.
