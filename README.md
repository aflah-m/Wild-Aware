🐘 WILD EYE: Wild Animal Intrusion Detection System
A real-time wildlife detection system using YOLOv8 to identify elephants and bears via webcam and trigger an alarm for early warning.

📖 Introduction
Wild animal intrusions near human settlements, farmlands, or forest-adjacent areas pose serious threats to both people and wildlife. Early detection and timely alerts are essential to prevent dangerous encounters and property damage.

This project provides a real-time animal detection system using the YOLOv8 deep learning model to identify specific wild animals—such as elephants and bears—through a live camera feed. Upon detection, a loud alarm is triggered to alert nearby individuals, allowing a quick response and deterrence.

By combining computer vision, deep learning, and audio alerts, this system can serve as a low-cost, efficient, and customizable solution for wildlife monitoring, farm protection, and early warning systems in rural or high-risk zones.

⚠️ Note: The model is trained only for specific animals relevant to the target environment (primarily elephants and bears).

🛠️ Tools & Technologies Used
Tool / Library	Purpose
YOLOv8 (Ultralytics)	Real-time object detection (PyTorch backend)
OpenCV	Webcam access and frame rendering
Pygame	Plays alarm sound on detection
Python 3.8+	Core scripting language
Threading	Non-blocking alarm execution
Custom YOLO Model	Trained to recognize elephants and bears

🚀 Quick Start
1. Clone the repository
bash
Copy
Edit
git clone https://github.com/aflah-m/WILD-EYE.git
cd WILD-EYE
2. Install dependencies
bash
Copy
Edit
pip install ultralytics opencv-python pygame
3. Run the detection script
bash
Copy
Edit
python animal_detection.py
🎥 Make sure your webcam is accessible and not used by other applications.

📦 Files Included
File	Description
animal_detection.py	Main Python script
best.pt	YOLOv8 custom-trained model for detection
alarm.wav	Alarm sound triggered upon detection
README.md	Project documentation

⚠️ Python Interpreter Warning Fix (VS Code)
If you see a warning about the Python interpreter:

Press Ctrl + Shift + P

Choose "Python: Select Interpreter"

Select .venv/Scripts/python.exe or your active environment interpreter.

🧠 Model Details
best.pt is a custom-trained YOLOv8 model.

Trained primarily for:

Elephant (class ID 20)

Bear (class ID 21)

Uses a COCO-style dataset

📁 Dataset Structure (for retraining)
bash
Copy
Edit
datasets/
├── images/
│   ├── train/
│   ├── val/
│   └── test/         # Optional
├── labels/
│   ├── train/
│   ├── val/
│   └── test/
Each label file must follow YOLO format:

php-template
Copy
Edit
<class_id> <x_center> <y_center> <width> <height>
All values should be normalized between 0 and 1.

🔧 Customization
To detect more animals:
Retrain or fine-tune best.pt with additional classes.

Replace best.pt in the project.

Update the target_ids list in animal_detection.py.

To change the alarm sound:
Replace alarm.wav with your preferred .wav file.

🖼️ Sample Output
(Insert detection screenshots or sample video clips here.)

📌 Notes
Uses YOLOv8 via Ultralytics Python package.

Automatically leverages GPU if available.

Threading is used to prevent lag during alarm playback.

📜 License
This project is open-source and available under the MIT License.

🙏 Acknowledgements
Ultralytics YOLOv8

COCO Dataset

Python, OpenCV, Pygame
