# 🚢 Maritime Anomaly Detection using YOLOv12

An AI-powered maritime surveillance system that detects ships, boats, and other maritime objects while identifying windsurfers and SUP boards as anomalous objects. The project uses a custom-trained YOLOv12 model to automate maritime monitoring from images and videos, helping improve safety, security, and situational awareness.

---

## 📌 Overview

Maritime surveillance often requires continuous human monitoring, which is time-consuming and prone to errors. This project automates the detection of maritime objects and highlights potentially unusual objects separately, reducing manual effort and enabling faster decision-making.

---

## 🎯 Problem Statement

The system addresses the following challenges:

- Automated detection of ships and boats
- Identification of small or unusual maritime objects
- Reduced dependence on manual video monitoring
- Improved maritime safety and surveillance
- Faster analysis of maritime imagery and videos

---

## ⚙️ Features

- 🚢 Maritime vessel detection
- ⚠️ Anomaly detection for Wind/SUP Boards
- 🎥 Video processing and inference
- 🖼️ Image inference and visualization
- 📊 Custom YOLOv12 training pipeline
- 🔴 Red bounding boxes for anomalies
- 🟢 Green bounding boxes for normal objects

---

## 🏗️ System Pipeline

```text
Input Image/Video
        ↓
YOLOv12 Object Detection
        ↓
Object Classification
        ↓
Anomaly Check
(Wind/SUP Board?)
      /    \
    Yes     No
     ↓       ↓
 Red Box  Green Box
        ↓
 Annotated Output
```

---

## 🧠 Model Details

| Parameter | Value |
|------------|--------|
| Model | YOLOv12s |
| Epochs | 13 |
| Image Size | 640 × 640 |
| Batch Size | 16 |
| Framework | Ultralytics YOLO |

The model is trained on a custom maritime dataset containing ships, boats, vessels, and wind/SUP boards.

---

## 🚀 Usage

### Training

```python
from ultralytics import YOLO

model = YOLO("yolo12s.pt")

model.train(
    data="data.yaml",
    epochs=13,
    imgsz=640,
    batch=16
)
```

### Image Inference

```python
from ultralytics import YOLO

model = YOLO("best.pt")
results = model("image.jpg")
results[0].show()
```

### Video Inference

```python
from ultralytics import YOLO

model = YOLO("best.pt")

model.predict(
    source="video.mp4",
    save=True
)
```

---

## 🛠️ Technologies Used

- Python
- YOLOv12 (Ultralytics)
- OpenCV
- NumPy
- Matplotlib
- Google Colab

---

## 🔮 Future Improvements

- Multi-object tracking using ByteTrack
- Vessel Re-Identification (ReID)
- DINOv2-based feature embeddings
- Motion and stillness analysis
- Advanced anomaly detection
- Search and rescue intelligence systems

---

## 👨‍💻 Author

**Uttam Rathore**  
B.Tech, Electronics & Communication Engineering  
MNIT Jaipur

---

⭐ If you find this project useful, consider giving it a star on GitHub.
