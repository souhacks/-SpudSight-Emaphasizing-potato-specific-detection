
# Potato Leaf/Plant Detection using YOLOv5

This project implements a real-time detection system for identifying potato leaves and plants using YOLOv5. The project involves data collection, annotation, model training, and deployment optimized for NVIDIA Jetson Orin.

---

## Table of Contents

- [Objective](#objective)
- [Features](#features)
- [Project Workflow](#project-workflow)
  - [1. Data Collection](#1-data-collection)
  - [2. Data Annotation](#2-data-annotation)
  - [3. Model Training](#3-model-training)
  - [4. Real-time Detection](#4-real-time-detection)
  - [5. Deployment](#5-deployment)
- [Architecture](#architecture)
- [Technologies Used](#technologies-used)
- [Setup Instructions](#setup-instructions)
- [Future Improvements](#future-improvements)

---

## Objective

The goal of this project is to develop a robust and efficient detection model for potato plants and leaves using the YOLOv5 object detection framework and deploy it for real-time use.

---

## Features

- **Efficient Data Collection**: Automated image scraping using BingDownloader.
- **Accurate Data Annotation**: Generated bounding box annotations with labelImg.
- **State-of-the-Art Detection**: Trained using YOLOv5 for high-accuracy detection.
- **Real-time Performance**: Integrated detection pipeline with OpenCV.
- **Hardware Optimization**: Deployed on NVIDIA Jetson Orin for edge computing.

---

## Project Workflow

### 1. Data Collection
- Downloaded thousands of potato leaf/plant images using the BingDownloader library.
- Organized the dataset into `train/` and `test/` folders for training and testing.

### 2. Data Annotation
- Annotated the dataset using **labelImg**, saving bounding box data in `.xml` format.
- Converted the annotations to YOLO format (center x, center y, width, height).

### 3. Model Training
- Trained the YOLOv5 model using annotated data.
- Tested and evaluated model performance using precision, recall, and mAP metrics.
- Generated prediction files for further analysis and refinement.

### 4. Real-time Detection
- Built a real-time detection application using **OpenCV** to process live video feeds or image inputs.
- Visualized bounding boxes and detection scores during inference.

### 5. Deployment
- Deployed the project on **NVIDIA Jetson Orin**, leveraging its GPU for faster inference.
- Uploaded the complete project with documentation and code to GitHub.

---

## Technologies Used

- **Python**: Core programming language.
- **YOLOv5**: Object detection framework.
- **OpenCV**: Real-time computer vision library.
- **BingDownloader**: Automated image scraping tool.
- **labelImg**: Data annotation tool.
- **NVIDIA Jetson Orin**: Edge device for deployment.
- **GitHub**: Version control and project hosting.

---

## Setup Instructions

1. **Clone the Repository**:
   ```bash
   git clone https://github.com/your-username/potato-yolo-detection.git
   cd potato-yolo-detection
   ```

2. **Set Up the Virtual Environment**:
   ```bash
   python -m venv yolov5-env
   source yolov5-env/bin/activate  # For Windows: yolov5-env\Scripts\activate
   ```

3. **Install Dependencies**:
   ```bash
   pip install -r requirements.txt
   ```

4. **Organize the Dataset**:
   - Place images in the `data/train/` and `data/test/` folders.
   - Ensure YOLO annotations are correctly formatted.

5. **Train the Model**:
   ```bash
   python train.py --data data.yaml --cfg yolov5s.yaml --weights yolov5s.pt
   ```

6. **Run Real-time Detection**:
   ```bash
   python detect.py --source 0  # Use webcam as the input source
   ```

7. **Deploy on NVIDIA Jetson Orin**:
   - Transfer the trained weights and scripts to the Jetson device.
   - Install dependencies and run the detection script.

---

## Future Improvements

- Incorporate YOLOv8 for higher detection accuracy.
- Expand dataset with more diverse samples for better generalization.
- Add a user-friendly interface for non-technical users.

---

## License

This project is licensed under the [MIT License](LICENSE).

---

## Acknowledgments

- YOLOv5 by Ultralytics for providing the backbone model.
- NVIDIA Jetson Orin for hardware support.
- OpenCV for real-time detection tools.

---

Feel free to contribute to the project or raise any issues! 😊
