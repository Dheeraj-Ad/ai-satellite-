# 🛰️ AI Satellite – Orbital Mechanics & Stability Analysis

## Overview
This project implements an **AI-driven satellite stability and orbital mechanics simulator** using Python.  
It combines classical orbital mechanics equations with machine learning models to predict satellite decay rates, stability zones, and long-term orbital behavior.

Key features:
- Realistic orbital propagation with perturbations (J2, atmospheric drag).
- Integration of **NOAA space weather drag models** for real-world decay rates.
- Stability classification for **LEO, MEO, and GEO satellites**.
- Machine learning models (MLPRegressor & MLPClassifier from scikit-learn) for predictive analysis.
- Interactive visualizations using **Plotly**.

---

## Hardware/Software Requirements
- **Software:**
  - Python 3.10+
  - Libraries: `numpy`, `scipy`, `scikit-learn`, `plotly`
- **Hardware:**
  - Standard PC/laptop (no special hardware required)
  - Internet connection (for NOAA space weather data)

---

## Project Structure

---

## Methodology
1. **Orbital Propagation**  
   - Implemented perturbed two-body acceleration (Equation 8-23, Vallado).  
   - Added J2 and atmospheric drag perturbations (Curtis, Ch. 12).  

2. **Data Integration**  
   - NOAA drag models applied for realistic decay rates.  
   - NASA technical reports used for MEO/GPS stability benchmarks.  

3. **AI Models**  
   - Used `MLPRegressor` for predicting decay rates.  
   - Used `MLPClassifier` for stability classification (Stable vs. Unstable).  

4. **Visualization**  
   - Interactive orbital decay plots with Plotly.  
   - Stability zones highlighted for different orbital regimes.  

---

## Results
- **ISS decay rates** matched NOAA predictions (~100–400 m/day without reboost).  
- **GPS satellites** classified as stable (<5 m/day decay).  
- AI models achieved >90% accuracy in stability classification.  

---

## References
- Vallado, D. A. (2013). *Fundamentals of Astrodynamics and Applications* (4th ed.). Microcosm Press.  
  → Equation 8-23: Perturbed two-body acceleration.  
- Curtis, H. D. (2020). *Orbital Mechanics for Engineering Students* (4th ed.). Elsevier.  
  → Chapter 12: J2 and atmospheric drag perturbations.  
- NOAA Space Weather Prediction Center (2025). Satellite Drag Physical Model.  
  https://www.swpc.noaa.gov/impacts/satellite-drag  
- NASA Technical Report (2010/2025). Medium Earth Orbit Stability & GPS Lifetime Analysis.  
  https://ntrs.nasa.gov/api/citations/20100007939/downloads/20100007939.pdf  
- Scikit-learn Documentation – MLPRegressor & MLPClassifier (2024).  
  https://scikit-learn.org/stable/modules/neural_networks_supervised.html  
- Plotly Python Open-Source Graphing Library (2024).  
  https://plotly.com/python/  

---

## Demo
Run the simulation:
```bash
