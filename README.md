# PyDIPS: Python Digital Intrusion Prevention Suite

## Project Overview
PyDIPS is an end-to-end, machine learning-powered network security framework designed to act as an Intrusion Detection and Prevention System (IDS/IPS). The suite provides a complete engineering pipeline: sniffing raw network traffic, logging data, training an artificial intelligence network on traffic features, simulating common attack vectors, and executing automated live detection to isolate anomalous network threats.

---

## 📂 Repository Architecture & Core Components

### 1. Technical Documentation & Models
* **Project Report:** Full engineering breakdown detailing packet features, model architecture, and defensive accuracy scores: [ReportPYDIPS.pdf](ReportPYDIPS.pdf)
* **Trained ML Model:** The serialized, production-ready network security model weights: [network_defense_model.pkl](network_defense_model.pkl)
* **Dataset:** Compiled network traffic captures used for feature engineering and model training: [traffic_data.csv](traffic_data.csv)

### 2. The Defensive Software Pipeline
To demonstrate the full machine learning lifecycle, the software architecture is organized into sequentially executed modules:

* **Step 1: Ingestion & Data Harvesting**
  Monitors raw network sockets to sniff packets and harvest structural feature data for local database logging:
  [1. Sniffer to harvest data for database.py](1.%20Sniffer%20to%20harvest%20data%20for%20database.py)

* **Step 2: Validation & Stress Testing**
  Simulates controlled network attack vectors to generate anomalous data footprints and evaluate system response:
  [2. Attack simulator.py](2.%20Attack%20simulator.py)

* **Step 3: Intelligence & Model Training**
  Processes harvested CSV traffic history and trains an intelligence layer to map safe vs. anomalous behavioral boundaries:
  [3. AI Trainer.py](3.%20AI%20Trainer.py)

* **Step 4: Live Interception & Prevention**
  The operational core engine that monitors active network interfaces, loads the trained intelligence model, and intercepts unauthorized vectors in real time:
  [4. Final Detection System.py](4.%20Final%20Detection%20System.py)

---

## ⚡ Technical Highlights & Implementation
* **Full-Lifecycle ML Pipeline:** Demonstrates engineering mastery across data collection (packet sniffing), dataset creation, model training, and active hardware-level deployment.
* **Network Behavior Profiling:** Extracts protocol features dynamically to differentiate standard operations from synthetic attack vectors.
* **Modular Infrastructure:** Designed as isolated, clean scripts allowing separate testing of data harvesting, threat simulation, and active intrusion defense engines.
