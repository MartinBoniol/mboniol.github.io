---
permalink: /thesis
hidden: true
classes: wide
# layout: single-hf
# layout: single
layout: default
title: "Detection of Anomalies and Identification of their Precursors in Large Data Series Collections"
author_profile: true
redirect_from: 
  - /thesis
  - /thesis.html
---

# Verification of Neural Network mechanisms of ACAS-Xu

### Work In Progress, by Martin Boniol



## Context

Collision avoidance systems for air traffic, such as the Traffic Collision Avoidance System (TCAS), have been used for decades to reduce the risk of mid-air collisions. Their successor, the ACAS-X family, incorporates more advanced decision-making methods to address new challenges related to increasing air traffic and the emergence of drones.

The ACAS-X family includes two main variants:

- **ACAS-XA**: dedicated to commercial aviation, replacing legacy systems (TCAS and TCAS-II)  
- **ACAS-XU**: designed for drones, more complex, and introducing new challenges:
  - horizontal maneuvering
  - non-cooperative traffic management

The decision logic of these systems relies on Markov Decision Process (MDP) models to generate (offline) lookup tables (*LUTs – Look-Up Tables*) based on geometric state parameters of aircraft, enabling both horizontal and vertical collision avoidance guidance.

These LUTs store maneuver decisions depending on aircraft states.

#### Example of horizontal decisions

- **COC** (Clear of Conflict)  
- **WL / SL** (Weak / Strong Left)  
- **WR / SR** (Weak / Strong Right)  

![ACAS advisories]([acas-advisories.png](https://github.com/MartinBoniol/martinboniol.github.io/blob/main/assets/img/acas-advisories.png))  
![ACAS-Xu geometry]([acas-horizontal.png](https://github.com/MartinBoniol/martinboniol.github.io/blob/main/assets/img/acas-horizontal.png))

---

Despite their deterministic nature, these LUTs are extremely large, making their deployment on embedded systems challenging.  
Several approaches have proposed compressing them using neural networks, but these methods rely on approximations and raise safety and formal verification concerns.

In this context, this PhD work aims to analyze, evaluate, and improve compression and verification methods for ACAS-Xu systems.

---

## Scientific Objectives

This work is structured around three main objectives:

1. **Formal analysis of neural networks**
   - Identify limitations and fragile regions
   - Go beyond global accuracy metrics

2. **Exact compression using BDDs (Binary Decision Diagrams)**
   - Faithfully represent decision logic
   - Significantly reduce memory footprint

3. **Extension to complex scenarios**
   - Multi-intruder situations
   - Closed-loop system analysis

---

## Methodology and Results

### 1. Neural Network Analysis

The goal is not to validate neural networks as a final solution, but to precisely identify their weaknesses.

#### Two-step approach:

- **Global analysis**
  - Based on structured operational properties
  - Verified using formal tools (Marabou, alpha-beta-CROWN, CAISAR)
  - Identification of critical regions

- **Fine-grained local analysis**
  - Point-by-point comparison with LUTs
  - Precise identification of failure cases

Result:  
Identification of regions requiring a **Safety Net** based on LUT subsets.

---

### 2. Exact Compression with BDDs

An alternative approach based on **Binary Decision Diagrams (BDDs)** was developed:

- Binary encoding of states (Gray code)
- Construction using the CUDD library
- Dynamic variable reordering

#### Results:

- Exact equivalence with original LUTs  
- Memory reduction of **45–50%**  
- Embedded-compatible implementation  
- Improved real-time performance  

A C code generation pipeline was also developed.

---

### 3. Formal Verification with BDDs

BDDs enable **exact verification** without approximation.

### Principle:

- Encode properties as logical formulas
- Combine them with system BDDs
- Perform verification using Boolean operations

#### Advantages:

- Generation of concrete counterexamples  
- High interpretability  
- Detection of inconsistencies in LUTs  

Key insight:  
Some properties validated on neural networks are actually **violated** when evaluated on the original LUTs.

---

### 4. Multi-Intruder Extension

Ongoing work extends the approach to multi-intruder scenarios:

- Combination of LUT scores
- Encoding minimum scores with BDDs

Result:
- Feasibility demonstrated
- Not yet fully embedded-compatible

---

### 5. Closed-Loop Verification

Dynamic simulation of the system:

- Integration of BDDs into a simulation environment
- Observation of system behavior over time

#### Observations:

- Overall stability of decisions  
- Presence of unexpected unstable cycles leading to collisions  

Investigation ongoing

---

## Perspectives

This work establishes an approach based on exact symbolic representations for compression, analysis, and verification of ACAS-Xu systems.

### Short-term

- Improve multi-intruder handling  
- Optimize encodings  
- Extend the set of verifiable properties  

### Mid-term

- Full integration into closed-loop simulations  
- Combined symbolic and dynamic analysis  

### Long-term

Development of methodologies for systems that are:

- compact  
- interpretable  
- formally verifiable  

Goal: contribute to the certification of complex autonomous systems in aeronautics and other safety-critical domains.










[Back to main page](https://boniolp.github.io/)
