# F0 Explorer – Crack Tensor & Fabric Tensor on 2D

This repository provides the **F0 Explorer**, a standalone HTML/JavaScript application for 
generating 2-D synthetic crack-trace networks and computing crack-density measures based 
on the fabric tensor (Oda, 1982) and crack tensor (Oda et al., 2002).

---

## Overview

F0 Explorer allows users to:

- Generate synthetic 2-D fracture trace patterns
- Control fracture number, length, orientation, and randomness
- Compute the scalar crack-density measure **F₀ = Σ L² / A**
- Visualize fracture orientation distributions
- Export trace data (TXT) and canvas images (PNG)
- Run entirely in a browser with no installation or dependencies

---

## Background Theory

### Fabric Tensor (Oda, 1982)

Oda (1982) introduced the **fabric tensor** to quantify the geometric characteristics of 
discontinuities (e.g., joints, cracks).  
Key concepts include:

- The **first invariant** of the fabric tensor represents crack intensity  
- The **deviatoric part** describes anisotropy associated with preferred orientations  
- The measure is general and applicable to discontinuous geological materials

### Crack Tensor (Oda et al., 2002)

Oda et al. (2002, JGR) extended the fabric concept to define the **crack tensor**, which 
incorporates crack orientation and size:

- Only even-rank tensors (0th, 2nd, 4th) are non-zero  
- The **0th-rank tensor F₀** represents crack density  
- The **2nd-rank tensor Fᵢⱼ** describes directional anisotropy  
- The **4th-rank tensor** is relevant to mechanical and transport coupling
- F₀ is linearly related to porosity when aperture scales with radius

### Relation to F0 Explorer

The F0 Explorer computes:

    F₀ = Σ L² / A

This formula is the 2-D analog of the r³‑weighted crack-density measure defined by 
Oda et al. (2002), where fracture segments are treated as projections of disk-like 
microcracks.

It provides a practical estimator of crack density and anisotropy for 2-D trace maps.

---

## How to Use

### Running the App

Simply open the file:

    F0_Explorer_Ver1.html

in a modern browser (Chrome, Safari, Firefox, Edge).  
No installation is required.

### Exporting Data

The application allows exporting:

- Crack trace coordinates (TXT)
- Canvas as PNG images
- Parameter-controlled synthetic networks

---

## File Structure

    F0_Explorer_Ver1.html   # Main application file

---

## References

Oda, M. (1982). Fabric tensor for discontinuous geological materials. *Soils and Foundations*, 22(4), 96–108.

Oda, M., Katsube, T., & Takemura, T. (2002). Microcrack evolution and brittle failure of Inada granite in triaxial compression tests at 140 MPa. *Journal of Geophysical Research: Solid Earth*, 107(B10), 2233.

---

