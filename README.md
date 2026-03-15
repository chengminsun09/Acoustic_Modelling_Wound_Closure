# Hybrid Fisher–KPP + Agent-Based Model for Wound Closure

This repository contains the code and data used to reproduce the simulations and analyses presented in the manuscript:

**“In Silico Optimization of Time-Dependent Motility and Proliferation Control for Wound Closure: A Hybrid Fisher–KPP and Force-Based Agent Model.”**

The repository provides:

- literature-based wound closure data extraction  
- Fisher–KPP model fitting  
- hybrid PDE–ABM simulation workflow  
- comparison between continuum and hybrid models  
- scripts used to generate figures and numerical analyses  

The code is intended to ensure **computational reproducibility of the modeling results reported in the manuscript.**

---

# Repository Structure


.
├── main.ipynb
├── johnston_data.ipynb
├── johnston2015_rwd_approx.csv
└── README.md


---

# File Description

## main.ipynb

Main notebook used to run the **hybrid PDE–ABM wound closure simulations** and generate the simulation outputs used in the study.

The notebook includes:

- hybrid simulation workflow  
- stochastic ensemble simulations  
- wound closure trajectories  
- parameter exploration  
- generation of simulation figures  

---

## johnston_data.ipynb

Notebook used to process literature wound-healing data from:

**Johnston et al., 2015 – BMC Systems Biology**

This notebook performs:

- loading digitized scratch-assay data  
- Fisher–KPP model fitting  
- hybrid model fitting  
- RMSE comparison between models  
- generation of validation plots  

---

## johnston2015_rwd_approx.csv

Digitized wound closure data extracted from the published figure in:

Johnston ST et al. (2015)  
*Estimating cell diffusivity and cell proliferation rate by interpreting IncuCyte ZOOM™ assay data using the Fisher–Kolmogorov model.*  
**BMC Systems Biology**

Because the original article presents the wound closure curve graphically, the values were extracted by **digitizing the published figure and converting it into tabular form**.

Small digitization errors may therefore be present.

The dataset represents **relative wound density (RWD) vs time** for a representative control-condition scratch assay.

---

# Requirements

The notebooks were tested using **Python 3.10** with the following packages:


numpy
pandas
matplotlib
scipy
seaborn


Install dependencies with:


pip install numpy pandas matplotlib scipy seaborn


---

# Running the Code

## 1. Fit literature data

Run:


johnston_data.ipynb


This notebook:

- loads the digitized dataset  
- fits the Fisher–KPP model  
- fits the hybrid model  
- generates comparison plots  

---

## 2. Run hybrid simulations

Run:


main.ipynb


This notebook performs:

- hybrid PDE–ABM simulations  
- stochastic ensemble runs  
- wound closure trajectories  
- parameter sweeps  
- figure generation  

---

# Reproducibility

The notebooks provide a **compact executable workflow** that reproduces the key analyses of the manuscript, including:

- literature-based model validation  
- hybrid vs Fisher–KPP comparison  
- simulation trajectories  
- parameter exploration  

All simulations are stochastic; results shown in the manuscript are based on **ensemble averages across multiple runs**.

---

# Citation

If you use this code, please cite the associated manuscript:


In Silico Optimization of Time-Dependent Motility and Proliferation Control
for Wound Closure: A Hybrid Fisher–KPP and Force-Based Agent Model


---

# License

This code is provided for academic and research purposes.

---

# Acknowledgment

Literature data used in the validation step originate from:

Johnston ST et al., 2015  
*BMC Systems Biology*
