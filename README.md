# 🖱️ Virtual Mouse Using Hand Gestures

This project implements a **virtual mouse** controlled entirely through **hand gestures** using your **webcam**, built with **OpenCV**, **MediaPipe**, **PyAutoGUI**, and **Pynput**.

With simple finger movements, you can move the cursor, perform clicks, take screenshots, and more — all hands-free!

---

## 🚀 Features

- 🎯 **Mouse Movement**  
  Control the on-screen cursor using the **index finger tip**.

- 👆 **Left Click**  
  Detected by closing the **thumb and index finger** at a specific angle.

- 👉 **Right Click**  
  Triggered by a different **finger gesture and angle**.

- ✌️ **Double Click**  
  Recognized via a combination of simultaneous gestures.

- 📸 **Screenshot**  
  Captured when a special **screenshot gesture** is performed.

---

## 🧠 Technology Stack

| Library      | Purpose                                      |
|--------------|----------------------------------------------|
| OpenCV       | Webcam access and video frame processing     |
| MediaPipe    | Real-time hand landmark detection            |
| PyAutoGUI    | Mouse control and screenshot functionality   |
| Pynput       | Mouse click simulation                       |
| Custom Utils | Angle & distance calculations for gestures   |

---

## 🧩 Code Explanation

### ✋ Hand Landmark Detection

- **MediaPipe Hands**  
  Used to detect and track hand landmarks, especially the **index finger tip**.

- **HandLandmark Enumeration**  
  Makes it easy to refer to landmarks like `INDEX_FINGER_TIP`, `THUMB_TIP`, etc.

---

### 🤙 Gesture Recognition Logic

Custom functions like:
- `is_left_click()`
- `is_right_click()`
- `is_double_click()`
- `is_screenshot()`

Use a combination of:
- **Angles between finger joints**
- **Distances between specific hand landmarks**

---

### 🖱️ Mouse Control

- `move_mouse()`  
  Maps **hand coordinates** to **screen dimensions** to move the mouse pointer smoothly.

- **Click Actions**
  - **Left Click:** Triggered by thumb-index angle threshold.
  - **Right Click:** Different angle gesture.
  - **Double Click:** Combo detection.
  - **Screenshot:** Triggered by thumb-index distance threshold.

---

### 🌀 Real-Time Processing Flow

1. Webcam feed is captured and **horizontally flipped** (mirror effect).
2. Frames are converted from **BGR → RGB** for MediaPipe compatibility.
3. Hand gestures are detected and interpreted.
4. Actions are triggered and **visual feedback is drawn** on the frame.
5. Press `'q'` to exit cleanly.

---

## 📷 Demo (Optional)

> Include a small GIF or video showcasing:
> - Mouse movement
> - Left/right click
> - Screenshot gesture

---


