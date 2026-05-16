# QZS Literature — Notes and Summaries

## Background: Why QZS?

A conventional passive isolator works above its natural frequency. To isolate low-frequency vibration, you need a low natural frequency, which means low stiffness — but low stiffness means poor load-bearing. QZS solves this by combining a positive stiffness mechanism (which carries the load) with a negative stiffness mechanism (which cancels out most of the dynamic stiffness near equilibrium). The result: high static stiffness, near-zero dynamic stiffness, and a natural frequency that can be pushed well below what a linear spring system allows.

---

## Paper Summaries

### 1. On the force transmissibility of a QZS vibration isolator
**Journal:** Journal of Sound and Vibration (2009)  
**Link:** https://www.sciencedirect.com/science/article/pii/S0022460X08009437

The foundational QZS paper. Uses a classic three-spring arrangement (one vertical spring + two oblique springs) and derives the force transmissibility analytically. Shows that QZS systems can achieve much lower transmissibility than equivalent linear isolators in the low-frequency range, at the cost of a nonlinear jump phenomenon under large excitation. Establishes conditions for the QZS point and derives the stiffness in terms of spring geometry. This is the paper most QZS work cites as its starting point.

---

### 2. A novel QZS isolation platform via tunable positive and negative stiffness compensation mechanism
**Journal:** Nonlinear Dynamics (2023)  
**DOI:** https://doi.org/10.1007/s11071-023-09018-0

Proposes a QZS platform where both the positive and negative stiffness components are independently tunable — addressing the limitation that most QZS designs only work well at one specific load. The compensation mechanism allows the QZS condition to be maintained across a range of payloads without redesigning the geometry. Relevant to this project because the VCA+Stewart platform will need to handle varying loads.

---

### 3. An innovative QZS isolator with three pairs of oblique springs
**Journal:** International Journal of Mechanical Sciences (2020)  
**Link:** https://www.sciencedirect.com/science/article/pii/S002074032032316X

Extends the basic three-spring QZS idea by using three *pairs* of oblique springs symmetrically arranged. More pairs → wider stroke over which near-zero stiffness is maintained, and better symmetry reduces lateral instability. Compares transmissibility and effective isolation bandwidth against single-pair configurations. Useful reference for understanding how geometry scaling affects QZS performance.

---

### 4. Nonlinear vibration of a slightly curved beam with QZS isolators
**Journal:** Nonlinear Dynamics (2018)  
**DOI:** https://doi.org/10.1007/s11071-018-4697-9

Most QZS work treats the isolated structure as a rigid mass. This paper considers what happens when the structure itself is a flexible beam with slight initial curvature. Finds that the curvature introduces square nonlinearity and increases the effective resonant frequency, narrowing the isolation bandwidth. QZS isolators still reduce transmissibility at resonance, but the flexible structure interacts with the isolator in ways that a simple SDOF model misses. Relevant if the platform legs or payload structure has significant compliance.

---

### 5. In-situ adjustable nonlinear passive stiffness using X-shaped mechanisms
**Journal:** Mechanical Systems and Signal Processing (2021)  
**Link:** https://www.sciencedirect.com/science/article/pii/S0888327021006348

X-shaped (scissor-type) mechanisms are a manufacturing-friendly alternative to oblique spring arrangements. This paper shows that the geometric nonlinearity of the X-shape naturally produces a softening stiffness characteristic, and that this can be tuned in-situ by adjusting the joint angles. Advantage over fixed oblique springs: stiffness can be adjusted after assembly. Relevant for the passive layer of this platform.

---

### 6. Nonlinear compensation method for quasi-zero stiffness vibration isolation
**Journal:** Journal of Sound and Vibration (2022)  
**Link:** https://www.sciencedirect.com/science/article/pii/S0022460X21007379

Addresses the main practical problem with QZS: the nonlinear stiffness means transmissibility degrades rapidly when the system operates away from the QZS point (overload/underload). Proposes a compensation strategy — either passive geometric correction or a feedforward active term — to extend the effective QZS region. Directly relevant to the control design for this project.

---

### 7. Magnetic Negative Stiffness Devices for Vibration Isolation — State-of-the-Art Review
**Journal:** Applied Sciences (2024)  
**Link:** https://www.mdpi.com/2076-3417/14/11/4698

Comprehensive review of magnetic negative stiffness (MNS) as a replacement for mechanical oblique springs. Covers four main architectures: magnetic ring arrangements, rectangular magnet pairs, wedge-shaped magnets, and electromagnetic (coil-based) springs. Key advantage of MNS over mechanical springs: no friction at joints, non-contact, tunable in real time if electromagnetic. Key challenge: load-dependent nonlinearity and sensitivity to alignment. Includes full mathematical models (magnetic charge method) for force and stiffness calculation. Useful for understanding whether permanent magnets could replace the passive spring layer in this platform.

---

## Key Takeaways for This Project

- The passive layer of the platform should target QZS to push the isolation frequency as low as possible before the VCAs take over
- Oblique springs, X-mechanisms, and magnetic springs are all viable negative stiffness mechanisms; magnetic springs avoid friction but require careful alignment
- QZS performance degrades off-equilibrium — the control layer (VCAs + LVDT feedback) will need to compensate for this
- Flexible structures interact with QZS isolators in non-trivial ways; worth checking whether the Stewart platform legs introduce significant compliance
