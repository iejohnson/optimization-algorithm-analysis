# Optimization Methods Comparison
**Authors:** Isabella Johnson & Mia Bella Rodriguez  
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

## Key Findings
- Newton's method converges in 1–2 iterations by leveraging exact Hessian information
- Gauss-Newton is remarkably effective on the Rosenbrock (3 iterations) due to its structured least-squares formulation
- First-order methods struggle significantly on the ill-conditioned Rosenbrock, failing to converge within 10,000 iterations
- Damped Gauss-Newton trades a few extra iterations for better stability via backtracking

## Tools
Python, NumPy, Matplotlib, Seaborn, Jupyter Notebook
