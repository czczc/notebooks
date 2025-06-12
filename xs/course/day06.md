# **Day 6: Generator Comparisons, Uncertainties, and Experiment Interface**

---

## **1. Introduction**

This lecture focuses on how different neutrino event generators compare, how uncertainties are estimated and propagated, and how these simulations are integrated into experimental workflows. Understanding this is essential for both designing experiments and interpreting their results.

Goals:

* Compare major neutrino event generators and their modeling differences.
* Explore how cross-section model uncertainties are estimated and managed.
* Understand how generators are tuned and interfaced with data.
* Discuss the impact of generator choices on oscillation and cross-section analyses.

---

## **2. Major Neutrino Event Generators**

### 2.1 Overview

| Generator | Origin  | Used By                     | Features                     |
| --------- | ------- | --------------------------- | ---------------------------- |
| **GENIE** | US      | DUNE, NOvA, MicroBooNE      | Modular, broad energy range  |
| **NEUT**  | Japan   | T2K, Super-K, Hyper-K       | Precision tuned for few-GeV  |
| **NuWro** | Poland  | Theory comparisons          | Lightweight, fast testing    |
| **GiBUU** | Germany | Theory, electron scattering | Transport-based FSI modeling |

Each implements similar channels (QE, RES, DIS, coherent, 2p2h), but with different physics assumptions, nuclear models, and FSI treatments.

---

### 2.2 Key Differences

| Feature       | GENIE                      | NEUT                         | NuWro           | GiBUU               |
| ------------- | -------------------------- | ---------------------------- | --------------- | ------------------- |
| Nuclear model | Global Fermi Gas (default) | Spectral Function (optional) | Local Fermi Gas | Off-shell transport |
| RES model     | Rein–Sehgal                | Rein–Sehgal (tuned)          | Hybrid          | Dynamical           |
| 2p2h          | Valencia (optional)        | T2K fit                      | Empirical       | Microscopic         |
| FSI           | Semi-classical (hA, hN)    | Cascade                      | Empirical       | Transport equation  |

Differences in input physics lead to observable differences in event kinematics and cross-section predictions.

---

## **3. Comparing Generator Predictions**

### 3.1 Sample Comparisons

For a given process (e.g., CCQE on carbon at 1 GeV):

* **GENIE** may predict higher cross section with flat $Q^2$ distribution.
* **NEUT** with RPA suppression gives lower cross section at low $Q^2$.
* **NuWro** may include more 2p2h at higher multiplicities.
* **GiBUU** models FSI more dynamically, showing broader nucleon energy spectra.

These differences can be 10–30% or more, particularly in observables like:

* Muon angle and momentum
* Hadronic energy
* Multiplicities of final-state nucleons and pions

---

### 3.2 Importance of Final-State Topologies

Since experiments classify events based on **final-state particles**, not primary interaction types, these modeling differences affect:

* CC0π (QE-like) classification
* Proton multiplicity
* Visible energy

This has major implications for oscillation analyses.

---

## **4. Systematic Uncertainties in Cross-Section Models**

### 4.1 Sources of Uncertainty

* **Form factors** (e.g., axial mass $M_A$)
* **Nuclear models** (Fermi gas vs spectral function)
* **2p2h model normalization**
* **FSI modeling**
* **Hadronization parameters in DIS**
* **Matching thresholds (e.g., RES/DIS transition)**

---

### 4.2 Handling Uncertainties

#### Parameter Variation ("Reweighting")

Generators provide tools to vary model parameters without regenerating events.

Example: Vary $M_A$ by ±0.1 GeV and recompute cross section:

```math
\sigma(M_A \pm \delta) \rightarrow \Delta \sigma / \sigma
```

Reweighting is used to estimate systematic effects on reconstructed observables.

#### Covariance Matrices

Experiments build **error matrices** encoding cross-section uncertainties across bins of energy or kinematics. These are used in fits to oscillation parameters or unfolded cross sections.

---

### 4.3 Generator Tuning

* Experiments use near detector data to **tune** generators.
* Tuning adjusts parameters (e.g., 2p2h normalization, FSI strength) to match observed distributions.
* Tunes are validated against independent measurements.

Example:

* **T2K ND280** tunes NEUT to match muon $p, \cos\theta$ distributions.
* **MINERvA** performs fits to recoil energy and hadronic multiplicities.

---

## **5. Generator Use in Experimental Analysis**

### 5.1 Oscillation Experiments

Generators provide predictions for:

* **Near detector** spectra (to constrain flux and cross sections)
* **Far detector** response (oscillated spectrum)

Ratio method: comparing near/far spectra cancels some systematics, but cross-section modeling must still be consistent between detectors.

### 5.2 Cross-Section Measurements

Generators are used to:

* Correct for **acceptance** and **efficiency**
* **Unfold** detector-level distributions to true kinematics
* Provide **signal definitions** (e.g., CC0π, CC1π)

Care is needed to avoid model bias in unfolding.

---

## **6. Case Study: T2K vs MINERvA**

| Feature   | T2K                                  | MINERvA                                                |
| --------- | ------------------------------------ | ------------------------------------------------------ |
| Flux      | Narrowband, \~0.6 GeV                | Broad, 1–20 GeV                                        |
| Detector  | Fine-grained tracker (carbon, water) | Scintillator + passive targets                         |
| Generator | NEUT                                 | GENIE                                                  |
| Strategy  | Model tuning to ND280                | Direct cross-section extraction, then model comparison |

Both experiments see tensions between default generator predictions and data, especially in QE-like and pion production channels.

---

## **7. Future Directions**

* **Joint tuning** across experiments (e.g., T2K and MINERvA working together)
* Development of **global generator fits**
* More sophisticated **theory-based models** (e.g., spectral functions, ab initio nuclear models)
* **Generator-independent measurements**: publish observables with minimal unfolding/model assumptions

---

## **8. Summary and Takeaways**

* Neutrino generators differ in models and assumptions, leading to nontrivial differences in predictions.
* Cross-section uncertainties are a major source of systematic error in oscillation experiments.
* Reweighting and tuning are tools to estimate and constrain these uncertainties.
* Careful validation and transparent reporting of generator settings are essential for reproducibility and comparison.
* Cross-section model systematics propagate directly into oscillation parameter measurements and need rigorous treatment.

---

## **Reading Assignments**

* NuSTEC White Paper, *Prog. Part. Nucl. Phys.* **100**, 1 (2018), Sections 3–4.
* T2K Collaboration, *Phys. Rev. D* **93**, 112012 (2016) – generator tuning example.
* MINERvA Collaboration, *Phys. Rev. D* **100**, 092001 (2019) – generator comparison in pion production.

---

## **Optional Homework**

**Exercise:**
Compare GENIE and NuWro predictions for CCQE muon angular distributions at $E_\nu = 1 \, \text{GeV}$ on carbon.

* What differences do you observe in $d\sigma/d\cos\theta_\mu$?
* Try changing $M_A$ and Fermi momentum in GENIE and re-plot.

**Discussion Prompt:**
How can we design an experiment or analysis to be less sensitive to generator uncertainties? What are the trade-offs?
