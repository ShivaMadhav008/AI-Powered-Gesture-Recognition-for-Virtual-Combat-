# AI-Powered-Gesture-Recognition-for-Virtual-Combat-
🎮 Controller-Free Gaming Using AI and Computer Vision

This project introduces an AI-powered gesture recognition system that transforms human body movements into real-time in-game actions. Using MediaPipe BlazePose, OpenCV, and pynput, players can perform gestures like punches, kicks, jumps, and crouches to control characters in fighting games — no physical controller required.

📘 Overview

The project leverages pose estimation and gesture recognition to create an immersive, interactive virtual combat experience. It enables natural full-body gameplay while providing the foundation for fitness, rehabilitation, and accessibility applications.

Key features include:

Real-time gesture tracking and recognition

Calibration for player-specific movement thresholds

Automatic key mapping to existing PC games

Optional Arduino-powered haptic feedback for immersive sensations

Potential multiplayer support via socket-based networking

🧠 Core Technologies
Category	Tools / Libraries
Programming Language	Python 3.x
Computer Vision	OpenCV
Pose Estimation	MediaPipe BlazePose
Key Simulation	pynput
AI Frameworks	TensorFlow / PyTorch
Visualization	Matplotlib
IDE Recommended	VS Code / PyCharm

⚙️ System Requirements
Hardware
CPU: Intel i5 / AMD Ryzen 5 or higher
RAM: Minimum 8GB (16GB recommended)
Webcam: 720p @ 30 FPS

Software
OS: Windows / Linux / macOS
Python 3.8+

Required libraries:
pip install opencv-python mediapipe pynput matplotlib numpy

🚀 How It Works
Frame Capture – The webcam captures live frames using OpenCV.
Pose Detection – MediaPipe BlazePose extracts 33 key landmarks from the body.
Gesture Recognition – Keypoint distances and movement patterns identify gestures like:
🥊 Punch (wrist entering hitbox)
🦵 Kick (knee movement)
🧍 Jump / Crouch (head & hip movement)
Action Mapping – Detected gestures are translated into keyboard inputs via pynput.
Game Control – The inputs control a PC fighting game

Output
Displays webcam feed with keypoint visualization and bounding boxes.
Logs detected gestures such as:

right_wrist HIT
left_knee HIT

Simulates mapped keypresses for in-game actions.

🧬 System Architecture
Camera Input → Pose Estimation → Gesture Engine → Keypress Simulation → Game Window

CameraManager: Captures real-time frames
PoseEstimator: Detects body landmarks
GestureEngine: Identifies gestures (punch, kick, crouch, jump)
KeypressController: Triggers mapped keypresses
CalibrationManager: Adapts thresholds for each player

🏁 Results
Achieved real-time recognition with low latency (<100ms)
Smooth gameplay control with minimal false positives
Compatible with most PC games via keyboard simulation
Extendable framework for custom gestures and multiplayer features
