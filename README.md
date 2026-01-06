# ATLAS-basic-particle-search-workflow

![Python](https://img.shields.io/badge/Python-f1dc00.svg) ![Pandas](https://img.shields.io/badge/Library-Pandas-1c0055.svg) ![NumPy](https://img.shields.io/badge/Library-NumPy-71a5d3.svg) ![SciPy](https://img.shields.io/badge/Library-SciPy-3943ad.svg) ![Matplotlib](https://img.shields.io/badge/Library-Matplotlib-edb066.svg)

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
