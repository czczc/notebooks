# **Day 4: Deep Inelastic Scattering (DIS) and the High-Energy Regime**

---

## **1. Introduction**

At neutrino energies above \~3 GeV, a new regime becomes dominant: **deep inelastic scattering (DIS)**. In DIS, the neutrino interacts not with an entire nucleon, but with individual quarks inside the nucleon.

Goals of this lecture:

* Understand the formalism and kinematics of neutrino DIS.
* Learn about structure functions and their relation to parton distribution functions (PDFs).
* Explore how DIS is modeled in event generators.
* Discuss nuclear effects in DIS and the transition from resonance to DIS (SIS region).

---

## **2. DIS: The Parton-Level Picture**

### 2.1 The Basic Reaction

```math
\nu_\mu + N \rightarrow \mu^- + X
```

* $N$: nucleon (proton or neutron),
* $X$: hadronic final state containing many particles (jets, pions, baryons),
* Neutrino scatters off an individual quark in the nucleon.

---

### 2.2 Feynman Diagram

At leading order, the process is:

```math
\nu_\mu + q \rightarrow \mu^- + q'
```

Mediated by $W^\pm$ exchange (CC) or $Z^0$ (NC), depending on the interaction.

---

## **3. Kinematics and Variables**

Define standard DIS variables:

```math
\begin{aligned}
& Q^2 = -q^2 = -(k - k')^2 \quad \text{(momentum transfer)} \\
& x = \frac{Q^2}{2 M \nu} \quad \text{(Bjorken-x, fraction of nucleon momentum)} \\
& y = \frac{\nu}{E_\nu} \quad \text{(inelasticity)} \\
& W^2 = (p + q)^2 = M^2 + 2 M \nu - Q^2 \quad \text{(invariant mass of hadronic system)} \\
\end{aligned}
```

Where:

* $k, k'$: initial and final lepton 4-momenta,
* $p$: nucleon 4-momentum,
* $q$: 4-momentum transfer,
* $\nu = E_\nu - E_\mu$: energy transferred to the hadronic system.

---

## **4. Neutrino DIS Cross Section**

### 4.1 Differential Cross Section (CC)

For an isoscalar target (equal number of p and n), the double differential cross section is:

```math
\frac{d^2\sigma^{\nu(\bar{\nu})}}{dx \, dy} = \frac{G_F^2 M E_\nu}{\pi} 
\left[ \left(1 - y - \frac{M x y}{2 E_\nu} \right) F_2(x, Q^2) 
+ \frac{y^2}{2} 2xF_1(x, Q^2) 
\pm y \left(1 - \frac{y}{2} \right) xF_3(x, Q^2) \right]
```

* $\pm$ for $\nu$ and $\bar{\nu}$,
* $F_1, F_2, F_3$: structure functions,
* $F_2$ is most commonly used; $F_1$ is related by the Callan-Gross relation at LO.

---

### 4.2 Callan-Gross Relation

At leading order and assuming spin-1/2 partons:

```math
F_2(x, Q^2) = 2x F_1(x, Q^2)
```

This is used to eliminate $F_1$ in many expressions.

---

### 4.3 Structure Function $F_3$

The $F_3$ term is unique to weak interactions and reflects parity violation. It is odd under charge conjugation:

```math
xF_3^\nu = x[q(x) - \bar{q}(x)]
```

This makes $xF_3$ sensitive to valence quark distributions.

---

## **5. Parton Distribution Functions (PDFs)**

### 5.1 What Are PDFs?

* PDFs describe the probability of finding a parton (quark or gluon) carrying a momentum fraction $x$ inside the nucleon at a scale $Q^2$.
* Not perturbatively calculable; extracted from global fits to experimental data.
* Depend on $x$ and $Q^2$, and evolve via DGLAP equations.

Common PDF sets: CTEQ, MSTW, NNPDF, GRV.

---

### 5.2 Neutrino PDFs vs Electron PDFs

* Neutrinos can access both quarks and anti-quarks due to the weak interaction's chiral nature.
* Unique sensitivity to strange and charm quarks via:

```math
\nu_\mu + s \rightarrow \mu^- + c
```

Allows probing of sea quark content and CKM matrix elements.

---

## **6. From Resonance to DIS: The SIS Region**

The **Shallow Inelastic Scattering (SIS)** region bridges resonance production and DIS.

* Typically $W \sim 1.6\text{–}2.2 \, \text{GeV}$.
* Overlap between multiple resonances and partonic behavior.
* Double counting must be avoided in generators: careful matching of RES and DIS models is needed.

Generators handle this via:

* Switching from RES to DIS at a matching scale $W_\text{cut} \sim 1.7 \, \text{GeV}$.
* Smooth blending of contributions or empirical suppression factors.

---

## **7. Hadronization and Final States**

In DIS, the struck quark hadronizes into multiple particles.

### 7.1 Hadron Multiplicity

Typical features:

* Many pions, baryons, and sometimes kaons or heavier mesons.
* Multiplicity grows with $W$.

### 7.2 Hadronization Models

Generators use fragmentation models, e.g.:

* **PYTHIA** (Lund string model),
* **KNO scaling**,
* **Empirical fits**.

Above a certain $W$, full hadronization libraries are invoked. Below this, semi-inclusive channels are modeled.

---

## **8. Nuclear Effects in DIS**

Even in DIS, nuclear targets modify observed cross sections:

### 8.1 Shadowing

At low $x \lesssim 0.1$, coherent scattering off multiple nucleons reduces the cross section:

```math
R_A(x) = \frac{F_2^A(x)}{A F_2^N(x)} < 1
```

### 8.2 EMC Effect

At intermediate $x \sim 0.3\text{–}0.7$, structure functions in nuclei deviate from free nucleons.

### 8.3 Fermi Motion

At large $x$, smearing due to nucleon motion enhances the structure functions.

These are measured in charged lepton DIS and assumed to be similar in neutrino DIS, though this is not guaranteed.

---

## **9. Experimental Inputs**

Major DIS data sources:

* CCFR and NuTeV: $\nu$-Fe cross sections, structure functions.
* CDHSW: early structure function measurements.
* NOMAD: high-resolution data with hadronic reconstruction.
* MINERvA: modern DIS cross sections and nuclear comparisons.

These datasets feed into global PDF fits (e.g., nCTEQ for nuclear PDFs).

---

## **10. Summary and Takeaways**

* DIS becomes dominant above \~3 GeV; neutrinos scatter off quarks.
* Structure functions $F_2, F_3$ encode the quark momentum distributions.
* Neutrino DIS provides unique probes of the nucleon sea (strange, charm).
* Transition region between resonance and DIS requires careful modeling.
* Nuclear modifications (shadowing, EMC, Fermi motion) impact neutrino DIS cross sections.

---

## **Reading Assignments**

* Formaggio & Zeller, *Rev. Mod. Phys.* **84**, 1307 (2012), §V (DIS).
* Particle Data Group, “Structure Functions” and “Neutrino Cross Sections” sections.
* U.K. Yang & A. Bodek, *Phys. Rev. Lett.* **82**, 2467 (1999) – modified PDFs at low $Q^2$.

---

## **Optional Homework**

**Problem:**
Using PDFs (e.g., simple toy model), compute the neutrino DIS cross section at $E_\nu = 10 \, \text{GeV}$ and $x = 0.3$. Assume only $u$ and $d$ valence quarks contribute and use:

```math
F_2^\nu(x) = 2x[u(x) + d(x)], \quad xF_3^\nu(x) = 2x[u(x) - d(x)]
```

**Discussion Prompt:**
Why is it difficult to cleanly separate resonance and DIS events in detectors? How might hadron multiplicity and kinematic variables help in identifying DIS?

