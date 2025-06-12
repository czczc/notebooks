# **Day 2: Quasi-Elastic Scattering on Nucleons and Nuclei**

---

## **1. Introduction**

Quasi-elastic (QE) scattering is one of the most important neutrino interaction modes at energies of \~0.5–2 GeV, especially for oscillation experiments like T2K, MicroBooNE, and DUNE. In this lecture, we will examine the formalism of QE interactions with **free nucleons** and how these processes are modified when the target is a **nucleus** (e.g., carbon or argon).

---

## **2. Charged-Current Quasi-Elastic (CCQE) Scattering**

### 2.1 The Reaction

For free nucleons:

```math
\begin{aligned}
  & \nu_\ell + n \rightarrow \ell^- + p \\
  & \bar{\nu}_\ell + p \rightarrow \ell^+ + n \\
\end{aligned}
```

This process proceeds via $W^\pm$ exchange and is mediated by the charged weak current.

---

### 2.2 Hadronic Current

The hadronic matrix element between nucleon states is written as:

```math
\langle p | J^\mu | n \rangle = \bar{u}_p(p') \left[ 
  F_1(Q^2)\gamma^\mu + 
  F_2(Q^2)\frac{i\sigma^{\mu\nu}q_\nu}{2M} + 
  F_A(Q^2)\gamma^\mu \gamma^5 + 
  F_P(Q^2) q^\mu \gamma^5
\right] u_n(p)
```

where:

* $F_1, F_2$ are vector form factors,
* $F_A$ is the axial-vector form factor,
* $F_P$ is the pseudoscalar form factor,
* $q^\mu = k^\mu - k'^\mu$ is the four-momentum transfer,
* $Q^2 = -q^2$ is the momentum transfer squared,
* $M$ is the average nucleon mass.

---

### 2.3 Vector Form Factors

The vector form factors are determined from electron scattering experiments using the Conserved Vector Current (CVC) hypothesis:

```math
F_1(Q^2) = \frac{G_E(Q^2) + \tau G_M(Q^2)}{1 + \tau}, \quad
F_2(Q^2) = \frac{G_M(Q^2) - G_E(Q^2)}{1 + \tau}, \quad
\tau = \frac{Q^2}{4M^2}
```

where $G_E$ and $G_M$ are the electric and magnetic Sachs form factors, often approximated by dipole forms.

---

### 2.4 Axial Form Factor

The axial-vector form factor is not accessible through electromagnetic probes and must be extracted from neutrino scattering data:

```math
F_A(Q^2) = \frac{g_A}{\left(1 + \frac{Q^2}{M_A^2} \right)^2}
```

* $g_A \approx 1.267$ (from neutron beta decay),
* $M_A \approx 1.0 \text{–} 1.2 \, \text{GeV}$ (empirically determined).

---

### 2.5 Pseudoscalar Form Factor

The pseudoscalar form factor $F_P(Q^2)$ is typically suppressed in high-energy interactions and can be approximated by PCAC:

```math
F_P(Q^2) = \frac{2 M^2 F_A(Q^2)}{m_\pi^2 + Q^2}
```

It is only important at low $Q^2$ or for processes involving muons with low energy.

---

## **3. Differential Cross Section (Free Nucleon)**

Using the Llewellyn Smith formalism, the differential cross section for CCQE is:

```math
\frac{d\sigma}{dQ^2} = \frac{G_F^2 \cos^2\theta_C}{8\pi E_\nu^2} 
\left[ A(Q^2) - \frac{s - u}{M^2} B(Q^2) + \frac{(s - u)^2}{M^4} C(Q^2) \right]
```

with the structure functions:

```math
\begin{aligned}
& A(Q^2) = m_\ell^2 \left( \frac{(F_1 + F_2)^2}{4M^2} + \frac{F_A^2}{Q^2} \right) + \cdots \\
& B(Q^2), C(Q^2): \text{additional form factor combinations} \\
\end{aligned}
```

Note: For most practical applications at GeV energies and with muons, $m_\ell$ terms can often be neglected.

---

## **4. Total Cross Section Behavior**

For neutrino energies between 0.5–2 GeV:

```math
\sigma_{\nu n \rightarrow \mu^- p} \sim 0.9 \times 10^{-38} \left( \frac{E_\nu}{\text{GeV}} \right) \, \text{cm}^2
```

For antineutrinos, the cross section is significantly smaller:

```math
\sigma_{\bar{\nu} p \rightarrow \mu^+ n} \sim \frac{1}{3} \sigma_\nu
```

This asymmetry arises due to helicity suppression and the structure of the weak interaction.

---

## **5. From Nucleons to Nuclei: Nuclear Corrections**

### 5.1 Key Effects in Nuclei

When neutrinos scatter off bound nucleons inside a nucleus (e.g., C or Ar), we must account for:

* **Fermi Motion:** Nucleons are not at rest; they have a momentum distribution.
* **Pauli Blocking:** Final-state nucleons must occupy available quantum states.
* **Binding Energy:** Energy required to remove nucleons from the nucleus.
* **Final-State Interactions (FSI):** Outgoing hadrons interact with other nucleons.

These effects change both the cross section and the final-state topology observed in detectors.

---

### 5.2 Fermi Gas Model (FGM)

The simplest model is the **Relativistic Fermi Gas (RFG)**:

* Nucleons fill momentum states up to a Fermi momentum $p_F$ (\~220 MeV/c for carbon).
* Each nucleon has a binding energy $E_B$.
* The differential cross section is modified by integrating over the nucleon momentum distribution:

```math
\sigma_\text{nucleus} = \int d^3p \, f(p) \cdot \sigma_\text{free}(E_\nu, p)
```

This gives qualitative agreement with data but fails to capture correlations and long-range nuclear effects.

---

### 5.3 Spectral Function Approach

The **spectral function (SF)** provides a more realistic description:

* Describes the probability of finding a nucleon with momentum $\vec{p}$ and removal energy $E$.
* Encodes short-range correlations (SRC) and nuclear shell structure.
* Often computed from electron scattering data.

This model is more accurate but computationally intensive and requires empirical input.

---

### 5.4 Random Phase Approximation (RPA)

RPA accounts for **long-range correlations** and collective nuclear excitations.

* Particularly important at low $Q^2$, where Pauli blocking is strongest.
* Tends to **suppress** the cross section at low $Q^2$, improving agreement with T2K and MiniBooNE data.

---

### 5.5 Multi-Nucleon Effects (2p2h)

Experiments like MiniBooNE found excess CCQE-like events that couldn’t be explained by QE alone.

This led to the inclusion of:

* **2p2h interactions:** Neutrino scatters off a correlated nucleon pair.
* Leads to emission of two nucleons (e.g., $\mu^- + p + p$) without a pion.
* Often modeled semi-empirically due to lack of complete theoretical consensus.

These are not true QE, but often appear in the same event categories (i.e., 0 pion final states).

---

## **6. Experimental Definitions and Challenges**

In practice, experiments cannot always identify the interaction type perfectly.

* **CCQE-like (CC0π):** Events with one muon, no pions above detection threshold.
* Can include true QE, 2p2h, and RES events with absorbed pions.
* Final-state observables are **not** uniquely tied to interaction mechanisms due to FSI and nuclear effects.

---

## **7. Summary and Takeaways**

* CCQE is the dominant interaction mode at \~1 GeV and essential for oscillation measurements.
* On free nucleons, CCQE is well-described by the Llewellyn Smith formalism using form factors.
* In nuclei, significant modifications arise from nuclear motion, binding, correlations, and FSI.
* Accurate modeling of QE-like processes requires inclusion of multi-nucleon and correlation effects.
* Theoretical models (FGM, SF, RPA, 2p2h) are implemented in neutrino event generators (e.g., GENIE, NEUT, NuWro) with varying complexity.

---

## **Reading Assignments**

* J. Nieves et al., *Phys. Rev. C* **83**, 045501 (2011) — detailed nuclear model including RPA and 2p2h.
* G.P. Zeller, *PDG Review*, “Neutrino Cross Section Measurements,” §51.2.
* C.H. Llewellyn Smith, *Phys. Rept.* **3**, 261 (1972) — QE formalism for free nucleons.

---

## **Optional Homework**

**Problem:**
Using the dipole form factor for $F_A(Q^2)$ and assuming constant $F_1, F_2$, derive the expression for $d\sigma/dQ^2$ in the free nucleon case. Evaluate numerically for $E_\nu = 1 \, \text{GeV}$ and $Q^2 = 0.2 \, \text{GeV}^2$.

**Discussion Prompt:**
Why might an event with a muon and two protons be classified as CCQE-like? What measurements could help distinguish between true QE and 2p2h?


