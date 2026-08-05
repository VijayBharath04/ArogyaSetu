ArogyaSetu Mobile Node — Nurse Interaction Tool
ArogyaSetu Mobile Node is a lightweight, single-file static web UI that runs in the browser and provides on-device face-distress detection (using MediaPipe FaceMesh) and speech-to-text symptom capture. It packages a simple workflow for a nurse or frontline worker to capture a heuristic distress level plus spoken/typed symptoms and transmit a JSON payload to a clinic hub endpoint.

Stack
Language(s): HTML (single-page)
Framework / runtime: Browser (vanilla JS)
Notable libraries / browser APIs:
@mediapipe/face_mesh (FaceMesh model via CDN)
@mediapipe/camera_utils (camera helper)
Web Speech API (SpeechRecognition)
Fetch API (POST to server)
What it does (high level)
Runs the MediaPipe FaceMesh on-device to compute a small facial landmark heuristic (distance between eyebrow and eye points) and maps it to LOW / MEDIUM / HIGH distress.
Provides a speech-record button (Web Speech API) to capture symptoms as text into a textarea, or allows manual typing.
Sends a JSON packet containing timestamp, distress_level, and symptoms to the configured backend endpoint.
