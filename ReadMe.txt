Quantum Optimization and Benchmarking Framework
Author: Kushal Anjaria Date: July 2025 Location: Anand, Gujarat, India
This project is organized into two primary folders:
1.	Orchestration Framework (“Software” folder): Contains the complete, modular implementation of the hybrid quantum optimization framework.
2.	Comparative Analysis (“Comparison” folder): Contains scripts that benchmark the orchestration philosophy against alternative approaches inspired by recent research papers.
________________________________________
1. Orchestration Framework
This part of the project implements a novel hybrid optimization framework designed to find robust parameters for noisy quantum circuits. It demonstrates noise impact, mitigation, and the full optimization process.
Files
•	orchestrator.py: The main entry point with a user menu to run the different modules.
•	module_noise_simulation.py: Module 1 - Visualizes the impact of noise on a quantum circuit by comparing ideal and noisy outputs.
•	module_noise_aware_opt.py: Module 2 - Demonstrates noise mitigation techniques like Zero-Noise Extrapolation (ZNE).
•	module_hybrid_opt.py: Module 3 & 4 - The full implementation of the hybrid optimizer that integrates Ant Colony Optimization (ACO), Particle Swarm Optimization (PSO), a Genetic Algorithm (GA), and the Bee Algorithm (BA).
How to Run
1.	Install dependencies:
Bash
pip install pennylane numpy matplotlib scipy
2.	Run the orchestrator:
Bash
python orchestrator.py
Follow the interactive menu to select and run any module.
________________________________________
2. Comparative Analysis & Benchmarking
This part of the project compares the hybrid orchestration philosophy against other state-of-the-art methods, particularly Differentiable Quantum Architecture Search (DQAS), on a standard quantum chemistry problem (VQE for H₂).
Files
•	Paper1.pdf & paper11.py: A conceptual visualization comparing a fixed orchestrator (ensemble of operators) with an adaptive selection method inspired by the Deep Reinforcement Learning approach in the paper.
•	Paper2.pdf & paper2.py: A script inspired by the paper on Differentiable Quantum Architecture Search (DQAS). It compares a traditional VQE (fixed ansatz, optimized parameters) with a DQAS approach that learns both the circuit architecture and its parameters.
•	overall.py: The primary benchmarking script. It evaluates a 
Proposed Orchestrator (simplified GA+PSO hybrid) against standard optimizers (Adam, GA, PSO) for the H₂ VQE problem under various noise levels.
How to Run
1.	Install dependencies (if not already installed):
Bash
pip install pennylane numpy matplotlib pandas scipy
2.	Run the individual analyses:
o	Paper 1 Concept:
Bash
python paper11.py
This will show a 2x2 plot comparing the optimization strategies.
o	Paper 2 (DQAS) Concept:
Bash
python paper2.py
This will show a bar chart comparing the final VQE energies.
o	Full Benchmark:
Bash
python overall.py
This will run the full benchmark, print a summary table to the console, and save two image files (vqe_convergence_plot.png, vqe_noise_robustness_plot.png) and a results table (vqe_benchmark_results.csv).

