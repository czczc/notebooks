# **Day 3: Resonance Production and Pion Channels**

---

## **1. Introduction**

At neutrino energies around 1–3 GeV, inelastic processes become increasingly important. One of the dominant mechanisms in this regime is **resonance production**, where the neutrino excites a baryonic resonance (like the Δ(1232)), which decays into a nucleon and one or more pions.

This lecture will cover:

* The formalism of neutrino-induced baryon resonance excitation.
* The Rein–Sehgal model for single-pion production.
* Coherent pion production.
* Nuclear medium effects on pion production.

---

## **2. Charged-Current Resonance Production**

### 2.1 The Basic Process

The leading resonance channel is:

```math
\nu_\mu + N \rightarrow \mu^- + \Delta \rightarrow \mu^- + N + \pi
```

Example:

```math
\nu_\mu + p \rightarrow \mu^- + p + \pi^+
```

This process dominates just above the QE regime (typically $E_\nu \gtrsim 1 \, \text{GeV}$) and produces a final state with a charged lepton and one or more pions.

---

### 2.2 The Δ(1232) Resonance

* The Δ(1232) is the lowest-lying and most prominent baryon resonance.
* Isospin triplet (I=3/2), spin-3/2 state.
* Mass: \~1232 MeV, width: \~120 MeV.
* Decays via strong interaction: $\Delta \rightarrow N + \pi$

Branching ratios:

* $\Delta^{++} \rightarrow p + \pi^+$
* $\Delta^+ \rightarrow p + \pi^0$, $n + \pi^+$

The neutrino primarily excites the Δ via charged-current interaction.

---

## **3. Rein–Sehgal Model**

### 3.1 Overview

The most commonly used model for neutrino-induced resonance production is the **Rein–Sehgal (RS) model** (1981), which includes:

* 18 baryon resonances up to \~2 GeV.
* Relativistic quark model form factors.
* Breit–Wigner distributions to account for resonance widths.
* Transition amplitudes parametrized using helicity amplitudes.

This model is implemented in most neutrino event generators (e.g., GENIE, NEUT, NuWro).

---

### 3.2 Matrix Element

The matrix element for neutrino excitation of a resonance $R$ is:

```math
\mathcal{M} \propto \bar{u}_\mu \gamma^\mu (1 - \gamma^5) u_\nu \cdot \langle R | J_\mu^\text{had} | N \rangle
```

The hadronic transition current is modelled as:

```math
\langle R | J_\mu^\text{had} | N \rangle = \bar{U}^\alpha(p_R) \Gamma_{\alpha\mu}(q) u(p_N)
```

where:

* $U^\alpha$: Rarita-Schwinger spinor for spin-3/2 resonances.
* $\Gamma_{\alpha\mu}(q)$: vertex function with vector and axial contributions.

---

### 3.3 Differential Cross Section

For single-resonance excitation (e.g., Δ), the cross section is typically expressed as:

```math
\frac{d\sigma}{dQ^2 dW} = \frac{G_F^2 \cos^2 \theta_C}{8\pi^2} \frac{|k'|}{|k|} \frac{W \Gamma(W)}{(W^2 - M_R^2)^2 + M_R^2 \Gamma^2(W)} \cdot | \mathcal{M} |^2
```

Where:

* $W$: hadronic invariant mass,
* $M_R$: resonance mass (e.g., 1232 MeV for Δ),
* $\Gamma(W)$: energy-dependent width.

This describes how likely it is to excite a resonance of mass $W$ in a given neutrino interaction.

---

## **4. Non-Resonant and Interference Contributions**

* In addition to resonance diagrams, **non-resonant background** (Born terms, contact interactions) contribute.
* The RS model includes both resonant and non-resonant amplitudes.
* For certain channels (e.g., $\nu p \rightarrow \mu^- p \pi^+$), **interference** between resonant and non-resonant amplitudes is constructive or destructive depending on isospin.

This leads to model dependence and challenges in fitting data.

---

## **5. Coherent Pion Production**

### 5.1 Process

In coherent interactions, the neutrino interacts with the entire nucleus as a whole, leaving it intact:

```math
\nu_\mu + A \rightarrow \mu^- + \pi^+ + A
```

* Occurs at low $Q^2$ and small $t$ (momentum transfer to the nucleus).
* The signature is a forward-going pion and lepton with no nuclear breakup.
* Only \~a few percent of total cross section near 1 GeV.

---

### 5.2 Theoretical Description

Models often rely on the **PCAC (Partially Conserved Axial Current)** hypothesis:

```math
\frac{d\sigma}{dQ^2 dt} \bigg|_{Q^2 \rightarrow 0} \propto \frac{1}{Q^2} \cdot f_\pi^2 \cdot \frac{d\sigma_{\pi A}}{dt}
```

* Uses pion–nucleus scattering data as input.
* Extended to finite $Q^2$ with axial form factor suppression.

Commonly used models: Rein–Sehgal (1983), Alvarez-Ruso (microscopic models), Berger–Sehgal.

---

## **6. Final-State Interactions (FSI)**

Even if a pion is produced in the primary interaction, it may be:

* **Absorbed** in the nucleus,
* **Charge-exchanged** (e.g., $\pi^+ \rightarrow \pi^0$),
* **Rescattered**, altering its energy and angle.

FSI reduce the observed pion yield and smear kinematics. This affects the reconstruction of the interaction type.

Generators model FSI using semi-classical intranuclear cascades (e.g., GENIE's INTRANUKE).

---

## **7. Experimentally Observed Channels**

Key final states observed in detectors:

* **CC1π⁺:** Charged-current with exactly one $\pi^+$ (often from Δ resonance).
* **CC1π⁰:** CC with one neutral pion.
* **CC0π:** Zero-pion final state; can include QE, 2p2h, or pion production with pion absorption.
* **NCπ⁰:** Neutral-current with a single π⁰ (background for νₑ appearance).

Careful analysis and model comparisons are needed to disentangle these.

---

## **8. Summary and Takeaways**

* Resonant pion production is the dominant inelastic process around 1–2 GeV.
* The Δ(1232) resonance is the most significant contributor.
* The Rein–Sehgal model is widely used but has limitations.
* Coherent pion production adds a small, forward-peaked contribution.
* FSI significantly affect the observed final state and complicate event interpretation.
* Disentangling QE-like and resonance events requires detailed kinematic and topological analysis.

---

## **Reading Assignments**

* D. Rein and L.M. Sehgal, *Annals of Phys.* **133**, 79 (1981) – foundational RS model.
* E. A. Paschos and J.Y. Yu, *Phys. Rev. D* **65**, 033002 (2002) – coherent pion production via PCAC.
* K. Gallmeister et al., *Phys. Rev. C* **94**, 035502 (2016) – modern modeling of pion production and FSI.

---

## **Optional Homework**

**Problem:**
Using the Breit–Wigner formula, estimate the cross section for Δ(1232) production in $\nu_\mu p \rightarrow \mu^- p \pi^+$ at $E_\nu = 1.5 \, \text{GeV}$. Assume a width $\Gamma = 120 \, \text{MeV}$ and peak at $W = 1.232 \, \text{GeV}$.

**Discussion Prompt:**
Why do experiments report CC1π and CC0π channels separately? What challenges arise when trying to identify whether a pion was truly produced in the initial interaction?

