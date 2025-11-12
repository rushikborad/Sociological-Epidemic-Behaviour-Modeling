# 🧠 Sociological-Epidemic-Behaviour-Modelin

![Python](https://img.shields.io/badge/Built%20with-Python-blue)
![License](https://img.shields.io/badge/License-MIT-green)
![SciPy](https://img.shields.io/badge/Powered%20by-SciPy%20%26%20NumPy-orange)
![Status](https://img.shields.io/badge/Status-Research%20Project-lightgrey)

---

## 📘 Overview

**Sociological-Epidemic-Behaviour-Modelin** is a computational research project that explores how **social awareness and behavioral interactions** influence **epidemic spread dynamics**.

This work extends the classical **SIR (Susceptible–Infected–Recovered)** model by introducing **sociological feedback mechanisms** that dynamically modify infection rates based on awareness and inter-group influence.

---

## 🎯 Objectives

- Build a **two-layer behavioral–epidemic system**.
- Compare outcomes between the **classical SIR model** and the **extended sociological model**.
- **Optimize parameters** (`β`, `γ`, `θ₁`, `θ₂`) to minimize the deviation between both systems.
- **Visualize** epidemic and behavioral dynamics through plots and heatmaps.

---

## 🧩 Model Description

### 1️⃣ Classical SIR Model

The **SIR model** divides the population into three compartments:

- **S** — Susceptible  
- **I** — Infected  
- **R** — Recovered  

Equations:

\[
\frac{dS}{dt} = -\beta S I
\]

\[
\frac{dI}{dt} = \beta S I - \gamma I
\]

\[
\frac{dR}{dt} = \gamma I
\]

---

### 2️⃣ Sociological Interaction Model

This extended model divides the population into two interacting groups with their own compartments:

- \(S_1, S_2\) — Susceptible  
- \(I_1, I_2\) — Infected  
- \(R_1, R_2\) — Recovered  

It introduces **awareness parameters** (`θ₁`, `θ₂`) that adjust infection rates dynamically:

\[
a_i = \min\left(\max\left(\frac{\theta_i \cdot (I_1 + I_2) \cdot \beta}{2}, 0\right), 1\right)
\]

This represents how **increased infection awareness reduces susceptibility** within each social group.

---

## ⚙️ Features

✅ SIR baseline simulation  
✅ Dual-population sociological model  
✅ Parameter optimization using `scipy.optimize.minimize`  
✅ Error heatmaps comparing both models  
✅ R² score evaluation for model fitting  
✅ Comprehensive time-evolution and comparison visualizations  

---

## 📈 Visualizations

The project generates:

- 📊 **Time-evolution plots** for S, I, R (both models)
- 🔄 **Model comparison plots** between SIR and sociological model
- 🌡️ **Error heatmaps** across parameter grids (`β`, `γ`, `θ₁`, `θ₂`)
- 📉 **R² score trend plots**
- 📦 **Histogram** of model fitting errors

---

## 🧮 Dependencies

Make sure you have the following Python packages installed:

```bash
pip install numpy scipy matplotlib scikit-learn
