🎯 Concentration Detection System (OpenCV + MediaPipe)

📌 Overview

This project is a **real-time concentration tracking system** built using computer vision.
It uses a webcam feed to analyze **eye movement, blinking, and head position** to estimate a user's focus level.

The system outputs:

* Concentration score (0–100%)
* Blink detection
* Distraction counter
* Real-time status (ACTIVE / DISTRACTED)

---

🚀 Features

* 👁️ Eye Aspect Ratio (EAR) for blink detection
* 🎯 Gaze tracking using iris landmarks
* 🧠 Head pose estimation (basic)
* 📊 Smoothed concentration score
* ⚠️ Distraction detection logic
* ⚡ Real-time FPS display

---

🛠️ Tech Stack

* Python 3.10
* OpenCV
* MediaPipe
* NumPy
* Matplotlib (optional for future visualization)

---

📂 Project Structure

```
concentration-tracker/
│
├── project.py        # Main application file
├── README.md         # Project documentation
└── requirements.txt  # Dependencies (optional but recommended)
```

---

⚙️ Installation & Setup

1️⃣ Check Python Version

```bash
py -3.10 --version
```

2️⃣ Create Virtual Environment

```bash
py -3.10 -m venv myenv
```
3️⃣ Activate Environment

```bash
.\myenv\Scripts\activate
```
4️⃣ Install Dependencies

```bash
pip install opencv-python mediapipe numpy matplotlib
```

---

▶️ Run the Project

```bash
py project.py
```

Press **'q'** to quit the application.

---

🧠 How It Works

1. Eye Aspect Ratio (EAR)

Detects blinking based on eye landmark distances.

2. Gaze Tracking

Checks whether the user is looking at the center of the screen.

3. Head Pose Score

Measures deviation of the nose from screen center.

4. Concentration Score Formula

```
Score = (0.4 × Gaze) + (0.4 × Head Pose) + (0.2 × Eye State)
```

* Blink → reduces score
* Looking away → reduces score
* Head turned → reduces score

---

⚠️ Limitations (Don’t Ignore This)

* Not accurate in low lighting conditions
* Head pose estimation is **very basic** (not true 3D)
* Gaze tracking is approximate, not precise
* Works best for a single face only
* No calibration per user → results can be inconsistent

If you present this as “accurate AI,” you’ll get called out. Be honest—it’s a **prototype**, not a production system.

---

🔮 Future Improvements

* Add deep learning-based gaze tracking
* Improve head pose using PnP algorithm
* Multi-user detection
* Data logging & analytics dashboard
* Mobile app integration

---

📸 Demo (Optional)

*Add screenshots or demo video here*

---

## 🙌 Acknowledgements

* MediaPipe by Google
* OpenCV community

---

📬 Contact

Add your name / GitHub profile here

---

⭐ Final Note

This project is good for:

* Learning computer vision basics
* Understanding real-time processing
* Building portfolio projects

But don’t overestimate it—this is **entry-level CV work**, not advanced AI.
