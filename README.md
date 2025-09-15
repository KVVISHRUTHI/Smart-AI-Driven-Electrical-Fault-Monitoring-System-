# CogniSense: Smart AI-Driven Electrical Fault Monitoring System

## 🔹 Project Overview
This project implements a smart AI-driven system to monitor electrical faults like earth leakage, continuity, and resistance in real time. It moves beyond traditional, manual checks by using an embedded AI model to predict potential failures, thus preventing safety hazards, equipment failures, and inefficient maintenance.



## 🔹 Features
AI-Driven Prediction: Utilizes a machine learning model for predictive maintenance.

Real-time Monitoring: Continuously analyzes data from sensors for instant fault detection.

Proactive Alerts: Provides actionable alerts and insights to prevent failures before they occur.

User Interface: A web-based UI for real-time monitoring and reporting.

Scalable Design: The system can be expanded to monitor multiple circuits and larger infrastructures.

Cost & Safety: Reduces maintenance costs and enhances safety by preventing electrical hazards.



## 🔹 System Architecture
```
[Electrical Panel/Circuit]
        ↓ (Sensors: ACS712, etc.)
[ Microcontroller (ESP32) ]
        ↓ (Wired/Wireless)
[ Raspberry Pi / Mini-PC (Central Hub) ]
        ↓ (AI Model & Dashboard)
[ User (via Web UI) ]


```

## 🔹 Pseudo Code
```Python

Start Central Hub
Initialize sensors and communication (MQTT)
Load pre-trained AI model

Loop (continuously):
    Read data from sensors (current, voltage, etc.)
    Preprocess data for the AI model
    Run data through AI model for anomaly detection
    
    If anomaly detected:
        Generate a "high risk" alert
        Log the event in the database (e.g., SQLite)
        Send an alert to the user's dashboard

    Receive UI requests for historical data
    Display real-time and historical data on the dashboard

End Loop
🔹 Software Stack
Raspberry Pi OS / Linux

Python 3

AI/ML Libraries: Scikit-learn or TensorFlow Lite

Communication: MQTT (e.g., Paho-MQTT)

Backend: Flask / FastAPI

Database: SQLite (local storage)

Frontend: HTML/JS/React (for the UI dashboard)

🔹 References & Research Work
AI & Fault Detection Research:

A study on using machine learning for fault diagnosis in electrical systems.

Research papers on predictive maintenance in electrical power systems.

Technical Libraries & Hardware:

TensorFlow for Anomaly Detection: Guides on using TensorFlow for time-series anomaly detection.

ACS712 Current Sensor: Documentation for commonly used current sensors that can interface with a microcontroller or Raspberry Pi.

Paho-MQTT Python Client: Documentation for the Python MQTT client used for communication between devices.

🔹 Future Enhancements
Incorporate more sensor types (e.g., temperature, humidity) for a more comprehensive analysis.

Develop a mobile application for on-the-go monitoring and alerts.

Implement a user authentication and multi-user system for different roles (e.g., administrator, technician).

Integrate with a notification service (e.g., SMS or email) for critical alerts.

🔹 Team
Hackathon Project by [Cogni Crew]
