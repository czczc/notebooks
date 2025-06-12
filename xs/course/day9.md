# **Day 9: Neutrino Cross Sections and the DUNE Experiment**

---

## **1. Introduction**

The Deep Underground Neutrino Experiment (DUNE) is a next-generation flagship neutrino experiment aiming to resolve fundamental questions about neutrino masses and mixing, CP violation, and supernova neutrinos. To reach its ambitious precision goals, DUNE must achieve unprecedented control over **neutrino cross-section systematics**, particularly for interactions on **argon**.

Goals:

* Understand how DUNE is designed to measure and control neutrino interaction systematics.
* Explore the role of the Near Detector (ND) and Far Detector (FD).
* Learn what cross-section measurements DUNE will provide.
* Discuss open challenges and how DUNE aims to overcome them.

---

## **2. DUNE Overview**

### 2.1 General Setup

* Long-baseline experiment: $L = 1300 \, \text{km}$ (Fermilab to SURF in South Dakota).
* Neutrino beam: high-intensity, wide-band (up to \~5 GeV), primarily $\nu_\mu$.
* Detectors:

  * **Far Detector (FD)**: Four 10-kt LArTPC modules, deep underground.
  * **Near Detector (ND)** complex (on Fermilab site):

    * High-resolution **ND-LAr** TPC (same target material as FD),
    * Magnetized **ND-GAr** gas TPC for charge/momentum measurements,
    * **SAND** beam monitor (on-axis).

---

## **3. Role of Cross Sections in DUNE**

### 3.1 Why It Matters

Precision measurements (e.g., CP violation phase $\delta_{CP}$) require:

* Accurate neutrino energy reconstruction,
* Reliable signal/background separation (e.g., CCQE vs CCπ),
* Knowledge of final-state particle multiplicities and kinematics.

Cross-section uncertainties propagate into:

* **Energy bias**,
* **Signal misidentification**,
* **Systematic error inflation** in oscillation parameter fits.

---

## **4. Challenges with Argon as a Target**

### 4.1 Nuclear Effects on Argon

Argon ($^{40}\text{Ar}$) is heavier and more complex than carbon or oxygen:

* **Fermi motion**: higher average momentum (\~250 MeV/c),
* **Binding energy**: affects outgoing nucleon energy,
* **2p2h effects**: not fully characterized on argon,
* **FSI**: denser nuclear medium → more rescattering, pion absorption, etc.

These introduce uncertainties in both final-state particle content and energy reconstruction.

---

## **5. The DUNE Near Detector Strategy**

DUNE uses a multi-detector approach to separate and control flux and cross-section uncertainties.

---

### 5.1 ND-LAr: Liquid Argon TPC

* Same target as FD → minimizes extrapolation bias,
* Excellent imaging of tracks and showers,
* Sensitive to protons, pions, and muons,
* Provides high-statistics samples of:

  * CC0π, CC1π, 2p2h,
  * ν vs $\bar{\nu}$ interactions,
  * Multiplicities and kinematic distributions.

---

### 5.2 ND-GAr: Magnetized Gas TPC

* Lower density: reduced overlapping tracks and FSI confusion,
* Magnetic field allows:

  * Charge separation ($\mu^+$ vs $\mu^-$),
  * Precision momentum measurements (curvature),
* Complements ND-LAr by resolving ambiguities (e.g., sign identification, low-energy neutrons).

---

### 5.3 DUNE-PRISM Concept

* The entire ND complex can **move off-axis** up to ±30 m,
* Samples different neutrino energy spectra with the same flux integral,
* Allows **model-independent constraints** of cross-section effects,
* Facilitates disentangling of energy-dependent response and flux shape.

---

## **6. Expected Measurements and Capabilities**

DUNE ND will perform:

* **Flux-integrated differential cross sections** on argon:

  * $\frac{d\sigma}{dQ^2}$, $\frac{d\sigma}{dp_\mu}$, etc.
* **Exclusive final state topology measurements**:

  * CC0π, CC1π, CC2p, etc.
* **Neutron multiplicity measurements** using calorimetry and timing,
* **Proton kinematics and correlations** (e.g., $\delta p_T$, opening angles),
* **$\nu_e$** and $\nu_\tau$ cross sections (from beam tail and appearance),
* **Cross-section ratios** (e.g., $\bar{\nu}_\mu / \nu_\mu$).

These will be used to:

* Constrain cross-section model parameters,
* Tune event generators (e.g., GENIE),
* Reduce oscillation systematic uncertainties to target levels (e.g., <3%).

---

## **7. From Near to Far: Oscillation Analysis Flow**

### 7.1 Traditional Approach

1. Measure event spectra at ND,
2. Tune model (GENIE, etc.),
3. Use model to predict FD spectra without oscillations,
4. Apply oscillation probability,
5. Compare with FD data.

**Challenge:** Model errors at ND affect FD extrapolation.

---

### 7.2 DUNE’s Enhanced Strategy

* Use PRISM off-axis data to constrain energy-dependent response without relying solely on a generator,
* Apply data-driven extrapolation techniques,
* Marginalize over cross-section uncertainties informed by ND measurements.

This improves robustness and reduces model dependence.

---

## **8. Broader Impact of DUNE ND Measurements**

Beyond DUNE oscillations, the ND will provide:

* World-leading data on $\nu$-argon interactions,
* New input for global generator development,
* Testbed for new nuclear models (e.g., spectral function, SuSAv2, EFT),
* Calibration samples for supernova neutrino response,
* Probes of fundamental physics (e.g., sterile neutrinos, BSM interactions).

---

## **9. Summary and Takeaways**

* DUNE’s sensitivity to CP violation and mass ordering depends critically on controlling cross-section uncertainties.
* The DUNE Near Detector suite is designed to provide detailed and high-statistics interaction measurements on argon.
* The combination of LArTPC, gas TPC, and off-axis capability makes DUNE uniquely powerful for cross-section constraints.
* These measurements will shape both DUNE’s success and broader advances in neutrino interaction physics.

---

## **Reading Assignments**

* DUNE Near Detector Conceptual Design Report (CDR), available on [DUNE docDB](https://docs.dunescience.org).
* M. Tenti et al., *JINST* **15**, T08008 (2020) – DUNE ND overview.
* Carneiro et al., “Neutrino Interaction Physics and the DUNE Near Detector,” DUNE-doc-17325.

---

## **Optional Homework**

**Exercise:**
Propose a measurement of $\nu_\mu$ CC0π cross sections on argon using ND-LAr.

* What cuts would you apply?
* What observables would you report?
* How would you control for FSI effects?

**Discussion Prompt:**
What are the advantages of DUNE-PRISM over a traditional fixed-location near detector? How does it reduce model dependence?
