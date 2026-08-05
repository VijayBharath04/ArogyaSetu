📱 ArogyaSetu Mobile Node – Nurse Interaction Tool
Overview

ArogyaSetu Mobile Node is a lightweight, browser-based application designed to assist nurses and frontline healthcare workers in capturing patient information quickly during primary screening. The application performs on-device facial distress detection using MediaPipe FaceMesh and records patient symptoms through speech-to-text or manual text entry.

The entire application is built as a single HTML file, making it easy to deploy and run without complex installation or server-side processing.

Features
🎥 Real-Time Face Distress Detection
Uses MediaPipe FaceMesh to analyze facial landmarks.
Computes a simple heuristic based on eyebrow-to-eye landmark distances.
Classifies patient distress into:
LOW
MEDIUM
HIGH
🎙️ Speech-to-Text Symptom Capture
Uses the Web Speech API for voice recognition.
Converts spoken symptoms into text automatically.
Supports manual editing and text input.
📄 Patient Data Collection
Captures:
Timestamp
Distress Level
Symptoms
🌐 Backend Integration
Sends collected patient information as a JSON payload to a configured clinic hub endpoint using the Fetch API.
⚡ Lightweight Deployment
Single HTML file.
No installation required.
Runs directly in modern web browsers.
Technology Stack
Component	Technology
Frontend	HTML, CSS, Vanilla JavaScript
Face Detection	MediaPipe FaceMesh
Camera Access	MediaPipe Camera Utils
Speech Recognition	Web Speech API
Communication	Fetch API
Runtime	Modern Web Browser
Project Workflow
Open the application in a supported browser.
Allow camera access.
FaceMesh analyzes facial landmarks in real time.
The application estimates the patient's distress level.
Capture symptoms using:
Voice input
Manual text entry
Click Submit.
A JSON packet is sent to the clinic hub.
JSON Payload Example
{
  "timestamp": "2026-08-05T15:30:12Z",
  "distress_level": "MEDIUM",
  "symptoms": "Patient reports chest pain and dizziness."
}
Project Structure
ArogyaSetu-Mobile-Node/
│
├── index.html        # Complete application
└── README.md
Browser Requirements
Google Chrome (Recommended)
Microsoft Edge
Any Chromium-based browser

The application requires:

Camera Permission
Microphone Permission (for speech recognition)
Libraries Used
MediaPipe FaceMesh
MediaPipe Camera Utils
Web Speech API
Fetch API
Use Cases
Rural healthcare centers
Primary health clinics
Mobile health screening
Emergency patient triage
Community health camps
Future Enhancements
AI-based facial emotion classification
Offline data synchronization
Multi-language speech recognition
Patient history management
Secure authentication for healthcare workers
Cloud dashboard integration
License

This project is intended for educational and research purposes. It can be extended and integrated into larger healthcare systems for further development.
