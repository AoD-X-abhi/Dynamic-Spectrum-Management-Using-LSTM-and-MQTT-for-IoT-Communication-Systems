# 📡 Dynamic-Spectrum-Management-Using-LSTM-and-MQTT-for-IoT-Communication-Systems

[![Python 3.11](https://img.shields.io/badge/Python-3.11-blue.svg)](https://www.python.org/)
[![TensorFlow](https://img.shields.io/badge/TensorFlow-2.x-orange.svg)](https://www.tensorflow.org/)
[![MQTT](https://img.shields.io/badge/MQTT-Paho-green.svg)](https://pypi.org/project/paho-mqtt/)
[![Dataset](https://img.shields.io/badge/Dataset-RadioML_2018.01A-lightgrey.svg)](https://www.kaggle.com/datasets/jrfelix/radioml2018)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

---

## 📖 Executive Summary

This repository presents the simulation of a **Cognitive Radio Network (CRN)** that integrates Deep Learning-based signal classification with dynamic spectrum management within an Internet of Things (IoT) framework. 

The architecture employs a Long Short-Term Memory (LSTM) neural network to accurately classify complex radio signal modulations extracted from the RadioML 2018 dataset. Concurrently, it conducts real-time spectrum sensing utilizing Fast Fourier Transform (FFT) for Power Spectral Density (PSD) analysis. To emulate a distributed IoT environment, the system publishes real-time inference results and dynamic channel allocation metrics to an MQTT broker, demonstrating the practical application of edge-node intelligence in modern telecommunications.

---

## ✨ Core Capabilities

* **Deep Learning Modulation Classification:** Leverages a robust multi-layer LSTM network to classify 8 distinct modulation schemes (`4ASK`, `BPSK`, `QPSK`, `16PSK`, `16QAM`, `FM`, `AM-DSB-WC`, `32APSK`).
* **Real-Time Spectrum Sensing:** Executes precise PSD analysis via FFT to differentiate between occupied and available frequencies across a simulated 64-channel spectrum.
* **Intelligent Channel Allocation:** Integrates a custom algorithmic `SpectrumManager` to dynamically assign available channels based on historical quality metrics and real-time occupancy.
* **IoT/MQTT Telemetry:** Utilizes the `paho-mqtt` protocol to broadcast model training progression (epochs, accuracy) and real-time predictive streams to a centralized or subscriber node.

---

## 🛠️ Technology Stack

* **Programming Language:** Python 3.11
* **Machine Learning & AI:** TensorFlow / Keras, Scikit-Learn
* **Signal Processing & Mathematics:** NumPy, SciPy (FFT)
* **Data Engineering:** Pandas, h5py
* **IoT Messaging Protocol:** Eclipse Paho MQTT (`test.mosquitto.org` test broker)
* **Data Visualization:** Matplotlib

---

## 📂 Repository Architecture

```text
├── mainfinal.ipynb        # Primary Edge Node: Data processing, LSTM architecture, Spectrum Management, and MQTT Publisher
├── subscriberfinal.ipynb  # Observer Node: MQTT Subscriber capturing and formatting real-time network telemetry
└── README.md              # Project documentation
