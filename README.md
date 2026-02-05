# Turkish Airlines Profit Models: Examples in Linear Optimization

**MATH 441 – Mathematical Modelling: Discrete Optimization Problems**
University of British Columbia · February 2026
Umay Gokturk, Erhan Asad Javed, Luna Kim

## Overview

This project applies linear optimization techniques to two core airline profit problems using Turkish Airlines as a case study, then combines them into a single profit-maximization model via weighted-sum multi-objective optimization.

## Models

### 1. Revenue Model (`revenue_model.ipynb`)
Maximizes ticket revenue by optimizing seat allocation across four fare classes (EcoFly, FlexFly, PrimeFly, Business), subject to cabin capacity and fixed demand constraints.

### 2. Fleet Assignment Model (`fleet_model.ipynb`)
Minimizes total operating cost (fuel, crew, and maintenance) by assigning aircraft types to flight legs. Constraints include flight coverage, crew-hour limits, range feasibility, and round-trip pairing consistency.

### 3. Profit Maximization Model (`profit_maximization_model.ipynb`)
Combines revenue maximization and cost minimization into a single objective using the weighted-sum method:

$$\text{Maximize} \quad \lambda \cdot \text{Revenue} - (1 - \lambda) \cdot \text{Cost}$$

Includes capacity constraints tied seat sales to the fleet type assigned to each flight. The relationship between revenue generation and cost efficiency can be observed by adjusting the weights \lambda.

## Requirements

- Python 3.10+
- `cvxpy`, `numpy`, `pandas`, `scipy`, `matplotlib`


## Limitations

- Fixed demand estimates (no stochastic or dynamic pricing)
- No network flow, repositioning, or scheduling included

## References

- Kim & de Weck (2006). *Adaptive weighted sum method for multiobjective optimization.* Structural and Multidisciplinary Optimization, 31(2), 105–116.
- Ozdemir, Basligil & Nalbant (2012). *Optimization of fleet assignment: A case study in Turkey.* IJOCTA, 2(1), 59.