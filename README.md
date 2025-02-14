# Virtual Mouse

## Overview
The Virtual Mouse project allows users to control the cursor and perform mouse actions using hand gestures, eliminating the need for a physical mouse. It leverages computer vision techniques to track hand movements and execute virtual mouse operations.

## Features
- **Hand Tracking**: Detects and tracks hands using Mediapipe's Hand Tracking module.
- **Cursor Control**: Maps hand gestures to screen coordinates for smooth cursor movement.
- **Click Detection**: Recognizes gestures to perform left-click and other mouse actions.
- **Gesture-Based Mouse Actions**: Enables various mouse interactions using specific hand gestures.
- **Smooth Movement**: Implements an averaging technique to prevent jittery cursor motion.

## How It Works
### 1. Hand Tracking using Mediapipe
- The `handDetector` class detects hands using Mediapipe's Hand Tracking module.
- Identifies 21 landmarks on the hand and draws connections between them.
- The `findHands()` method processes the video frame and detects hands in real-time.

### 2. Cursor Control
- The index finger controls the cursor movement.
- Fingertip coordinates are mapped to the screen using `numpy.interp()`.
- A smoothing algorithm ensures stable cursor movement.

### 3. Click Detection
- The program detects which fingers are up using the `fingersUp()` method.
- If only the index finger is up, the cursor moves.
- If both the index and middle fingers are up, a click is detected when the fingertips are close (using the `findDistance()` method).

### 4. Virtual Mouse Actions
- **Move Cursor** → Move the index finger.
- **Left Click** → Touch index and middle fingers together.
- **Smooth Movement** → Uses an averaging technique to prevent jerky cursor motion.

## Installation
To install and run the Virtual Mouse application, follow these steps:

1. **Clone the repository**
   ```bash
   git clone https://github.com/your-username/virtual-mouse.git
   ```
2. **Navigate to the project directory**
   ```bash
   cd virtual-mouse
   ```
3. **Install dependencies**
   ```bash
   pip install -r requirements.txt
   ```  
4. **Run the application**
   ```bash
   python virtual_mouse.py
   ```

## Technologies Used
- **Python** 🐍
- **OpenCV** (for real-time video processing)
- **Mediapipe** (for hand tracking)
- **PyAutoGUI** (for controlling the mouse)
- **NumPy** (for coordinate mapping)

## License
This project is licensed under the MIT License (LICENSE).

## Contact
For any questions, feedback, or support, please contact:

- **E-mail**: palegariroopeshnaidu@gmail.com
- **GitHub**: github.com/Roopi0963

