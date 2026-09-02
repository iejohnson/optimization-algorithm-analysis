# Optimization Methods Comparison
## Authors
- **Isabella Johnson** — Designed and implemented all code in this repository
- **Mia Bella Rodriguez** — Presented the related textbook section in class
  
**Course:** Optimization | University of Colorado Colorado Springs  
**Date:** Spring 2026

## Overview
Implements and compares six numerical optimization algorithms on two classic test functions, analyzing convergence speed, iteration count, and behavior under different conditions.

## Functions Tested
- **Quadratic:** f(x,y) = x² + 10y²
- **Rosenbrock:** f(x₁,x₂) = 100(x₂ - x₁²)² + (1 - x₁)²

## Methods Implemented
| Method | Iterations (Quadratic) | Iterations (Rosenbrock) |
|---|---|---|
| Constant Step Size | 153 | 10,000 (did not converge) |
| Backtracking Line Search | 84 | 10,000 (did not converge) |
| Exact Line Search | 15 | — |
| Newton's Method | 1 | 2 |
| Gauss-Newton | 22 | 3 |
| Damped Gauss-Newton | 22 | 13 |

## Results
Convergence iterations and contour plots for quadratic:
<img width="983" height="584" alt="image" src="https://github.com/user-attachments/assets/dcd43daa-b581-4d12-bfa3-f130f78acb69" />

<img width="1784" height="1080" alt="image" src="https://github.com/user-attachments/assets/d2a2f2b5-7be1-40d3-9549-d741a0384ba9" />



Convergence iterations and contour plots for Rosenbrock:
<img width="984" height="584" alt="image" src="https://github.com/user-attachments/assets/fba6a293-9eb1-41cb-8ba0-09491a82aefb" />

<img width="1784" height="1080" alt="image" src="https://github.com/user-attachments/assets/c2c5dd33-d731-430b-be9e-c57a91ac54a9" />

## Key Findings
- Newton's method converges in 1–2 iterations by leveraging exact Hessian information
- Gauss-Newton is remarkably effective on the Rosenbrock (3 iterations) due to its structured least-squares formulation
- First-order methods struggle significantly on the ill-conditioned Rosenbrock, failing to converge within 10,000 iterations
- Damped Gauss-Newton trades a few extra iterations for better stability via backtracking

## Tools
Python, NumPy, Matplotlib, Seaborn, Jupyter Notebook
