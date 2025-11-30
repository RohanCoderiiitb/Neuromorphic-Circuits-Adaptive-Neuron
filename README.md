# 🧠 Adaptive LIF Neuron With Disease Modelling  
*A hardware-realistic neuromorphic neuron with spike-frequency adaptation and biologically grounded dysfunction models.*

> **Authors:** Vedant Mundada, Rohan Kamath, Heer

---

## 🚀 Overview  
NeuroSync implements a **biophysically inspired Leaky-Integrate-and-Fire (LIF) neuron** extended with a **self-inhibiting RC adaptation mechanism**.  
The goal: build an analog neuron whose firing behaviour resembles real neural tissue — including **adaptation**, **aging**, and **disease states**.

The project also models the effects of:
- **Physiological aging**
- **Early Alzheimer's (Amyloid-β disruption)**
- **Epileptic hyperexcitability**

All simulations are implemented using **LTSpice**, designed to mimic biological electrophysiology using CMOS-like transistor behaviour.

---

## 🧬 Key Features

### 🔹 1. Biologically Inspired LIF Core  
A transistor-level LIF neuron that captures:
- Sodium channel excitation  
- Potassium-driven repolarization  
- After-hyperpolarization (AHP)  
- Threshold-based spiking

---

### 🔹 2. RC-Based Spike Frequency Adaptation  
A slow **Radapt–Cadapt** feedback network:
- Stores charge after each spike  
- Decays exponentially over time  
- Acts as a self-inhibiting current  
- Gradually increases inter-spike intervals  

This mirrors real **neural fatigue** and **self-regulation** observed in biological neurons.

---

### 🔹 3. Disease & Aging Simulation  
The neuron model is extended to emulate realistic changes seen in neurological states:

#### 🧓 Aged Neuron
- Reduced sodium channel availability  
- Weaker AHP reset  
- Linear, metronome-like firing patterns

#### 🧠 Early Alzheimer’s  
- SK channel suppression / internalization  
- Loss of intrinsic adaptation  
- High-frequency tonic firing (~198 Hz)

#### ⚡ Epilepsy  
- Breakdown of stabilizing M-current  
- Runaway depolarization  
- Hyperexcitability leading to depolarization block (~455 Hz)

---

## 📊 Results Summary  

| Model | Firing Rate (Hz) |
|-------|------------------|
| Young | **23.33** |
| Aged | **106.67** |
| Alzheimer’s | **198.33** |
| Epilepsy | **455.00** |

Visual analyses also illustrate:
- Healthy neurons exhibiting strong logarithmic adaptation  
- Aged neurons losing AHP depth and becoming easily re-excitable  
- Alzheimer neurons firing continuously in panic mode  
- Epileptic neurons showing extreme hyperexcitability with voltage plateaus

---

## 🛠 Simulation Details  

- **Software:** LTSpice XVII  
- **Primary Files:**  
  - `Adaptation_rohan_final.asc` – Adaptive neuron with RC inhibition  
  - `Alzheimer's.asc` – Model for Alzheimer-type hyperactivity  
  - `Epilepsy.asc` – Epileptic neuron with suppressed M-current  
- **Devices:** Default LTSpice NMOS/PMOS  
- **Input:** Current-pulse excitation to trigger spiking  
- **Output Measurements:** Membrane voltage, firing rate, inter-spike intervals  

---

## 🌟 Acknowledgements  
Built with guidance from **IIITB ECE Department**, combining neuromorphic engineering with biological modeling.

---

## 🤝 Contributions  
Contributions, discussions, and feature suggestions are welcome!  
Feel free to open issues or submit pull requests.
