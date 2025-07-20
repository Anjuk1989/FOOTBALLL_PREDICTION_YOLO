# ⚽ YOLOv8 Football Object Detection

A custom object detection project using YOLOv8 to detect key entities in football match videos — including **players**, **goalkeeper**, **referee**, and the **ball** — for real-time analysis and potential use in sports analytics.

---

## 🎯 Project Objective

To train a YOLOv8 model capable of detecting multiple football-specific objects in real-time, enabling insights into player positions, referee movements, and ball tracking.

---

## 🛠️ Tech Stack

- Python 🐍
- [Ultralytics YOLOv8](https://docs.ultralytics.com)
- Google Colab (training environment)
- OpenCV (video processing)
- Roboflow (annotation & dataset management)

---

## 📁 Dataset

- Created using **Roboflow**
- Annotated images with four custom classes:
  - `player`
  - `goalkeeper`
  - `referee`
  - `ball`
- YOLO format with `images/train`, `images/val`, `labels/train`, `labels/val`
- `data.yaml` defines class names and paths

---

## 🚀 Model Training

```bash
!yolo task=detect mode=train model=yolov8l.pt data=data.yaml epochs=10 project=final_results
