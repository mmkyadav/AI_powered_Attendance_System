# AI-Powered Student Attendance System

An automated face recognition–based student attendance system that identifies students in real time using a camera feed and marks attendance securely in the cloud. The system replaces manual roll calls with a fast, contactless, and scalable solution.

---

## 📌 Features

- Real-time face recognition using a webcam  
- Automatic attendance marking with cooldown control  
- Admin and student web portals  
- Secure cloud storage using Firebase  
- Student management (add, update, delete)  
- Attendance visualization with dynamic UI  
- Cloud-based student data and image storage  

---

## 🧠 How It Works

1. **Student Registration**
   - Admin uploads student details and face image
   - Face is detected, cropped, and standardized
   - Facial features are encoded into numerical embeddings

2. **Face Encoding**
   - A pre-trained deep learning model (dlib) converts faces into 128-D vectors
   - Encodings are stored locally for fast comparison

3. **Real-Time Recognition**
   - Webcam captures live video
   - Face embeddings are generated in real time
   - Euclidean distance is used to match faces

4. **Attendance Update**
   - Attendance is marked only if a cooldown period has passed
   - Data is stored in Firebase Realtime Database

5. **Web Interface**
   - Flask-based admin and student dashboards
   - Admin can manage students
   - Students can view their attendance records

---

## 🏗️ Project Structure

```
AI-Powered-Student-Attendance-System/
│
├── main.py
├── InterfaceMain.py
├── AddDataToDatabase.py
├── EncodeGenerator.py
├── encode_upload.py
├── face_processing.py
├── FaceCropping.py
├── requirements.txt
│
├── Images/
├── Resources/
│   └── Modes/
├── templates/
│
└── encodeFile.p
```

---

## 🧰 Technology Stack

**Programming & Frameworks**
- Python
- Flask

**Computer Vision & AI**
- OpenCV
- face_recognition (dlib)
- cvzone

**Cloud Services**
- Firebase Realtime Database
- Firebase Cloud Storage

**Data Handling**
- Pickle

---


---

## 🔐 Security & Constraints

- Firebase Admin SDK for secure data access
- Attendance cooldown prevents duplicate entries
- Admin-only access for student management

---

## ⚠️ Limitations

- Face encodings are regenerated entirely when a student is added or removed
- Haar Cascade face detection is sensitive to lighting conditions
- Hard-coded local paths reduce portability
- No liveness detection (photo spoofing possible)

---

## 🚀 Future Enhancements

- Replace Haar Cascade with MTCNN or MediaPipe
- Incremental face encoding updates
- Store encodings in a database instead of pickle files
- Add liveness detection
- Deploy as a cloud-hosted service
- Support multiple cameras and classrooms

---

## ▶️ How to Run

1. Clone the repository
```bash
git clone https://github.com/your-username/AI-Powered-Student-Attendance-System.git
```

2. Install dependencies
```bash
pip install -r requirements.txt
```

3. Configure Firebase
- Add your Firebase Admin SDK JSON file
- Update database and storage URLs in the code

4. Run the web application
```bash
python InterfaceMain.py
```

5. Run the attendance system
```bash
python main.py
```

---

## 👤 Author

**M. Muddu Krishna**

---



---

## 📄 License

This project is intended for educational and demonstration purposes.
