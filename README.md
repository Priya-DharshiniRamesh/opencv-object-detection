# 🎯 Real-Time Object Detection using OpenCV DNN and MobileNet-SSD

A simple, beginner-friendly **Object Detection** project built with **OpenCV's DNN module** and the pre-trained **MobileNet-SSD (Caffe)** model. This repo contains two scripts:

- `image_detection.py` — Detect objects in a **static image**.
- `video_detection.py` — Detect objects in **real-time** using your **webcam**.

The model can detect **20 object classes** such as person, car, dog, cat, bicycle, bus, and more.

---

## 🚀 Technologies Used

- Python
- OpenCV
- NumPy
- OpenCV DNN
- MobileNet-SSD
- Caffe Model

---

## ✨ Features

- Detects 20 object classes
- Supports image object detection
- Supports real-time webcam detection
- Displays confidence scores
- Draws bounding boxes around detected objects
- Easy to customize confidence threshold

---
## 🧠 How It Works

This project uses the **MobileNet-SSD** (Single Shot MultiBox Detector) architecture, pre-trained on the **PASCAL VOC dataset**, loaded via OpenCV's `cv2.dnn` module. For every frame/image:

1. The input is converted into a **blob** (resized to 300x300, normalized).
2. The blob is passed through the pre-trained Caffe network.
3. Detected objects above a confidence threshold are drawn with bounding boxes, class labels, and confidence scores.

---

## 📂 Project Structure

```
Object-Detection/
│
├── models/
│   ├── MobileNetSSD_deploy.prototxt       # Model architecture
│   └── MobileNetSSD_deploy.caffemodel     # Pre-trained weights
│
├── image_detection.py                     # Detect objects in an image
├── video_detection.py                     # Detect objects via webcam
├── requirements.txt
└── README.md
```

---

## 🛠️ Requirements

- Python 3.7+
- OpenCV (with DNN support)
- NumPy

Install dependencies:

```bash
pip install -r requirements.txt
```

**requirements.txt**
```
opencv-python
numpy
```

---

## 📥 Download the Pre-trained Model

This repo does **not** include the model files (they're excluded via `.gitignore` since binary weight files are large). Download them and place them inside the `models/` folder:

- `MobileNetSSD_deploy.prototxt`
- `MobileNetSSD_deploy.caffemodel`

---

## ▶️ Usage

### 1. Object Detection on an Image

Update the `image_path` variable in `image_detection.py` to point to your image, then run:

```bash
python image_detection.py
```

Press any key to close the output window.

### 2. Real-Time Object Detection via Webcam

```bash
python video_detection.py
```

Press **`q`** to quit the webcam window.

---

## ⚙️ Configuration

You can tweak these variables in either script:

| Variable | Description | Default |
|----------|-------------|---------|
| `min_confidence` | Minimum confidence threshold to display a detection | `0.2` |
| `classes` | List of 20 detectable object classes (PASCAL VOC) | — |

---

## 🏷️ Detectable Classes

```
aeroplane, bicycle, bird, boat, bottle, bus, car, cat, chair, cow,
diningtable, dog, horse, motorbike, person, pottedplant, sheep,
sofa, train, tvmonitor
```

---

## 📌 Notes

- Lower `min_confidence` to detect more objects (may increase false positives); raise it for stricter detections.
- Webcam index `0` is used by default in `video_detection.py` — change it if you have multiple cameras.

---

## 🔮 Future Improvements

- YOLOv8 integration
- Video file object detection
- FPS counter
- Object tracking
- Custom dataset training

---

## 👩‍💻 Author

**Priya Dharshini R**\
srpriyadharshini16@gmail.com
