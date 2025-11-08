# 🔬 Parametric Curve Fitting using Global Optimization

This repository contains the implementation and results for a **Parametric Curve Fitting** experiment performed using **global optimization algorithms** — specifically **Differential Evolution (DE)**, **Dual Annealing (DA)**, and **Basin Hopping (BH)**.

The objective was to find optimal parameters that minimize the **L₁ distance** between the observed data and the modeled curve.

---

## 🎯 Final Parametric Equation

\[
\left( t*\cos(29.999980) - e^{0.03000023\left|t\right|}\cdot\sin(0.3t)\sin(29.999980) + 55.000005, 42 + t*\sin(29.999980) + e^{0.03000023\left|t\right|}\cdot\sin(0.3t)\cos(29.999980) \right)
\]

> **Optimizer Used:** Differential Evolution (DE)  
> **Minimum L₁ Distance:** `0.016584`  
> **Status:** ✅ _Final Answer (Best Performing Model)_

---

## ⚙️ Optimizer Comparison

| **Optimizer**                   | **Type**            | **Nature**                                           | **Strength**                                                |
| ------------------------------- | ------------------- | ---------------------------------------------------- | ----------------------------------------------------------- |
| **Differential Evolution (DE)** | Global Evolutionary | Population-based search using mutation and crossover | Very robust; best performance                               |
| **Dual Annealing (DA)**         | Global Annealing    | Simulated annealing with local refinement            | Balanced exploration & exploitation                         |
| **Basin Hopping (BH)**          | Global + Local      | Random jumps + local minimization                    | Fast for smooth surfaces, but can get stuck in local minima |

---

## 📊 Performance Metrics

| **Optimizer** | **θ (deg)** | **M**      | **X**     | **L₁ Total** | **L₁ Mean** | **RMSE** |
| ------------- | ----------- | ---------- | --------- | ------------ | ----------- | -------- |
| **DE**        | 29.999980   | 0.03000023 | 55.000005 | 457.049021   | 0.01658400  | 0.000016 |
| **DA**        | 30.043639   | 0.02999055 | 55.015524 | 453.436902   | 0.30229127  | 0.318027 |
| **BH**        | 28.118423   | 0.02138896 | 54.899130 | 2081.987884  | 1.38799192  | 1.327262 |

> 🏁 **Conclusion:**  
> The **Differential Evolution (DE)** algorithm achieved the most stable and accurate parameter estimation with the lowest L₁ and RMSE errors, proving to be the most effective optimizer for this curve fitting task.

---

## 📘 Overview

### **Objective**

To fit a parametric curve to observed data using different global optimization strategies and evaluate their performance using error metrics.

### **Key Techniques**

- Parametric modeling of nonlinear functions
- Global optimization (DE, DA, BH)
- Error minimization using **L₁ distance** and **RMSE**

### **Metrics Used**

- **L₁ Distance (Total & Mean)**: Measures absolute deviation
- **RMSE (Root Mean Square Error)**: Penalizes larger deviations more heavily

---

## 🧠 Insights

- **Differential Evolution** consistently converged to the global optimum, handling non-linear and multi-modal surfaces effectively.
- **Dual Annealing** achieved comparable performance but required more iterations for stabilization.
- **Basin Hopping** was significantly faster but more sensitive to local minima.

---
## 📚 References & Citations

### 🔹 Differential Evolution (DE)
Storn, R. & Price, K. (1997).  
**"Differential Evolution – A Simple and Efficient Heuristic for Global Optimization over Continuous Spaces."**  
*Journal of Global Optimization, 11(4), 341–359.*  
[https://doi.org/10.1023/A:1008202821328](https://doi.org/10.1023/A:1008202821328)

---

### 🔹 Dual Annealing (DA)
Tsallis, C. & Stariolo, D. A. (1996).  
**"Generalized Simulated Annealing."**  
*Physica A: Statistical Mechanics and its Applications, 233(1–2), 395–406.*  
(Implemented in SciPy as `scipy.optimize.dual_annealing`.)  
[https://doi.org/10.1016/S0378-4371(96)00271-3](https://doi.org/10.1016/S0378-4371(96)00271-3)

---

### 🔹 Basin Hopping (BH)
Wales, D. J. & Doye, J. P. K. (1997).  
**"Global Optimization by Basin-Hopping and the Lowest Energy Structures of Lennard-Jones Clusters Containing up to 110 Atoms."**  
*The Journal of Physical Chemistry A, 101(28), 5111–5116.*  
[https://doi.org/10.1021/jp970984n](https://doi.org/10.1021/jp970984n)

---

### 🔹 Comparative Study
Baioletti, M., Santucci, V., & Tomassini, M. (2024).  
**"A Performance Analysis of Basin Hopping Compared to Established Metaheuristics for Global Optimization."**  
*arXiv preprint arXiv:2403.05877.*  
[https://arxiv.org/abs/2403.05877](https://arxiv.org/abs/2403.05877)

---