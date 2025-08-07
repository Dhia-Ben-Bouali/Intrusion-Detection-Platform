# 🛡️ Intrusion-Detection-Platform

An intelligent, ML-based intrusion detection platform deployed in a virtualized environment. It integrates classic network security tools like **pfSense**, **Snort**, and **Wazuh SIEM**, with **machine learning models** for enhanced detection of intrusions and phishing attacks.

## 📌 Overview

This project demonstrates a security monitoring environment that detects:

- **Network intrusions** via real-time PCAP analysis from Snort
- **Phishing emails** using content-based ML classification

All components work together to create a responsive and intelligent threat detection system.

---

## 🧱 Architecture

The platform is deployed in a **virtualized lab setup** consisting of:

- **pfSense firewall** with **Snort IDS** installed
- **Two LAN machines** configured with local **email services**
- **Wazuh SIEM** to monitor system events and forward suspicious emails
- A central **ML-based Intrusion Detection Platform**

---

## 🤖 Machine Learning Models

### 1. Intrusion Detection System

- **Dataset**: NSL-KDD
- **Algorithm**: Classification (e.g., RandomForest, DecisionTree, etc.)
- **Functionality**:
  - Snort generates PCAP files at regular intervals
  - PCAP files are sent to the ML platform
  - The model analyzes each packet/flow to detect normal vs anomalous traffic

### 2. Phishing Detection System

- **Dataset**: Phishing Email Dataset (Kaggle)
- **Algorithm**: XGBoost Classifier
- **Functionality**:
  - Wazuh detects suspicious emails based on configured rules
  - The platform receives and analyzes the email
  - The model classifies it as phishing or legitimate

---
