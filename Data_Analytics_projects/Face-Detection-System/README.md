# 🎭 Face Detection System

A real-time face detection application built with Python and OpenCV. Uses Haar Cascade classifiers to detect and highlight faces through a live webcam feed.

> **Learning Context:** Data Analytics Course — Practical Project

![Python](https://img.shields.io/badge/Python-3.7%2B-blue?style=flat-square&logo=python)
![OpenCV](https://img.shields.io/badge/OpenCV-4.x-green?style=flat-square&logo=opencv)
![License](https://img.shields.io/badge/License-MIT-yellow?style=flat-square)
![Platform](https://img.shields.io/badge/Platform-macOS%20%7C%20Linux%20%7C%20Windows-lightgrey?style=flat-square)

---

## 📸 Features

- **Real-time face detection** via webcam using Haar Cascade classifiers
- **Live face counter** displayed directly on the video feed
- **Snapshot capture** — save the current frame with a single keypress
- **Lightweight & fast** — no deep learning dependencies required

<img width="1440" height="900" alt="Screenshot 2026-02-22 at 16 49 48" src="https://github.com/user-attachments/assets/1ae319a3-5e59-4bf4-8afb-72667d09d3c9" />


---

## 🛠️ Requirements

- Python 3.7+
- OpenCV (`opencv-python`)

---

## ⚙️ Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/moubani-dev/Data_Analytics_Handbook.git
cd Data_Analytics_Handbook
   ```

2. **Install dependencies**
   ```bash
   pip install opencv-python
   ```

3. **Run the application**
   ```bash
   python Data_Analytics_projects/Face-Detection-System/face_detection.py
   ```

---

## 🎮 Controls

| Key | Action |
|-----|--------|
| `S` | Save current frame as `captured_face.jpg` |
| `Q` | Quit the application |

---

## 🧠 How It Works

The application uses OpenCV's pre-trained **Haar Cascade classifier** (`haarcascade_frontalface_default.xml`) — a machine learning-based approach that identifies faces by analyzing patterns of light and dark regions across an image.

**Detection Pipeline:**
1. Capture a frame from the webcam
2. Convert the frame to grayscale (improves detection speed and accuracy)
3. Run the Haar Cascade detector with a scale factor of `1.3` and a minimum neighbor threshold of `5`
4. Draw a green bounding box around each detected face
5. Overlay the total face count on the video feed

---

## 📁 Project Structure

```
Data_Analytics_Handbook/
└── Data_Analytics_projects/
    └── Face-Detection-System/
        ├── face_detection.py
        └── README.md
```

---

## 🔧 Configuration

You can tune detection sensitivity by adjusting these parameters in `face_detection.py`:

| Parameter | Current Value | Description |
|-----------|--------------|-------------|
| `scaleFactor` | `1.3` | How much the image is scaled down at each step. Lower = more accurate, slower. |
| `minNeighbors` | `5` | Higher values reduce false positives but may miss some faces. |

---

## 📝 Notes

- This project uses `cv2.CAP_AVFOUNDATION` as the camera backend, optimized for **macOS**. On Linux or Windows, you can remove this flag:
  ```python
  cap = cv2.VideoCapture(0)
  ```
- Haar Cascade detection works best under **good lighting** and with **front-facing** subjects.

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## 🙌 Acknowledgements

- [OpenCV](https://opencv.org/) — Open Source Computer Vision Library
- Haar Cascade XML model provided by the OpenCV project


## 👤 Author

Moubani Das

This project was developed as part of my Data Analytics learning journey and practical coursework.