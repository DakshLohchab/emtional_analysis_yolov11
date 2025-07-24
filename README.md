Facial Emotion Detection using YOLOv11
This project implements real-time facial emotion detection using YOLOv11, a state-of-the-art object detection model. The model has been trained on a custom-labeled dataset sourced from Roboflow Universe, consisting of seven basic human emotions.

🔍 Overview
Facial Emotion Detection aims to identify and classify human emotions from facial expressions in images or video streams. This project detects the following seven emotions:

😠 Angry

🤢 Disgust

😱 Fear

😄 Happy

😐 Neutral

😢 Sad

😲 Surprise

🧠 Model Architecture
Model: YOLOv11 (You Only Look Once - Version 11)

Framework: Ultralytics YOLO

Dataset: Roboflow Universe - Facial Emotion Dataset

Training Framework: Python with PyTorch

📂 Dataset Details
Source: Roboflow Universe

Images: Preprocessed, annotated with bounding boxes and labels

Format: YOLOv8-compatible format

Split:

Training: 70%

Validation: 20%

Test: 10%

🏁 Getting Started
1. Clone the repository
bash
Copy
Edit
git clone https://github.com/your-username/facial-emotion-yolov11.git
cd facial-emotion-yolov11
2. Install dependencies
bash
Copy
Edit
pip install ultralytics
3. Download dataset from Roboflow
You can either:

Use the Roboflow integration in the data.yaml file.

Or download manually and set paths in data.yaml.

Example data.yaml:

yaml
Copy
Edit
train: /path/to/train
val: /path/to/valid
test: /path/to/test

nc: 7
names: ['angry', 'disgust', 'fear', 'happy', 'neutral', 'sad', 'surprise']
4. Train the model
bash
Copy
Edit
yolo train model=yolov11.pt data=data.yaml epochs=50 imgsz=640
5. Run Inference
bash
Copy
Edit
yolo detect model=runs/detect/train/weights/best.pt source=path_or_video
