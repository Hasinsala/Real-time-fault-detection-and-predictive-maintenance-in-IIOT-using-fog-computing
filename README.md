Dataset-> https://www.kaggle.com/datasets/sujaykapadnis/ball-bearing-run-to-failure-dataset?resource=download




# 🔧 Real-Time Fault Detection & Predictive Maintenance in IIoT Using Fog Computing

## 🛰️ Project Overview

This project presents a real-time fault detection and predictive maintenance system for Industrial IoT (IIoT) environments, specifically targeting **ball bearing failure** in rotating machinery. By leveraging **fog computing** with **Raspberry Pi edge nodes**, the system performs intelligent predictions near the data source, reducing latency and enhancing reliability.

We use a time-series dataset of bearing vibration signals to build a deep learning model based on **Long Short-Term Memory (LSTM)** for Remaining Useful Life (RUL) prediction. This model is deployed on a **Raspberry Pi** edge device to provide real-time insights and failure alerts, enabling proactive maintenance.

---

## 📦 Features

- ✅ Real-time bearing fault detection
- 📈 LSTM-based Remaining Useful Life (RUL) prediction
- 🌐 Edge computing using Raspberry Pi (Fog Node)
- ☁️ Optional cloud sync for visualization and long-term analytics
- 🔍 Scalable to other industrial machinery components
- ⚠️ Early alert system before physical bearing damage
- 🛠️ Enhancement ideas: Explainability (SHAP), Autoencoder, Edge TPU integration

---

## 🧠 Dataset Description

- **Source**: Time-series data from industrial bearings
- **Samples**: 128 hourly CSV files
- **Features**:
  - Vibration signals (x, y, z)
  - Acoustic or voltage readings (if available)
- **Labels**: No direct labels; RUL derived from failure timeline

---

## 🏗️ Tech Stack

| Layer               | Tools / Technologies                  |
|--------------------|----------------------------------------|
| Data Processing     | Python, Pandas, Numpy                  |
| ML Modeling         | TensorFlow / PyTorch (LSTM)           |
| Edge Deployment     | Raspberry Pi, TensorFlow Lite         |
| IIoT Communication  | MQTT, Flask, HTTP                     |
| Cloud Dashboard     | AWS / Firebase / Node-RED / Grafana   |
| Explainability      | SHAP (optional)                       |
| Hardware (optional) | Vibration sensors, Temp sensors       |

---

## 🔁 DevOps Integration (CI/CD + Containerization)

To ensure reliability, automation, and scalability, DevOps practices are integrated into our project pipeline.

### 🧰 Tools & Practices Used

| Category              | Tools / Technologies                         |
|------------------------|-----------------------------------------------|
| Version Control        | Git + GitHub                                  |
| CI/CD Pipeline         | GitHub Actions *(for testing, model build)*   |
| Containerization       | Docker *(for preprocessing, model inference)* |
| Edge Deployment        | SCP + shell scripts for remote model updates  |
| Infrastructure as Code | Ansible *(optional, for Pi setup)*            |
| Monitoring             | Prometheus + Grafana *(optional)*             |

### 🛠️ Docker Setup

Key parts of the application are containerized:

- Data Preprocessing
- LSTM Model Training & Inference
- Flask API for real-time predictions

```bash
# Build and run container
docker build -t bearing-failure-detector .
docker run -p 5000:5000 bearing-failure-detector
