<div align="center">

# 🌍 Environmental Kuznets Curve (EKC) Analysis for India 🇮🇳

**An empirical time-series investigation of income growth, energy structure, and CO₂ emissions in India using ARDL and UECM models**

---

[![GitHub](https://img.shields.io/badge/GitHub-Repository-blue?style=flat&logo=github)](https://github.com/yourusername/ekc-india)
[![License](https://img.shields.io/badge/License-MIT-green.svg)](LICENSE)
[![Python](https://img.shields.io/badge/Python-3.8%2B-blue?logo=python)](https://www.python.org/)
[![R](https://img.shields.io/badge/R-4.0%2B-276DC3?logo=r)](https://www.r-project.org/)

</div>

---

## 📌 Introduction

This repository contains an econometric study of the **Environmental Kuznets Curve (EKC) hypothesis** for India.

The EKC hypothesis proposes a **nonlinear (inverted-U) relationship** between economic growth and environmental degradation.

### 🔍 Research Focus

Given India's rapid economic growth and evolving energy mix, this study examines:

- **GDP per capita** and **CO₂ emissions per capita**
- Long-run vs short-run income–emissions dynamics
- The role of renewable energy in emissions mitigation

### 🛠️ Methodology

To ensure econometric validity for trending time-series data, the analysis employs:
- **ARDL** (Autoregressive Distributed Lag) framework
- **UECM** (Unrestricted Error Correction Model)

---

## 📊 Results: ARDL and UECM

### 📈 Long-Run ARDL Estimates

The optimal specification selected using the **Akaike Information Criterion (AIC)** is **ARDL(1,1)**.

| Variable | Coefficient | p-value | Interpretation |
|:---------|------------:|--------:|:---------------|
| ln(GDP per capita)ₜ | +0.152 | 0.011 | Income growth increases emissions |
| ln(GDP per capita)ₜ₋₁ | −0.113 | 0.061 | Nonlinear income effect (marginally significant) |
| ln(CO₂ per capita)ₜ₋₁ | +0.928 | <0.001 | Strong emissions persistence |

> **💡 Key insight:**  
> Although coefficient signs are consistent with EKC-type nonlinearity, the implied turning point lies far beyond India's current income level, indicating that emissions continue to rise with growth in the observed range.

---

### ⚡ Short-Run UECM Dynamics

| Variable | Coefficient | p-value | Interpretation |
|:---------|------------:|--------:|:---------------|
| Error Correction Term (ECT) | −0.092 | 0.062 | Slow adjustment to long-run equilibrium (~9% per year) |
| Δ ln(GDP per capita) | +0.140 | 0.022 | Short-run growth increases emissions |
| Δ Renewable energy share | −0.949 | 0.208 | Negative but statistically insignificant |

> **📊 Analysis:**  
> The negative ECT confirms a stable long-run relationship, while short-run dynamics show that income growth remains emissions-increasing.

---

## 🧪 Test Scores & Diagnostics

### 🔬 ADF Unit Root Tests

| Variable | Status | p-value | Integration Order |
|:---------|:-------|--------:|:------------------|
| ln(CO₂ per capita) | Non-stationary | 0.86 | I(1) |
| ln(GDP per capita) | Non-stationary | 0.99 | I(1) |
| Renewable energy share | Stationary | 0.014 | I(0) |

**Integration Order:** Mixed I(0) / I(1) → **ARDL appropriate**

### 🎯 Model Performance

| Metric | Value |
|:-------|------:|
| **ARDL AIC** | −184.13 |
| **UECM AIC** | −182.07 |
| **Cointegration Evidence** | ✅ Negative ECT confirms long-run equilibrium |
| **Residual Diagnostics** | ✅ No evidence of serial correlation or instability |


<p align="center">
  <img src="docs/results_notbooklm.png" width="700" />
</p>

---

## 📌 Conclusions

### 🔑 Key Findings

Based strictly on the empirical findings:

1. **📈 Income–Emissions Relationship**  
   Economic growth in India increases CO₂ emissions in both the short and long run.

2. **🔄 EKC Hypothesis Status**  
   While EKC-consistent nonlinearity is present, the turning point is far beyond current income levels.

3. **🔒 Structural Inertia**  
   Emissions exhibit strong persistence, indicating structural inertia in the economy.

4. **🌱 Renewable Energy Impact**  
   Renewable energy expansion has not yet reached a scale sufficient to generate statistically detectable long-run emission reductions.

5. **⚠️ Growth Limitations**  
   Income growth alone cannot deliver environmental improvement without targeted energy and climate policy.

---

### 🎯 Policy Implication

> **⚡ Critical Takeaway:**  
> Waiting for growth-driven "automatic decoupling" is unrealistic; **deliberate energy transition policies are required**.

---

### 📚 Documentation

Detailed documentation will be added in the `/docs` directory, including:

- ✅ Data sources & preprocessing
- ✅ Variable construction
- ✅ Model specification choices
- ✅ Robustness checks

---

## 📚 References & Data Sources

### 📊 Data

- [World Bank – World Development Indicators (WDI)](https://databank.worldbank.org/source/world-development-indicators)
- [Our World in Data – Energy & Emissions](https://ourworldindata.org/energy)

### 📖 Key Literature

- **Pesaran, M. H., Shin, Y., & Smith, R. J. (2001)**  
  "Bounds testing approaches to the analysis of level relationships"  
  *Journal of Applied Econometrics*, 16(3), 289-326.

- **Grossman, G. M., & Krueger, A. B. (1995)**  
  "Economic growth and the environment"  
  *The Quarterly Journal of Economics*, 110(2), 353-377.

---

## 👨‍💻 Contact

**Shubhansh Sharma**
this research was done for my learning purpose only. Any advice and contribution from your side will be higly appreciated.

- 📧 **Email:** [shubhanshsharma030604@gmail.com]
---

<div align="center">

### 🌟 If you found this research useful, please consider starring the repository!


</div>
