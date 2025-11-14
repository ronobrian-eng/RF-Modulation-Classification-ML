# RF-Modulation-Classification-ML

## 📘 Overview
This project implements a **software-only RF modulation classification system** in **MATLAB**.  
It generates several digital modulation schemes (BPSK, QPSK, 8PSK, 16QAM), passes them through an AWGN channel, extracts RF-inspired features from the complex baseband signal, and trains a **multi-class SVM classifier** to recognise the modulation type.

The goal is to demonstrate practical RF signal processing + machine learning skills in a compact, portfolio-ready project.

---

## ⚙️ Features

### 🔹 Modulation Schemes
- **BPSK**
- **QPSK**
- **8PSK**
- **16QAM**

### 🔹 Signal Processing Chain
- Random symbol generation for each modulation type  
- Complex baseband modulation (PSK/QAM)  
- AWGN channel with random SNR per example  
- Feature extraction from the received complex samples:
  - Variance of I component  
  - Variance of Q component  
  - Mean magnitude  
  - Mean squared magnitude (power)  
  - Kurtosis of magnitude  

### 🔹 Machine Learning
- Dataset built from many labelled examples across modulations
- Train/test split (70% / 30%)  
- **Multi-class SVM** classifier using `fitcecoc`  
- Overall accuracy printed in the MATLAB command window  
- Confusion matrix visualisation for performance analysis  

---

## 🧩 File Summary

| File / Folder | Description |
|---------------|-------------|
| `modulation_classification_project.m` | Main MATLAB script (signal generation + feature extraction + ML) |
| `figures/` | Folder containing exported plots |
| `figures/q1.png` | Constellation plots for BPSK, QPSK, 8PSK, 16QAM |
| `figures/q2.png` | QPSK magnitude vs time and spectrum |
| `figures/q3.png` | Feature space scatter (mean magnitude vs kurtosis) |
| `figures/q4.png` | Confusion matrix of predicted vs true modulation class |

---

## 🧪 Tools & Environment

- **MATLAB** (tested with R2024b)  
- Recommended Toolboxes:
  - **Communications Toolbox** (for `pskmod` / `qammod`)
  - **Statistics and Machine Learning Toolbox** (for `fitcecoc`, `confusionchart`)

---

## 📊 Results

### 1️⃣ Constellation Plots (q1.png)
Shows the noisy constellations for BPSK, QPSK, 8PSK, and 16QAM, giving a visual feel for symbol clustering and decision regions under AWGN.

### 2️⃣ Time & Spectrum for QPSK (q2.png)
Displays the magnitude of a QPSK signal over time and its spectrum, illustrating bandwidth and energy distribution in frequency.

### 3️⃣ Feature Space (q3.png)
Plots **mean magnitude vs kurtosis** of the received signals, coloured by modulation class.  
This makes it clear how RF/statistical features separate BPSK, PSK, and QAM constellations.

### 4️⃣ Confusion Matrix (q4.png)
The confusion matrix summarises classifier performance across all four classes and highlights any confusion between similar schemes (e.g., 8PSK vs QPSK).

---

## ▶️ How to Run

1. Open MATLAB.  
2. Set this folder as the **Current Folder**.  
3. Open `modulation_classification_project.m`.  
4. Click **Run** or press `F5`.  
5. The script will:
   - Generate the dataset  
   - Train the SVM classifier  
   - Print accuracy in the command window  
   - Produce four figures (`q1`–`q4`) which you can save into the `figures/` folder.

---

## 📡 Applications

- RF spectrum monitoring and signal identification  
- Cognitive radio and dynamic spectrum access  
- Wireless communication education (modulation recognition)  
- RF + ML portfolio work for telecom / 5G / SDR roles  

---

## 👤 Author

**Brian Rono**  
Electrical & Computer Engineer • RF & Wireless • Embedded Systems • Machine Learning  
🔗 [GitHub Profile](https://github.com/ronobrian-eng)
