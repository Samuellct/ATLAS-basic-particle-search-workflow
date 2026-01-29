# ATLAS-basic-particle-search-workflow

![Python](https://img.shields.io/badge/python-ffdd54?logo=python&logoColor=4f68a8) ![Pandas](https://img.shields.io/badge/pandas-%23150458.svg?logo=pandas&logoColor=white) ![NumPy](https://img.shields.io/badge/numpy-%23013243.svg?logo=numpy&logoColor=white) ![Scipy](https://img.shields.io/badge/SciPy-%230C55A5.svg?logo=scipy&logoColor=white) ![Matplotlib](https://img.shields.io/badge/Matplotlib-%23e5e5e6?logo=data:image/png;base64,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) 

## Overview
This repository contains the analysis framework developed by my partner and me during our L3 Physics IMAPP Data Analysis course at Université Clermont Auvergne. The project was designed as a "blind search" for a Beyond the Standard Model (BSM) particle, the **X boson**, using simulated High-Luminosity LHC data.

The mission was to build a selection pipeline to filter out the Standard Model background and extract any potential resonance in the diphoton channel ($X \rightarrow \gamma\gamma$). Our work followed a standard experimental procedure: defining an optimal selection on training samples before applying it on our assigned dataset (`data_4`).

## The Physics Case
In a hadron collider like the LHC, we don't measure the invariant mass directly. We detect the energy and position of particles. For two massless particles like photons, the invariant mass $m_{inv}$ is reconstructed using their transverse momenta ($p_T$), their pseudorapidity ($\eta$), and their azimuthal angle ($\phi$):

$$m_{inv} = \sqrt{2p_{T1}p_{T2}(\cosh(\eta_1-\eta_2)-\cos(\phi_1-\phi_2))}$$

A new particle would appear as a narrow Gaussian peak. In this project, the theoretical mass of the X boson was expected to be between 500 and 1000 GeV.

## Analysis Methodology
Since I already had some experience with Python, the main challenge for us was the physics logic rather than the syntax. The analysis pipeline in this repository isn't built entirely from scratch, it is based on a framework provided by our professor during the lab sessions, which we adapted and optimized for our specific dataset.

### 1. Events selection on training datasets
The primary challenge was to reduce the background while keeping as much signal as possible. We applied several "cuts" on kinematic variables:
- **Acceptance:** Photons were required to be within the detector's central region ($|\eta| < 2.37$).
- **Transverse Momentum:** Keeping only high-energy photons to reduce the low-energy background.
- **Isolation:** Requirements on the energy around the photon to distinguish prompt photons from those coming from hadronic jets.

We measured our progress using the **Sensitivity ($Z$)** metric. Before any cuts, the initial sensitivity on the raw data was **3.24** and focusing on the invariant mass window of **[400; 1100] GeV**, we successfully increased the sensitivity to **5.53**. By refining our selection we managed to increase the sensitivity up to **10.19**.

### 2. Application to Observed Data (data_4)
Once our pipeline was ready, we applied it to the **134,926 events** contained in our specific dataset, `data_4`. The goal was to see if the analysis tools developed in Phase 1 would reveal an excess. In the [400; 1100] GeV window, we had to filter a massive background. After our selection, we estimated the background in the signal region to be **4129 $\pm$ 118 events**.

## Statistical Results
To quantify what we found in `data_4`, we used two main metrics:

1. **Significance ($s$):** After filtering, our dataset yielded a significance of only **0.5 $\sigma$**. In particle physics, this is far below the $5\sigma$ threshold required for a discovery, indicating that our data is perfectly consistent with the Standard Model background.
2. **Signal Strength Index ($\mu$):** We used the **CLs method** to set an upper limit on the signal. We found an upper limit of **0.3736 $\mu$**.

## Conclusion
The nominal theoretical cross-section for the X boson is **5.4 pb** (corresponding to $\mu=1$). Our observed limit of $0.3736 \mu$ means the signal in our data corresponds to an effective cross-section of only **2.01744 pb**. This result clearly shows that the X boson, was not present in our dataset.

## Academic Context
Following the standards of the ATLAS collaboration, we produced a final report using **LaTeX**. We aimed to match the official CERN-ATLAS publication style, including a formal abstract and a detailed description of the detector and statistical methods used.
