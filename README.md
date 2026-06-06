# Vessel Detection and Tracking System

## Overview

This project focuses on real-time vessel detection and tracking for maritime surveillance using state-of-the-art Computer Vision and Deep Learning techniques. The system detects marine objects such as ships, boats, and other watercraft from video streams and tracks them across frames using unique IDs.

The project aims to support maritime security, automated monitoring, search-and-rescue operations, and reduce dependence on manual surveillance systems.

---

## Project Status

🚧 **Work in Progress**

### Completed

* Dataset Collection and Analysis
* Data Preprocessing
* YOLO Dataset Preparation
* Custom YOLOv12 Model Training
* Vessel Detection Pipeline
* Initial ByteTrack Integration
* Model Evaluation

### Upcoming Features

* Vessel Re-Identification
* Anomaly Detection
* Trajectory Analysis
* Real-Time Dashboard
* Performance Optimization
* Deployment Pipeline

---

## Features

* Real-time vessel detection using YOLOv12
* Multi-object tracking using ByteTrack
* Unique ID assignment for each detected vessel
* Bounding box visualization
* Coordinate extraction for detected vessels
* Maritime surveillance support
* Scalable architecture for future anomaly detection

---

## Dataset

The model was trained on maritime datasets containing multiple classes of marine objects including:

* Ships
* Boats
* Watercraft
* Marine Vehicles

The datasets were cleaned, merged, and converted into YOLO format for training.

> Note: Due to dataset size and licensing constraints, the complete dataset is not included in this repository.

---

## Technologies Used

* Python
* YOLOv12
* OpenCV
* ByteTrack
* NumPy
* Pandas
* Google Colab
* Git & GitHub

---

## System Architecture

```text
Input Video
     │
     ▼
YOLOv12 Detection
     │
     ▼
Bounding Boxes
     │
     ▼
ByteTrack Tracking
     │
     ▼
Object ID Assignment
     │
     ▼
Trajectory Generation
     │
     ▼
Maritime Surveillance Output
```

## Model Training

* Prepared custom maritime datasets in YOLO format.
* Applied preprocessing and annotation verification.
* Trained YOLOv12 model on custom vessel datasets.
* Evaluated model performance using standard object detection metrics.
* Optimized training parameters for improved detection performance.

---

## Results

The model was evaluated using standard object detection metrics:

* Precision
* Recall
* mAP (Mean Average Precision)
* F1 Score

Training and evaluation results demonstrated strong vessel detection performance under varying environmental conditions.

---

## Repository Structure

```text
Vessel-Detection-and-Tracking/
│
├── README.md
├── vessel_detection.ipynb
├── requirements.txt
│
├── images/
│   ├── sample_predictions/
│   └── tracking_outputs/
│
└── results/
    ├── confusion_matrix.png
    ├── PR_curve.png
    └── results.png
```

## Installation

```bash
git clone <repository-link>
cd Vessel-Detection-and-Tracking
pip install -r requirements.txt
```

## Usage

Open the notebook and run:

```bash
vessel_detection.ipynb
```

using Google Colab or Jupyter Notebook.

---

## Future Scope

* Vessel Re-Identification
* Maritime Anomaly Detection
* Illegal Activity Detection
* Collision Risk Analysis
* Smart Port Monitoring
* Coast Guard Surveillance Support
* Real-Time Deployment

---

## Author

**Uttam Rathore**

B.Tech Electronics & Communication Engineering
MNIT Jaipur

Interested in Machine Learning, Computer Vision, Deep Learning, and AI-powered surveillance systems.

---

## License

This project is released under the MIT License.
