# Optical-Physics-Based-Generative-Models
Optical Physics-Based Generative Models

🚀 Overview
This repository provides a full implementation of physics-inspired generative models based on both linear and nonlinear optical physics equations. These models connect wave and ray optics to modern AI generation tasks, enabling new approaches that combine physical insight with machine learning.

The framework includes:

Linear and nonlinear Helmholtz, dissipative wave, and Eikonal equations

Nonlinear effects such as Kerr nonlinearity and cubic-quintic interactions

Robust, high-quality generative sampling for images and synthetic data

Tools for both forward generation and inverse problems in nonlinear optics

📖 Paper
Ahmadnejad, A., Koohi, S. (2025). Optical Physics-Based Generative Models.

✨ Key Features
Unified PDE-based generative modeling:
Models probability density flows as solutions to optical wave equations

Supports both linear & nonlinear physics:

Linear: Helmholtz, dissipative wave, Eikonal

Nonlinear: Kerr effect, cubic-quintic, intensity-dependent refractive index

Superior mode separation and sample quality:

Nonlinear models outperform linear ones (e.g., FID score 0.0089 vs. 1.09 on MNIST)

Up to 60–70% parameter reduction and 50% faster training via self-organization

Flexible, modular code:

Finite difference, split-step Fourier, Runge-Kutta, WENO solvers

PML boundary conditions and adaptive time-stepping

Extensive experiments:

Synthetic distributions & MNIST

Visualizations for density evolution, Green’s functions, velocity fields

Inverse problems:

Soliton propagation, caustic detection, adaptive wavefront control, refractive index recovery

🖥️ Installation
Clone the repo:

bash
Copy
Edit
git clone https://github.com/yourusername/optical-generative-models.git
cd optical-generative-models
Install dependencies:

bash
Copy
Edit
pip install -r requirements.txt
Recommended: Python 3.8+

Major dependencies: numpy, scipy, matplotlib, torch (optional: JAX/NumPyro for acceleration)

🔬 Models Implemented
Model Type	Equation (PDE)	Linear/Nonlinear	Nonlinear Term	Unique Feature
Helmholtz	∇²ϕ + k₀²ϕ = 0	Linear	-	Oscillatory wave generation
Dissipative Wave	ϕₜₜ + 2ϵϕₜ - ∇²ϕ = 0	Linear	-	Wave-diffusion transition
Eikonal	ϕₜ +	∇ϕ	² = n²(x)	Linear
Kerr-Helmholtz	∇²ϕ + k₀²ϕ + α	ϕ	²ϕ = 0	Nonlinear
Cubic-Quintic	ϕₜₜ + 2ϵϕₜ - ∇²ϕ + αϕ³ + βϕ⁵ = 0	Nonlinear	Cubic, Quintic	Soliton formation, stabilization
Intensity Eikonal	ϕₜ +	∇ϕ	² = n²(x) + χ	ϕ

📊 Results & Benchmarks
Nonlinear Helmholtz: FID 0.0089 (linear: 1.09), 71% fewer parameters, 50% less training time

Cubic-Quintic Wave: 20–40% better mode coverage, stable soliton formation

Intensity Eikonal: 30–50% fewer steps than classifier guidance; smooth, adaptive sampling

See experiments/ and results/ for scripts, plots, and notebook demos.

🛠️ Usage
Train a model (example)
bash
Copy
Edit
python train.py --model nonlinear_helmholtz --dataset mnist --epochs 100
Sample generation
bash
Copy
Edit
python sample.py --model cubic_quintic_wave --checkpoint checkpoints/model.pt --num_samples 1000
Visualize results
bash
Copy
Edit
python visualize.py --experiment results/exp1/
Notebooks are provided for end-to-end demos:

notebooks/linear_vs_nonlinear.ipynb

notebooks/soliton_simulation.ipynb

🧑‍💻 Repository Structure
bash
Copy
Edit
.
├── models/         # All PDE model definitions and numerical solvers
├── experiments/    # Experiment scripts and configs
├── datasets/       # Data loaders (MNIST, synthetic)
├── notebooks/      # Example Jupyter notebooks
├── results/        # Output figures and logs
├── utils/          # Helper functions and visualization tools
├── requirements.txt
└── README.md
📈 Applications
Generative modeling for images, signals, distributions

Physics-informed inverse problems: soliton dynamics, caustics, refractive index mapping

Benchmarking physical inductive biases for AI

👩‍🔬 Contributing
Pull requests are welcome! For major changes, please open an issue first to discuss what you would like to change or extend (e.g., new physics equation, new dataset).

📄 Citation
If you use this code or find it useful, please cite:

bibtex
Copy
Edit
@article{ahmadnejad2025optical,
  title={Optical Physics-Based Generative Models},
  author={Ahmadnejad, Amirreza and Koohi, Somayyeh},
  journal={arXiv preprint arXiv:xxxx.xxxxx},
  year={2025}
}
📧 Contact
Amirreza Ahmadnejad: amirreza.ahmadnejad@sharif.edu

Somayyeh Koohi: koohi@sharif.edu

📝 License
This repository is licensed under the MIT License. See LICENSE for details.
