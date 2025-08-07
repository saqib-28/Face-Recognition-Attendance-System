
# 🧠 Smart Face Recognition Attendance System

This project implements a real-time face recognition attendance system that captures video through a webcam, identifies known individuals, and logs their attendance with timestamps. It combines computer vision and facial recognition technology to automate attendance tracking efficiently.

## 🎯 Key Features

- 🔍 Real-time facial recognition from webcam input
- 📋 Automatic attendance logging with name and timestamp
- 🖼️ GUI interface to display live video feed and recognized faces
- 📁 Attendance records saved to a CSV file for easy tracking

## 🧰 Requirements

- Python 3.x
- OpenCV (`opencv-python`)
- `face_recognition` library
- `Tkinter` (built-in with Python)
- `Pillow` for image handling

### ✅ Install Dependencies

```bash
pip install opencv-python face_recognition pillow
```

## 🚀 How to Use

1. **Prepare your dataset:**
   - Add clear face images of each known person into the `known_faces/` directory.
   - Example: `known_faces/john_doe.jpg`

2. **Run the application:**
   ```bash
   python face_recognition_attendance.py
   ```

3. **View attendance records:**
   - Attendance entries will be saved in a CSV file named `attendance.csv`, including the recognized name and timestamp.

## ⚙️ How It Works

- Loads and encodes known faces from images in the `known_faces/` folder
- Continuously captures video from the webcam and detects faces
- Matches detected faces with known encodings using the `face_recognition` library
- Logs each matched individual's name and current time into `attendance.csv`
- Prevents duplicate entries for the same person in a single session

## 📦 Project Structure

```
FaceRecognitionAttendance/
├── known_faces/                   # Folder for reference face images
│   └── john_doe.jpg
├── attendance.csv                 # Log file for attendance records
├── face_recognition_attendance.py# Main script
└── README.md                      # Project documentation
```

## 💡 Future Improvements

- Add database integration for secure attendance management
- Implement notification or alert system for unknown faces
- Integrate with access control hardware for physical security

