Virtual Mouse Using Hand Gestures
This project implements a virtual mouse controlled by hand gestures using OpenCV, MediaPipe, and PyAutoGUI. It allows users to perform mouse movements and actions like clicks, double clicks, and screenshots through hand gestures detected via webcam.



Features
Mouse Movement: Control the mouse pointer using the tip of your index finger.
Left Click: Perform a left-click gesture by closing your thumb and index finger at a specific angle.
Right Click: Perform a right-click gesture by a different angle of the fingers.
Double Click: Trigger a double-click by combining specific finger gestures.
Screenshot: Capture the screen when a gesture indicating a screenshot is detected.
Technology Used
OpenCV: Captures webcam feed and processes video frames.
MediaPipe: Detects hand landmarks and tracks finger movements.
PyAutoGUI: Handles mouse control and screenshots.
Pynput: Simulates mouse button clicks programmatically.
Custom Utility Module: Provides gesture-detection helper functions for distance and angle calculations.
Code Explanation
1. Hand Landmark Detection:
MediaPipe Hands: Tracks hand landmarks and detects the index finger's tip.
HandLandmark Enumeration: Provides access to specific points like the tip of the index finger.
2. Gesture Recognition:
Custom functions (is_left_click, is_right_click, etc.) determine gestures using:
Angles between finger joints.
Distances between specific landmarks.
3. Mouse Control:
move_mouse: Maps the hand movement coordinates to screen dimensions and moves the mouse pointer accordingly.
Gestures for Actions:
Left Click: Triggered by a specific angle of the index and thumb.
Right Click: Similar logic but with different angles.
Double Click: Checks simultaneous conditions.
Screenshot: Gesture detected based on thumb-index distance.
4. Real-Time Processing:
Webcam frames are processed in a loop:
Frames are flipped horizontally for a mirror-like experience.
Converted from BGR to RGB for MediaPipe compatibility.
Detected gestures are overlaid on the frame with appropriate annotations.
5. Exiting the Application:
Pressing the 'q' key exits the webcam feed and closes the application gracefully.