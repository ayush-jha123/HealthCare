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
Video Link:https://drive.google.com/file/d/1GJwinesYZ1jdW5plxTEzf7leL_TJbNPL/view?usp=drivesdk
## 🚀 Demo

> **Live Demo:** https://healthcare-d7vz.onrender.com/

![](./screenshots/interface.png)  
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

```plaintext
User Input → Preprocessing → SVC Model → Prediction → Knowledge Base Lookup → Output Display
