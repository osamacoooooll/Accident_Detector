# Accident Detection and Prediction

![architecture pipeline](https://github.com/user-attachments/assets/0960b5fc-a3c2-4178-9472-eda3360b9c73)

## Overview
With the growing demand for intelligent transportation systems, this project focuses on accident detection and prediction from video data. By leveraging modern computer vision techniques and deep learning models, the project aims to advance accident analysis, contributing to traffic safety research. This work is crucial for the development of safety-guaranteed autonomous vehicles and accident prevention systems.

## Methodology
The methodology is divided into three key components:

### 1. Accident Prediction Model
The accident prediction model analyzes video footage captured from dash cameras to predict whether an accident is likely to occur in the next frame. Several deep learning architectures were experimented with, including:

- **Swin Video Transformer**
- **ResNet-3D**
- **Mixed Convolutional 3D (MC3)**

Each architecture was evaluated for its ability to capture temporal and spatial patterns indicative of potential accidents. Evaluation metrics included F1 score, recall, and precision. The selected model serves as the initial trigger for decision-making.

### 2. Vehicle Detection Model
The vehicle detection module processes video frames to identify and localize vehicles in the scene. Multiple YOLO models were explored and tested, including:

- **YOLOv7**
- **YOLOv10**
- **YOLOv11**

The best-performing architecture provides detailed predictions, offering critical context for understanding the environment and assessing the severity and nature of potential accidents.

### 3. BART Decoder for Decision-Making
If the accident prediction model detects a potential crash, the post-processed outputs of the detection model, along with encoded video tokens, are passed to the BART decoder. This component generates textual decision outputs describing the appropriate action to take in response to the detected scenario.

**Note:** The BART decoder is planned for future iterations of the project. Due to time and resource constraints, this component was not fully implemented in the current iteration.

## Dataset
The following datasets were utilized:

- **Car Crash Dataset (CCD)**
- **Car Crash Dataset RUSSIA 2022-2023**
- **Car Person Dataset**

These datasets provide comprehensive video and labeling data for training and evaluating the models.

## Models and Architectures
The following models were used and evaluated:

- **EfficientNet**
- **YOLOv3, YOLOv5, YOLOv7, YOLOv10, YOLOv11**
- **Swin3D**
- **ResNet-3D**
- **Mixed Convolutional 3D (MC3)**

## Future Work
- Implementation and evaluation of text decoder architectures such as the BART decoder.
- Optimization of current models to improve accuracy and performance.
- Integration of the system into real-time intelligent transportation systems.

## Contributing
Contributions to improve the models and expand the functionality are welcome! Please open an issue or submit a pull request with your ideas and updates.

## License
This project is licensed under the MIT License. See the `LICENSE` file for details.

---

Thank you for exploring this project! For any questions or feedback, feel free to open an issue or contact the project maintainer.

