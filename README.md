# Acoustic Characterisation of UAV Propeller Noise

**Author:** Isha Kulshrestha  
**Affiliation:** B.Sc. (Hons) Physics, Lovely Professional University  
**Internship:** NIT Calicut Summer Internship Programme (SIP) 2026  
**Supervisor:** Dr. T. J. S. Jothi, Department of Physics, NIT Calicut  


---

## Overview

This repository contains the complete code, data processing pipeline, and analysis for the acoustic characterisation of a small UAV propeller across an RPM range of 2250–5700 RPM.

The project:
- Processes `.lvm` files recorded from a National Instruments DAQ system
- Computes FFT-based spectra and extracts the fundamental BPF (H1) and its harmonics (H2, H3)
- Analyzes Sound Pressure Level (SPL) trends at each harmonic
- Implements and compares Linear Regression models for RPM estimation using different feature sets:
  - **H1 only** (baseline)
  - **H1 + H3** (4 features)
  - **H1 + H2 + H3** (6 features)
- Evaluates models using Leave-One-Out Cross-Validation (LOO-CV)
- Extrapolates BPF and SPL to 10,000 RPM


## Dependencies

- Python 3.11+
- NumPy
- SciPy
- Matplotlib
- Pandas
- Scikit-learn

Install with:

```bash
pip install numpy scipy matplotlib pandas scikit-learn