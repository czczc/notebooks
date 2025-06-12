# **Day 8: Detector Technologies and Reconstruction Challenges**

---

## **1. Introduction**

The measurement of neutrino cross sections and oscillation parameters is limited not only by theoretical models, but also by the capabilities of the detectors used to observe final-state particles. Understanding the design, strengths, and limitations of various detector technologies is essential for interpreting neutrino interactions and constraining systematic uncertainties.

Goals:

* Learn how common detector types operate and reconstruct neutrino events.
* Identify key challenges in reconstructing neutrino energy and interaction type.
* Understand how detector technology impacts cross-section measurements.
* Appreciate how detector-specific limitations shape data analysis strategies.

---

## **2. Major Detector Technologies in Neutrino Experiments**

---

### 2.1 Liquid Argon Time Projection Chambers (LArTPCs)

#### Principle:

* Charged particles ionize argon as they traverse the detector.
* Ionization electrons drift in an electric field and are read out by wire planes.
* Combine with scintillation light for timing.

#### Features:

* High-resolution 3D imaging,
* Excellent particle identification (PID) via dE/dx,
* Low detection threshold for protons and pions (\~20–50 MeV),
* Fully active volume.

#### Challenges:

* Large data volumes,
* Complex reconstruction (pattern recognition, track merging),
* Neutron detection is difficult (mostly via secondary proton recoils).

#### Examples:

* MicroBooNE, ICARUS, SBND, DUNE.

---

### 2.2 Scintillator Tracking Detectors

#### Principle:

* Charged particles pass through plastic scintillator strips or bars,
* Produce light collected by photodetectors.

#### Features:

* Fast timing, moderate spatial resolution,
* Multi-plane design allows 2D/3D tracking,
* Magnetic field enables momentum and charge reconstruction (e.g., T2K ND280).

#### Challenges:

* Proton threshold typically higher (\~50 MeV kinetic energy),
* Limited PID beyond muon vs electron,
* Poor neutron sensitivity.

#### Examples:

* MINERvA, NOvA, T2K ND280.

---

### 2.3 Water Cherenkov Detectors

#### Principle:

* Charged particles above Cherenkov threshold emit cone of light in water,
* Light collected by photomultiplier tubes (PMTs),
* Ring shape identifies particle type.

#### Features:

* Large volumes at low cost,
* Excellent muon/electron discrimination,
* Good for energy and direction of leptons.

#### Challenges:

* High detection threshold:

  * Protons: invisible,
  * Pions: partial efficiency,
* No sensitivity to neutrons,
* No hadronic energy reconstruction.

#### Examples:

* Super-Kamiokande, Hyper-Kamiokande, T2K far detector.

---

### 2.4 Emulsion Detectors and Others

* **Emulsion detectors**: fine spatial resolution (used for τ identification).
* **Magnetized iron calorimeters**: measure muon charge and energy well (e.g., MINOS).

---

## **3. Reconstruction of Neutrino Events**

---

### 3.1 Neutrino Energy Estimation

There are two primary methods:

**1. Kinematic method** (for QE events):

```math
E_\nu^{QE} = \frac{2 (M - E_B) E_\mu - (E_B^2 - m_\mu^2 + \Delta M^2)}{2 \left[ (M - E_B) - E_\mu + p_\mu \cos\theta_\mu \right]}
```

Where:

* $M$: nucleon mass,
* $E_B$: binding energy,
* $\Delta M$: neutron-proton mass difference.

**2. Calorimetric method**:

```math
E_\nu = E_\mu + E_\text{had}
```

* Requires summing muon and hadronic energies,
* Sensitive to missing energy (neutrons, undetected particles).

---

### 3.2 Particle Identification

* **Muons**: long straight tracks, often exiting detector.
* **Electrons**: electromagnetic showers (Cherenkov rings or calorimeter blobs).
* **Protons**: short, heavily ionizing tracks (LAr, scintillator).
* **Pions**:

  * Charged: distinguish from muons via range/dE/dx,
  * Neutral: reconstruct from $\gamma\gamma$ pairs (π⁰ → γγ).

---

## **4. Challenges in Reconstruction**

---

### 4.1 Detection Thresholds

Each detector has a minimum energy for particle detection:

* **Water Cherenkov**: no proton detection below \~1 GeV/c,
* **Scintillator**: protons visible above \~50 MeV,
* **LArTPC**: protons seen down to \~20 MeV kinetic energy.

Undetected particles → underestimate hadronic energy → bias in $E_\nu$.

---

### 4.2 Neutron Detection

* Neutrons carry away energy undetected or with large delays.
* Can only be observed via:

  * Proton recoils (LArTPCs, with difficulty),
  * Capture gammas (delayed signals, low efficiency).

This is a major source of missing energy in calorimetric reconstruction.

---

### 4.3 Final-State Interactions (FSI)

FSI modify the final state after the initial neutrino interaction:

* Pions may be absorbed → mimic QE,
* Nucleons may be ejected or rescattered,
* Leads to wrong classification of interaction types.

Experiments report:

* **True topology** (e.g., CCQE),
* **Final-state topology** (e.g., CC0π, CC1π), more directly observable.

---

### 4.4 Detector Effects

* **Resolution**: affects momentum/energy reconstruction,
* **Smearing**: impacts unfolded cross-section distributions,
* **Acceptance**: limited by detector geometry and efficiency,
* **Mis-ID**: particle misidentification can swap channels (e.g., π⁺ ↔ μ⁺).

Careful simulation and unfolding procedures are required.

---

## **5. Detector-Specific Strategies**

---

### 5.1 Water Cherenkov (e.g., Super-K, Hyper-K)

* Focus on single-ring (μ or e) events,
* Use kinematic energy reconstruction,
* Poor hadronic reconstruction → reliance on CCQE-like events.

---

### 5.2 LArTPCs (e.g., MicroBooNE, DUNE)

* Identify exclusive topologies: e.g., 1μ1p, 1μ2p,
* Sensitive to nucleon-nucleon correlations,
* Use TKI observables to study nuclear effects:

```math
\delta p_T = |\vec{p}_\text{T}^{\,\mu} + \vec{p}_\text{T}^{\,p_1}| \quad \text{(transverse momentum imbalance)}
```

---

### 5.3 Scintillator Trackers (e.g., MINERvA)

* Broad acceptance, good timing,
* Use calorimetry and tracking for proton and pion ID,
* Subdivide data by multiplicity (0π, 1π, 1p1π, etc.).

---

## **6. Summary and Takeaways**

* Detector choice fundamentally shapes what can be measured and how precisely.
* No detector is perfect: all have blind spots and detection thresholds.
* Understanding these limitations is crucial for:

  * Accurate cross-section measurement,
  * Reducing bias in neutrino energy reconstruction,
  * Properly interpreting interaction modes.
* Ongoing development (e.g., improved reconstruction algorithms, hybrid detector designs) aims to minimize these limitations.

---

## **Reading Assignments**

* MicroBooNE Collaboration, *Phys. Rev. Lett.* **123**, 131801 (2019) – CC inclusive ν-Ar cross section.
* T2K Collaboration, *Phys. Rev. D* **98**, 012004 (2018) – Water vs CH cross-section ratio.
* MINERvA Collaboration, *Nucl. Instrum. Meth. A* **743**, 130 (2014) – Detector description and reconstruction.

---

## **Optional Homework**

**Exercise:**
Design an analysis to measure CCQE-like cross sections on argon using a LArTPC.

* What particles would you require in the final state?
* How would you define your signal?
* What are the dominant sources of uncertainty?

**Discussion Prompt:**
Why is it important to measure neutron multiplicities in neutrino interactions? What can these measurements tell us about the primary interaction and nuclear effects?
