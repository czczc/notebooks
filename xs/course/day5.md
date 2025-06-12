# **Day 5: Introduction to Neutrino Event Generators – The Case of GENIE**

---

## **1. Introduction**

Neutrino event generators are crucial tools for interpreting experimental data. They simulate neutrino interactions with matter, providing predictions for cross sections, final-state particles, and detector inputs. Today’s focus is on the **GENIE** event generator — widely used in DUNE, NOvA, MicroBooNE, and other experiments.

Goals:

* Understand why neutrino event generators are needed.
* Learn about GENIE’s structure and key physics models.
* Explore GENIE’s treatment of QE, RES, and DIS processes.
* Discuss input/output mechanics and how simulations are produced.

---

## **2. Why Use Event Generators?**

Experimental detectors observe **final-state particles**, not interaction types directly. To infer neutrino interaction mechanisms and reconstruct neutrino energy, we must:

* Simulate interactions: what particles are produced, at what energy and angle.
* Include detector effects: smearing, thresholds, efficiency.
* Model full interaction chain: primary vertex + nuclear effects + FSI.

Generators serve as the link between:

* **Theoretical models** (QE, RES, DIS, etc.)
* **Detector simulations** and **experimental analyses**

---

## **3. Overview of GENIE**

### 3.1 General Info

* **GENIE** = “Generates Events for Neutrino Interaction Experiments”
* Written in C++
* Covers neutrino energies from MeV to TeV
* Modular design with tunable parameters and alternate models

GENIE provides:

* Interaction cross sections for different processes
* Monte Carlo event generation with kinematics and particle IDs
* Final-state particle lists after nuclear re-interactions (FSI)

---

### 3.2 GENIE’s Process Flow

1. **Input**:

   * Neutrino flux (energy spectrum)
   * Target geometry (e.g., argon nucleus)
2. **Primary Interaction Generation**:

   * Randomly sample neutrino energy and target nucleon
   * Select interaction type (CCQE, RES, DIS, etc.)
   * Calculate kinematics using chosen physics model
3. **Final-State Interactions (FSI)**:

   * Simulate intranuclear rescattering of hadrons
4. **Output**:

   * Event record (particle types, momenta, origin, etc.)

---

## **4. Interaction Channels in GENIE**

GENIE implements distinct models for each process class:

### 4.1 Quasi-Elastic (CCQE)

* Based on **Llewellyn Smith formalism**
* Includes dipole axial form factor:

```math
F_A(Q^2) = \frac{g_A}{\left(1 + \frac{Q^2}{M_A^2} \right)^2}
```

* Default $M_A \sim 0.99 \, \text{GeV}$, configurable
* Nuclear model: **Global Fermi Gas (RFG)** by default
* Alternatives: **Local Fermi Gas**, **Spectral Function**, **RPA corrections**

---

### 4.2 Resonance Production (RES)

* Uses **Rein–Sehgal** model with up to 18 resonances
* Includes non-resonant background and interference terms
* Configurable resonance cut-off scale $W_\text{cut}$

---

### 4.3 Deep Inelastic Scattering (DIS)

* Uses **Bodek–Yang modified PDFs**
* Structure functions parameterized as:

```math
F_2(x,Q^2), \quad xF_3(x,Q^2)
```

* Cross-section interpolation in the low-$Q^2$ region
* Smoothly connected to resonance region via SIS model

---

### 4.4 Coherent Pion Production

* **Rein–Sehgal PCAC-based model**
* Separate modules for charged-current (CC) and neutral-current (NC)
* Improved versions available with Berger–Sehgal corrections

---

### 4.5 Two-Particle–Two-Hole (2p2h)

* Optional enhancement to model multi-nucleon interactions
* Effective models based on **Valencia group** (Nieves et al.)
* Activated in recent GENIE “tunes”

---

## **5. Final-State Interactions (FSI)**

After the primary interaction, GENIE models how particles propagate through the nucleus:

* **INTRANUKE-hA model**: semi-classical cascade
* Tracks pion and nucleon interactions with nuclear medium
* Possibilities:

  * Elastic scattering
  * Inelastic scattering
  * Absorption
  * Charge exchange

These affect what is observed in detectors and introduce **modeling uncertainties**.

---

## **6. Event Generation Mechanics**

### 6.1 Input Specifications

* Neutrino flux (text or ROOT histogram)
* Target material (e.g., CH, Ar, Pb)
* Geometry (optional, for full detector simulations)

### 6.2 Running GENIE

Basic command-line usage:

```bash
gevgen -p 14 -t 1000180400 -e 1,10 -n 10000 --cross-sections myxsec.xml
```

Where:

* `-p 14`: $\nu_\mu$
* `-t 1000180400`: $^{40}\text{Ar}$
* `-e`: energy range
* `-n`: number of events

### 6.3 Output

* Events stored in **GHEP format** (GENIE HEPEVT)
* Can be converted to ROOT trees or used in Geant4-based simulations
* Each event includes:

  * Incoming neutrino
  * Scattered lepton
  * Hadronic final state (pre- and post-FSI)

---

## **7. Model Parameters and Tunes**

GENIE allows **tuning** of model parameters:

* $M_A$, Fermi momentum, binding energy
* Normalization factors for RES, DIS, 2p2h
* FSI probabilities

Official tunes:

* **G18\_10a\_02\_11a**: widely used DUNE tune
* **G18\_02a\_02\_11b**: includes Valencia 2p2h and improved FSI

Experiments choose or develop their own tunes based on near detector data.

---

## **8. Strengths and Limitations**

**Strengths:**

* Modular, flexible, widely supported
* Broad energy range coverage
* Large user base and documentation

**Limitations:**

* Some models are phenomenological or simplified
* FSI treated semi-classically
* RES/DIS transition is model-dependent
* Limited theoretical uncertainty quantification

---

## **9. Summary and Takeaways**

* Event generators like GENIE are indispensable for neutrino experiments.
* GENIE implements QE, RES, DIS, and coherent processes with modular models.
* Final-state interactions are crucial for understanding detector observables.
* GENIE provides a tunable and extensible platform for simulation and analysis.
* Understanding model assumptions and limitations is key for interpreting data.

---

## **Reading Assignments**

* C. Andreopoulos et al., *Nucl. Instrum. Meth. A* **614**, 87 (2010) – GENIE overview paper
* GENIE User Manual (latest version) – available from genie-mc.org
* NuSTEC White Paper, *Prog. Part. Nucl. Phys.* **100**, 1 (2018), §2

---

## **Optional Homework**

**Exercise:**
Use GENIE to simulate 1000 $\nu_\mu$ CC interactions on $^{12}C$ at $E_\nu = 2 \, \text{GeV}$.

* What fraction are classified as QE, RES, DIS?
* What is the average number of pions produced per event?
* Vary $M_A$ from 0.99 to 1.2 GeV and compare $Q^2$ distributions.

**Discussion Prompt:**
Why might different experiments (e.g. T2K vs DUNE) require different GENIE tunes? How could this affect comparisons of cross-section results?
