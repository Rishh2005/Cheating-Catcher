# Cheating-Catcher
A real-time concentration and distraction tracker using your webcam, built with Python, OpenCV, and MediaPipe.  
It analyzes your face to estimate concentration based on gaze, head pose, and blink detection, and provides live feedback on your focus level.

---

## How It Works

1. **Face Detection:**  
   Uses MediaPipe Face Mesh to detect your face and facial landmarks from the webcam feed.

2. **Eye Aspect Ratio (EAR):**  
   Calculates the EAR to detect blinks.

3. **Gaze & Head Pose:**  
   Estimates if you are looking at the screen and if your head is centered.

4. **Concentration Score:**  
   Combines gaze, head pose, and blink status into a concentration score (0–100%).

5. **Distraction Counter:**  
   Increments a distraction count if your concentration drops below a threshold.

6. **Visual Feedback:**  
   Shows your concentration score, distraction count, FPS, and status (ACTIVE/DISTRACTED) on the video feed.

**Note:**  
No facial dots or lines are drawn on the video feed for a clean UI.

---

## Requirements

| Library      | Version (Recommended) | Description                                      |
|--------------|----------------------|--------------------------------------------------|
| Python       | 3.8+                 | Programming language                             |
| OpenCV       | 4.5+                 | Real-time computer vision library                |
| mediapipe    | 0.8+                 | Face mesh and landmark detection                 |
| numpy        | 1.19+                | Numerical operations                             |

### Install requirements

```bash
pip install opencv-python mediapipe numpy
```

---

## File Structure

| File Name           | Description                                 |
|---------------------|---------------------------------------------|
| Concentration.py    | Main script for concentration tracking      |
| README.md           | Project documentation (this file)           |

---

## Library Descriptions

- **OpenCV (`cv2`):**  
  Used for capturing webcam video, drawing UI elements, and displaying the video feed.

- **MediaPipe (`mediapipe`):**  
  Provides the Face Mesh solution for detecting facial landmarks in real time.

- **NumPy (`numpy`):**  
  Used for efficient numerical calculations, such as distances and averages.

- **collections.deque:**  
  For maintaining a rolling history of scores and FPS for smoothing.

- **time:**  
  For measuring FPS and implementing cooldowns.

---

## How to Run

1. Make sure your webcam is connected.
2. Install the requirements.
3. Run the script:

   ```bash
   python Concentration.py
   ```

4. A window will open showing your webcam feed with your concentration stats.
5. Press `q` to quit.

---

## About the Author

**Name:** Rishabh Jain
**Project:** Cheating Catcher
**Contact:** rishabhjain1175@gmail.com

---

## License

This project is for educational and non-commercial use only.  
Feel free to modify and distribute it, but please give credit to the original author.
