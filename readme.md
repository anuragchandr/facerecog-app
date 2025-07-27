# Face Recognition Attendance System

## Overview
This Python application uses face recognition technology to mark attendance automatically. It captures video from a webcam, detects faces, compares them with known faces in the database, and records attendance with timestamps in a CSV file.

## Features
- Real-time face detection and recognition
- Automatic attendance marking with timestamps
- CSV file generation for attendance records
- Simple and intuitive interface

## Requirements
- Python 3.x
- OpenCV (`cv2`)
- face_recognition library
- NumPy
- CSV module (built-in)
- datetime module (built-in)

## Installation
1. Install the required packages:
   ```bash
   pip install face-recognition opencv-python numpy
   ```

2. Prepare your face database:
   - Create a folder named `faces` in the same directory as the script
   - Add JPEG images of people you want to recognize (e.g., `harry.jpg`, `arjun.jpg`)
   - The filename (without extension) will be used as the person's name in the system

## Usage
1. Run the script:
   ```bash
   python attendance_system.py
   ```

2. The system will:
   - Open a camera window showing real-time video
   - Detect and recognize faces
   - Mark attendance automatically when a known face is detected
   - Create a CSV file with the current date as filename (e.g., `2023-11-15.csv`)

3. Press 'q' to quit the application

## Output
The system generates a CSV file for each day with the following format:
```
Name, Time
Harry, 14:30:25
Arjun, 14:31:10
```

## Customization
- To add more people, simply add their images to the `faces` folder and update the code to include their encodings
- Adjust recognition parameters like face distance threshold by modifying the `compare_faces` logic
- Change the display text properties (font, size, color) in the `cv2.putText` function

## Notes
- The system works best with clear, front-facing images in the database
- Lighting conditions may affect recognition accuracy
- For better performance with multiple faces, consider using a higher-resolution camera

## License
This project is open-source and free to use. Modify and distribute as needed.