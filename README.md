I made this project to demonstrate how to control the brightness of an LED connected to an Arduino board based on hand gestures detected using a webcam. The project leverages various libraries, including machine learning solutions for hand landmark detection, and integrates with Arduino for hardware control.


The project captures video from a webcam, processes the video to detect hand landmarks using MediaPipe's machine learning models, and adjusts the brightness of an LED connected to an Arduino board based on the distance between the thumb and index finger.

Real-time Hand Detection: Utilizes MediaPipe's hand tracking solution to detect hand landmarks in real-time.
LED Brightness Control: Adjusts the brightness of an LED based on the distance between the thumb and index finger.
Integration with Arduino: Uses the PyFirmata library to communicate with an Arduino board and control the LED.

Requirements
Python 3.x
OpenCV (Library)
MediaPipe (Library)
PyFirmata2 (Library)
NumPy(Library)
Arduino board
LED and appropriate resistors
Webcam
  
  
   STEPS:


Import Libraries: The script starts by importing necessary libraries: OpenCV for video capture, MediaPipe for hand tracking, PyFirmata2 for Arduino communication, and NumPy for data manipulation.

Initialize Arduino: The Arduino board is initialized on the specified COM port, and the LED pin is set up for PWM control.

Webcam Capture: The webcam is initialized for video capture.

Hand Detection: MediaPipe's hand solution is used to detect hand landmarks in each frame.

Distance Calculation: The Euclidean distance between the thumb tip and index finger tip is calculated.

LED Brightness Control: The distance is mapped to a PWM signal range (0-1) and sent to the Arduino to adjust the LED brightness.

Display Video: The video feed with hand landmarks is displayed in a window.
