# Drowning-detection-using-yolov11
Drowning detection using yolov11
Here’s a well-structured and professional `README.md` for your **Drowning Detection using YOLO** project, suitable for a GitHub repository:

---

 Drowning Detection Using YOLOv8

This project implements a real-time drowning detection system using the YOLOv8 (You Only Look Once) object detection algorithm. The model is trained to identify signs of potential drowning in surveillance footage, such as erratic movements, abnormal body posture, and prolonged submersion. The goal is to provide an automated safety solution that can alert lifeguards or emergency systems in swimming pools, beaches, and other water bodies.

 🔍 Project Overview

Drowning is often a silent event, making it difficult to detect with the naked eye, especially in crowded or large water areas. This project uses computer vision and deep learning to monitor individuals in real-time video feeds and raise alerts if drowning-like behavior is detected.

 🚀 Features

* Real-time drowning detection using YOLOv8
* Support for live webcam/video stream input
* Annotated datasets with drowning and non-drowning scenarios
* Custom trained YOLOv8 model with bounding box detection
* Frame-by-frame analysis with alert system integration potential
* Exportable predictions and video with bounding boxes

 🧠 Model Details

* Base Model: YOLOv8 (Ultralytics)
* Framework: PyTorch
* Training: Custom dataset with annotated drowning and safe swimming behavior
* Input: Video stream or pre-recorded video
* Output: Bounding boxes with class labels (Drowning, Safe)

 📁 Folder Structure

```
drowning-detection-yolo/
├── datasets/
│   └── drowning/               # Annotated dataset (YOLO format)
├── runs/                       # YOLOv8 training results and logs
├── weights/
│   └── best.pt                 # Trained YOLOv8 model weights
├── detect.py                   # Detection script
├── train.py                    # Custom training script
├── README.md
└── requirements.txt
```

🛠️ Installation

1. Clone the repository:

   ```bash
   git clone https://github.com/your-username/drowning-detection-yolo.git
   cd drowning-detection-yolo
   ```

2. Install dependencies:

   ```bash
   pip install -r requirements.txt
   ```

3. Download YOLOv8 from Ultralytics:

   ```bash
   pip install ultralytics
   ```

 🧪 Running Detection

To run detection on a video or webcam:

```bash
yolo detect predict model=weights/best.pt source=your_video.mp4
```

For webcam input:

```bash
yolo detect predict model=weights/best.pt source=0
```

🏋️‍♂️ Training

To train the model on your dataset:

```bash
yolo detect train data=datasets/drowning/data.yaml model=yolov8n.pt epochs=100 imgsz=640
```

📊 Evaluation

* Precision, Recall, mAP scores are computed automatically after training.
* Visual results are saved in the `runs/detect/` directory.


