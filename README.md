# 🧠 Real-Time Video Emotion Detector (OpenCV + DeepFace)

A Python application that analyzes live webcam video to detect and visualize human emotions in real time.
Using **OpenCV**, it detects faces and draws bounding boxes around them — the box color dynamically changes based on the detected emotion identified through **DeepFace**’s facial analysis.

### 🎥 How It Works

* Captures live video feed from your webcam.
* Detects faces using OpenCV’s **Haar Cascade Classifier**.
* Analyzes each face with **DeepFace** to identify the dominant emotion (e.g., *happy, sad, angry, neutral, fear*).
* Updates the bounding box color to represent the emotion:

  * 🟩 **Happy** → Green
  * 🟦 **Sad** → Blue
  * 🟥 **Angry** → Red
  * 🟧 **Neutral** → Orange
  * ⚫ **Fear** → Gray

### ⚙️ Technologies Used

* **Python**
* **OpenCV** — for real-time face detection
* **DeepFace** — for emotion recognition
* **Haar Cascade XML** — pretrained model for frontal face detection

### 🚀 How to Run

1. Install dependencies:

   ```bash
   pip install opencv-python deepface
   ```
2. Download the [Haar Cascade XML file](https://raw.githubusercontent.com/opencv/opencv/4.x/data/haarcascades/haarcascade_frontalface_default.xml) and place it in your project directory.
3. Run the script:

   ```bash
   python app.py
   ```
4. Press **Q** to quit the app.

### 🧩 Notes

* You can replace the webcam feed with a video file by changing:

  ```python
  webcam = cv2.VideoCapture(0)
  ```

  to:

  ```python
  webcam = cv2.VideoCapture("path_to_video.mp4")
  ```

