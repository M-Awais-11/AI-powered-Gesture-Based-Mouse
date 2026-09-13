# 🖱️ AI-Powered Gesture-Based Mouse

An AI-powered computer vision system that allows users to control their computer mouse using **hand gestures** detected through a webcam.

The project combines **OpenCV**, **MediaPipe**, and **PyAutoGUI** to provide real-time, hands-free mouse interaction. It detects hand landmarks, interprets finger gestures, and converts them into mouse actions such as cursor movement, left click, right click, and scrolling.

---

## 🚀 Features

- 🖐️ Real-time hand gesture detection
- 🎯 AI-based hand landmark tracking using MediaPipe
- 🖱️ Gesture-controlled cursor movement
- 👆 Left-click gesture
- 🖕 Right-click gesture
- 📜 Scroll up and down using multiple fingers
- 🔒 Cursor lock/unlock gesture
- 🎯 Smooth cursor movement using Exponential Moving Average (EMA)
- ⏱️ Click/action cooldown to prevent accidental repeated actions
- 📷 Real-time webcam processing
- 🛑 Automatically pauses mouse control when the hand leaves the camera view
- 💻 Hands-free human-computer interaction

---

## 🧠 Technologies Used

| Technology | Purpose |
|------------|---------|
| **Python** | Core programming language |
| **OpenCV** | Webcam capture and image processing |
| **MediaPipe** | Real-time hand tracking and landmark detection |
| **PyAutoGUI** | Computer mouse control |
| **NumPy** | Numerical processing used by the computer vision stack |

---

## ✋ Gesture Controls

The system recognizes different finger configurations and maps them to mouse operations.

| Gesture | Action |
|---------|--------|
| ☝️ Index Finger | Move Cursor |
| 🤏 Index Finger Down | Left Click |
| 🖕 Middle Finger Down | Right Click |
| ✌️ Index + Middle Down | Scroll Down |
| 🤟 Index + Middle + Ring Down | Scroll Up |
| 🤙 Pinky Down | Lock / Unlock Cursor |

### Cursor Movement

The cursor follows the position of the **index and middle fingertips**.

Their coordinates are averaged to create a more stable reference point:

```text
Cursor Position
      ↑
      |
Index + Middle
  Fingertips
      |
      ↓
Screen Coordinates
