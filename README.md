# 🩺 Medical Recommendation System

This project is a **Virtual Healthcare Recommendation System** built using a **Support Vector Classifier (SVC)** model, deployed via a responsive **Flask web application**. It allows users to input symptoms (via text or voice) and returns accurate disease predictions along with complete treatment guidance.

---

## 🔍 Table of Contents

- [Demo](#-demo)
- [Features](#-features)
- [System Architecture](#-system-architecture)
- [Machine Learning Model](#-machine-learning-model)
- [Datasets Used](#-datasets-used)
- [Application Workflow](#-application-workflow)
- [Installation & Usage](#-installation--usage)
- [Project Structure](#-project-structure)
- [Limitations](#-limitations)
- [Future Work](#-future-work)
- [License](#-license)

---

## 🚀 Demo

> **Live Demo:** https://healthcare-d7vz.onrender.com/

![](./static/img.png)  
*User-friendly symptom input and prediction interface*

---

## ✨ Features

- Predicts from **133 diseases** using **400+ symptoms**
- Real-time results under **500ms**
- **Multi-modal input**: Text and speech recognition
- Provides:
  - Disease description
  - Medication advice
  - Dietary recommendations
  - Workout suggestions
  - Precautionary tips
- Built using Flask + HTML/CSS (Tailwind)

---

## 🧠 System Architecture

User Input → Preprocessing → SVC Model → Prediction → Knowledge Base Lookup → Output Display

- **Frontend:** HTML + TailwindCSS  
- **Backend:** Python (Flask)  
- **Model:** Scikit-learn SVC  
- **Database:** CSV-based structured knowledge base  

---

## 🧬 Machine Learning Model

- **Model:** Support Vector Classifier (Linear Kernel)
- **Accuracy:** 100% (Validation Data)
- **Input Features:** Binary encoded 400+ symptom vector
- **Multiclass Strategy:** One-vs-Rest
- **Inference Time:** < 500ms

```python
svc = SVC(kernel='linear', C=1.0)
svc.fit(X_train, y_train)
```

---

## 📊 Datasets Used

| Dataset                  | Purpose                    |
|--------------------------|----------------------------|
| `Training.csv`           | Symptom-to-disease mapping |
| `description.csv`        | Disease descriptions       |
| `medications.csv`        | Drug recommendations       |
| `precautions_df.csv`     | Preventive measures        |
| `diets.csv`              | Nutritional plans          |
| `workout_df.csv`         | Exercise suggestions       |
| `Symptom-severity.csv`   | Detailed symptom metadata  |

---

## 🔄 Application Workflow

1. **User enters symptoms** (text/voice)
2. Input is encoded into binary vector
3. **SVC model** predicts likely diseases
4. Top 3 diseases are selected
5. Recommendations (medications, diets, etc.) are retrieved
6. Result is displayed in a clean UI

---

## ⚙️ Installation & Usage

### Prerequisites

* Python 3.8+
* `pip install -r requirements.txt`

### Setup

```bash
git clone https://github.com/your-username/medical-recommendation-system.git
cd medical-recommendation-system
pip install -r requirements.txt
```

### Run Application

```bash
python main.py
```

Visit `http://127.0.0.1:5000/` in your browser.

---

## 📁 Project Structure

```
MedicalRecommendationSystem/
│
├── datasets/
│   ├── Training.csv
│   ├── description.csv
│   ├── medications.csv
│   ├── diets.csv
│   ├── precautions_df.csv
│   ├── workout_df.csv
│   ├── Symptom-severity.csv
│   ├── symtoms_df.csv
│
├── templates/
│   ├── index.html
│   ├── about.html
│   ├── blog.html
│   ├── contact.html
│   ├── developer.html
│
├── static/
│   ├── img.png
│
├── models/
│   ├── svc.pkl
│
├── main.py
├── requirements.txt
├── README.md
```

---

## ⚠️ Limitations

* Covers only 133 diseases
* Needs formal clinical validation for medical use
* Speech input varies in accuracy by accent

---

## 🧭 Future Work

* Add 200+ more diseases and symptoms
* Support for regional languages
* Mobile and wearable device integration
* Drug interaction checker
* Electronic Health Record (EHR) compatibility

---

## 📜 License

This project is licensed under the MIT License. See `LICENSE` for more information.

---

> Developed with ❤️ by **Ayush Kumar Jha**
