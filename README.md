Driver Drowsiness Detection and Intelligent Voice Assistant System

Overview

This project is a real-time Driver Monitoring System that detects drowsiness and yawning using computer vision and facial landmark analysis. The system continuously monitors the driver through a webcam and provides instant voice alerts if fatigue is detected.

The application also logs all alert events and generates a trip summary at the end of the session. Additionally, it includes a voice interaction feature that allows activation through a spoken command.

The primary objective of this project is to improve road safety by reducing accidents caused by driver fatigue.

Features

* Real-time face detection using dlib
* Eye Aspect Ratio based drowsiness detection
* Mouth Aspect Ratio based yawn detection
* Offline voice alerts using pyttsx3
* Continuous monitoring with automatic event logging
* CSV log file generation
* Trip summary generation
* Voice activation system
* Multi-threaded non-blocking speech system

Technologies Used

* Python
* OpenCV
* Dlib
* Scipy
* Imutils
* Pyttsx3
* SpeechRecognition
* Pandas

System Architecture

1. The webcam captures live video input.
2. Face detection is performed using dlib’s frontal face detector.
3. Facial landmarks are extracted using a pretrained 68-point landmark model.
4. Eye Aspect Ratio (EAR) is calculated to detect prolonged eye closure.
5. Mouth Aspect Ratio (MAR) is calculated to detect yawning.
6. If EAR falls below a threshold for a defined number of frames, drowsiness is detected.
7. If MAR exceeds the threshold, yawning is detected.
8. Voice alerts are triggered using offline text-to-speech.
9. Events are logged into a CSV file.
10. A trip summary is generated at the end of the session.

Installation

1. Clone the Repository

```bash
git clone https://github.com/your-username/driver-drowsiness-detection.git
cd driver-drowsiness-detection
```

2. Install Dependencies

```bash
pip install opencv-python
pip install dlib
pip install imutils
pip install scipy
pip install pandas
pip install pyttsx3
pip install SpeechRecognition
```

3. Download Facial Landmark Model

Download the file:

```
shape_predictor_68_face_landmarks.dat
```

Place it inside your project directory.

You can obtain this file from the official dlib model repository.


How to Run

```bash
python main.py
```

Press `q` to exit the application.

Output

During Execution:

* Live webcam feed is displayed.
* Eye and mouth contours are drawn.
* Real-time EAR and MAR values are shown.
* Voice alerts are generated when fatigue is detected.

After Execution:

* A file named `drowsiness_log.csv` is created.
* A trip summary is printed.
* The summary is spoken via text-to-speech.

Project Structure

```
driver-drowsiness-detection/
│
├── main.py
├── shape_predictor_68_face_landmarks.dat
├── drowsiness_log.csv
└── README.md
```


Tell me what you need next.
