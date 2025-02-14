# Virtual-Mouse
This project implements a Virtual Mouse that allows users to control the cursor and perform mouse actions using hand gestures, eliminating the need for a physical mouse.
##🔹 How It Works
#✅ 1. Hand Tracking using Mediapipe
--**The handDetector class is created to detect hands using Mediapipe's Hand Tracking module.
--**It identifies 21 landmarks on the hand and draws connections between them.
--**The findHands() method processes the video frame and detects hands in real-time.
#✅ 2. Cursor Control
--**The index finger controls the cursor movement.
--**The detected fingertip coordinates are mapped to the screen using numpy.interp().
--**A smoothing algorithm prevents jittery movements.
#✅ 3. Click Detection
--**The program detects which fingers are up using the fingersUp() method.
--**If only the index finger is up, the cursor moves.
--**If both the index and middle fingers are up, the program detects a click when the two fingertips are close enough (findDistance() method).
#✅ 4. Virtual Mouse Actions
--**Move Cursor → Move the index finger
--**Left Click → Touch index and middle fingers together
--**Smooth Movement → Uses an averaging technique to prevent jerky cursor motion
##🔹 Technologies Used
--**Python 🐍
--**OpenCV (for real-time video processing)
--**Mediapipe (for hand tracking)
--**PyAutoGUI (for controlling the mouse)
--**NumPy (for coordinate mapping)
