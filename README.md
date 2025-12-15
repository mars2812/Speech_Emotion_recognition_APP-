#  Speech Emotion Recognition (SER)

A **Speech Emotion Recognition (SER)** web application built using **Deep Learning**, **TensorFlow/Keras**, and **Streamlit**. This project analyzes speech audio and predicts the underlying human emotion using a trained neural network model.

---

##  Project Overview

This application allows users to:

* Upload or record speech audio
* Extract **Mel Spectrogram** features
* Predict emotional states such as **happy, sad, angry, calm, fear**, etc.
* Visualize prediction probabilities
* Use a simple **login system** backed by SQLite

The project is designed for educational and demonstration purposes in the field of **Speech Processing** and **Affective Computing**.

---

##  Supported Emotions

The trained model predicts the following emotions:

* Angry
* Calm
* Disgust
* Fear
* Happy
* Neutral
* Sad
* Surprised

---

## Model Details

* **Model type:** Convolutional Neural Network (CNN)
* **Framework:** TensorFlow / Keras
* **Input:** Log-Mel Spectrogram (128 × 128)
* **Model file:** `speech_emotion_recognition_model.h5`

---

##  Project Structure

```
SER MODEL/
│
├── app.py                          # Streamlit web application
├── speech_emotion_recognition_model.h5   # Trained SER model
├── SER.db                          # SQLite database (users)
├── SER-Matrika.db                  # Additional database
├── requirement.text                # Project dependencies
├── temp.wav                        # Temporary audio file
├── block.jpg                       # UI image asset
├── speech.jpg                      # UI image asset
├── env/                            # Virtual environment (optional)
└── team/                           # Team-related files
```

---

##  Installation & Setup

### 1️⃣ Clone or Extract the Project

```bash
git clone <repository-url>
cd SER-MODEL
```

Or extract the provided ZIP file.

---

### 2️⃣ Create a Virtual Environment (Recommended)

```bash
python -m venv env
source env/bin/activate      # Linux / macOS
env\Scripts\activate         # Windows
```

---

### 3️⃣ Install Dependencies

```bash
pip install -r requirement.text
```

**Main Libraries Used:**

* streamlit
* librosa
* numpy
* matplotlib
* tensorflow
* scikit-learn
* sqlite3

---

##  Running the Application

Start the Streamlit app using:

```bash
streamlit run app.py
```

Then open your browser and go to:

```
http://localhost:8501
```

---

## Authentication System

* The app includes a **login & registration system**
* User credentials are stored securely in **SQLite (`SER.db`)**
* Session handling is managed using Streamlit session state

---

## How It Works

1. User uploads or records audio
2. Audio is processed using **Librosa**
3. Log-Mel Spectrogram is extracted
4. Spectrogram is fed into CNN model
5. Model outputs emotion probabilities
6. Results are visualized using bar charts

---

##  Visualization

* Emotion probabilities are displayed as a **bar chart**
* The highest probability emotion is shown as the prediction

---

##  Datasets Used (Training Phase)

Although not included in this repository, the model was trained using popular SER datasets such as:

* RAVDESS
* CREMA-D
* TESS

*(Datasets were combined and label-encoded during training)*

---

##  Known Limitations

* Works best with clean, short audio samples
* Background noise may affect predictions
* Model performance depends on microphone quality

---

##  Future Improvements

* Real-time emotion detection
* Noise reduction preprocessing
* More emotions & multilingual support
* Model performance optimization
* Improved UI/UX

---

## 👥 Team

Project developed by the **Matrika Dhamala and his Team** as part of an academic / learning initiative.

---

##  License

This project is intended for **educational use only**.

---

##  Contact

For questions or improvements, feel free to reach out to the project contributors.

---

⭐ *If you find this project useful, consider giving it a star!*
