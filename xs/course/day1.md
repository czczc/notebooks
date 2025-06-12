# **Day 1: Weak Interaction Formalism and Cross-Section Basics**

---

## **1. Introduction to Neutrino Interactions**

Neutrinos interact only via the **weak interaction**, mediated by the charged $W^\pm$ and neutral $Z^0$ bosons. This lecture introduces the formalism used to describe neutrino scattering processes, with a focus on charged-current (CC) interactions.

We aim to answer:

* How do we model neutrino interactions with fundamental particles (electrons, quarks, nucleons)?
* What is the structure of the weak interaction Lagrangian?
* How are cross sections defined and computed in scattering processes?

---

## **2. The Electroweak Lagrangian**

The weak interaction is part of the electroweak sector of the Standard Model:

$$
\mathcal{L}_\text{int} = \frac{g}{\sqrt{2}} \left( \bar{\ell}_L \gamma^\mu \nu_L W_\mu^- + \bar{u}_L \gamma^\mu d_L W_\mu^+ \right) + \text{h.c.} + \frac{g}{2\cos\theta_W} \sum_f \bar{f} \gamma^\mu (g_V^f - g_A^f \gamma^5) f Z_\mu
$$

Key points:

* $\nu_L$ and $\ell_L$ are left-handed neutrino and charged lepton fields.
* Charged-current (CC) processes involve $W^\pm$ exchange.
* Neutral-current (NC) processes involve $Z^0$ exchange.

---

## **3. Tree-Level CC Scattering Example: Neutrino-Electron Scattering**

We begin with the simplest process:

$$
\nu_e + e^- \rightarrow \nu_e + e^-
$$

This proceeds via **t-channel** exchange of a $Z^0$ boson for NC, or a $W^-$ boson for CC (if same flavor). The matrix element is:

$$
\mathcal{M} = \frac{G_F}{\sqrt{2}} \left[ \bar{u}_\nu \gamma^\mu (1 - \gamma^5) u_\nu \right] \left[ \bar{u}_e \gamma_\mu (g_V - g_A \gamma^5) u_e \right]
$$

For low-energy (much less than $M_W$), the weak interaction is approximated by a 4-fermion contact interaction with coupling $G_F \approx 1.166 \times 10^{-5} \, \text{GeV}^{-2}$.

---

## **4. Differential Cross Section – General Formalism**

The general form of a 2-to-2 differential cross section in the lab frame:

$$
\frac{d\sigma}{d\Omega} = \frac{1}{64\pi^2 s} \frac{|\vec{p}_f|}{|\vec{p}_i|} |\mathcal{M}|^2
$$

For neutrino scattering off stationary target particles (e.g., electrons or nucleons), we often work in the **lab frame**, where the target is at rest and the neutrino has incoming energy $E_\nu$.

**Kinematic variables:**

* $Q^2 = -q^2 = -(k - k')^2$: squared momentum transfer
* $x = \frac{Q^2}{2 M \nu}$: Bjorken scaling variable
* $y = \frac{\nu}{E_\nu}$: inelasticity

---

## **5. Neutrino–Nucleon Scattering**

Let’s move to a more relevant case: neutrino scattering off a **free nucleon**.

$$
\nu_\mu + n \rightarrow \mu^- + p
$$

The hadronic current is expressed as:

$$
J^\mu = \bar{u}_p \left[ F_1(Q^2)\gamma^\mu + F_2(Q^2)\frac{i\sigma^{\mu\nu} q_\nu}{2M} + F_A(Q^2) \gamma^\mu \gamma^5 + F_P(Q^2) q^\mu \gamma^5 \right] u_n
$$

Where:

* $F_1, F_2$: vector form factors (from electron scattering)
* $F_A$: axial-vector form factor (not directly accessible from charged leptons)
* $F_P$: pseudoscalar form factor (often small at GeV energies)

The matrix element is then:

$$
\mathcal{M} = \frac{G_F \cos\theta_C}{\sqrt{2}} [\bar{u}_\mu \gamma^\mu (1 - \gamma^5) u_\nu] \cdot [\bar{u}_p J_\mu u_n]
$$

Where $\theta_C$ is the Cabibbo angle (\~13°), accounting for quark mixing.

---

## **6. Cross Section for Charged-Current Quasi-Elastic (CCQE) Scattering**

We define:

* $E_\nu$: incoming neutrino energy
* $E_\mu$, $\theta_\mu$: outgoing muon energy and angle
* $Q^2 = 2 E_\nu E_\mu (1 - \cos\theta_\mu) - m_\mu^2$

Using Llewellyn Smith’s formalism (1972), the differential cross section is:

$$
\frac{d\sigma}{dQ^2} = \frac{G_F^2 \cos^2 \theta_C}{8\pi E_\nu^2} \left[ A(Q^2) - \frac{s - u}{M^2} B(Q^2) + \frac{(s - u)^2}{M^4} C(Q^2) \right]
$$

With functions $A, B, C$ depending on form factors.

In practice, we often use a **dipole form** for the axial form factor:

$$
F_A(Q^2) = \frac{g_A}{\left(1 + \frac{Q^2}{M_A^2}\right)^2}
$$

* $g_A \approx 1.267$
* $M_A \approx 1.0$ GeV (from bubble chamber data)

---

## **7. Total Cross Section Behavior**

For free nucleons, the CCQE cross section grows approximately linearly with energy in the sub-GeV to few-GeV range:

$$
\sigma(E_\nu) \approx 0.9 \times 10^{-38} \, \left( \frac{E_\nu}{\text{GeV}} \right) \, \text{cm}^2
$$

**Antineutrinos** have lower cross sections due to helicity and coupling differences. Roughly:

$$
\sigma_{\bar{\nu}} \sim \frac{1}{3} \sigma_\nu
$$

---

## **8. Neutrino–Nucleus Scattering Considerations**

When the target is a **nucleus** (C, O, Ar), several effects arise:

* **Fermi motion**: nucleons have intrinsic momentum
* **Pauli blocking**: outgoing nucleon cannot occupy filled states
* **Binding energy**: reduces available energy
* **Final-state interactions (FSI)**: outgoing hadrons scatter or are absorbed

We'll explore these in depth in the next lecture, but it's critical to understand that even a theoretically clean CCQE interaction becomes murky in nuclei.

---

## **9. Summary and Key Takeaways**

* Weak interactions are described by the $V - A$ structure of the Standard Model.
* Neutrino scattering processes can be computed using matrix elements and form factors.
* The simplest processes (e.g., $\nu e^-$) can be treated analytically; nucleon targets require phenomenological input (form factors).
* Nuclear targets require additional modeling (to be covered on Day 2).

---

## **10. Reading Assignments**

* J.A. Formaggio & G.P. Zeller, *Rev. Mod. Phys.* **84**, 1307 (2012), Sections II–III
* G.P. Zeller, *PDG Review (2023)*, "Neutrino Cross Section Measurements" – §51.1 and Table 51.1
* C.H. Llewellyn Smith, *Phys. Rept.* **3**, 261 (1972) (for QE formalism derivation)

---

## **Optional Homework**

**Problem:**
Derive the expression for $d\sigma/dQ^2$ for the process $\nu_\mu + n \rightarrow \mu^- + p$, assuming the nucleon is at rest and neglecting Fermi motion. Use a dipole axial form factor and ignore the pseudoscalar term.

**Bonus:**
Estimate the total cross section at $E_\nu = 1 \, \text{GeV}$ and compare to the empirical formula.

