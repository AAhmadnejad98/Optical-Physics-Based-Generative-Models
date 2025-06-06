# Optical-Physics-Based-Generative-Models
Optical Physics-Based Generative Models


## 🚀 Overview

This repository provides a comprehensive implementation of **physics-inspired generative models** based on both **linear and nonlinear optical physics equations**. We bridge the rich mathematical structure of optical wave and ray equations with modern AI, enabling efficient and interpretable generative models.

The framework includes:
- Linear and nonlinear forms of the **Helmholtz equation**, **dissipative wave equation**, and **Eikonal equation**
- Nonlinear effects such as **Kerr nonlinearity**, **cubic-quintic interactions**, and **intensity-dependent refractive index**
- Robust, high-quality generative sampling for synthetic data and real-world images
- Tools for both generative modeling and physics inverse problems

---

## 📖 Paper

> Ahmadnejad, A., Koohi, S. (2025). *Optical Physics-Based Generative Models*.  
> [Download PDF](https://arxiv.org/pdf/2506.04357v1)  


---

## ✨ Key Features

- **Unified PDE-based generative modeling:**  
  All models describe probability flows as solutions to optical wave equations.

- **Linear & nonlinear physics:**  
  - Linear: Helmholtz, dissipative wave, Eikonal  
  - Nonlinear: Kerr (cubic), cubic-quintic, intensity-dependent refractive index

- **Superior sample quality & efficiency:**  
  - Nonlinear models achieve FID 0.0089 (vs 1.09 for linear, MNIST)
  - Up to **71% fewer parameters**, 30–50% less training time

- **Flexible, modular codebase:**  
  - Finite difference, split-step Fourier, Runge-Kutta, WENO methods
  - Perfectly matched layer (PML) boundary conditions

- **Extensive experiments:**  
  - Scripts for synthetic datasets and MNIST
  - Visualizations: density evolution, velocity fields, Green’s functions

- **Inverse problems:**  
  - Soliton dynamics, caustic detection, adaptive wavefront control, refractive index reconstruction

---

## 🖥️ Installation

1. **Clone the repository:**
   ```bash
   git clone https://github.com/yourusername/optical-generative-models.git
   cd optical-generative-models


Somayyeh Koohi: koohi@sharif.edu

📝 License
This repository is licensed under the MIT License. See LICENSE for details.
