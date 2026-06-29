# 📂 Week 4: Dynamic Programming & Planning

This directory contains the completed assignments for Week 4 of the Summer of Code (SoC) Reinforcement Learning project. This week focused on **Dynamic Programming (DP)**, moving from simple environment interaction to solving for optimal policies given a known model of the environment.

## 🎯 Objective
To master the fundamental DP algorithms that compute optimal policies ($π^*$) and value functions ($V^*$) by exploiting the environment's internal transition dynamics ($P(s'|s,a)$).

---

## 📁 Repository Contents

| Notebook | Focus Area | Technical Execution |
| :--- | :--- | :--- |
| **`01_policy_evaluation.ipynb`** | Policy Evaluation | Implemented iterative updates using the Bellman Expectation Equation. Compared standard vs. in-place updates to demonstrate convergence speed. |
| **`02_policy_iteration.ipynb`** | Policy Iteration | Developed the full Policy Iteration cycle (Evaluation + Improvement). Implemented a "Modified Policy Iteration" challenge with truncated evaluation. |
| **`03_value_iteration.ipynb`** | Value Iteration | Implemented the Bellman Optimality Equation. Visualized 3D value topology and implemented asynchronous value iteration. |
| **`04_frozen_lake_dp.ipynb`** | DP on Gymnasium | Applied DP to the `FrozenLake-v1` environment. Transitioned to model-free learning by solving the environment using Tabular Q-Learning without `env.P`. |

---

## 🧠 Core Concepts Mastered
* **Policy Evaluation:** Calculating the value $V^π$ of a fixed policy using iterative sweeps.
* **Policy Improvement:** Using the Policy Improvement Theorem to derive a better policy greedily from $V^π$.
* **Value Iteration:** Combining evaluation and improvement into a single update step using the Bellman Optimality Equation.
* **Truncated & Asynchronous Updates:** Breaking the requirement of "full sweeps" to speed up convergence in large state spaces.
* **Model-Based vs. Model-Free:** Understanding the shift from using `env.P` (DP) to learning through experience (Q-Learning).

---

## 🚀 Key Insights & Observations
1. **Convergence Trade-offs:** Standard Policy Iteration is often faster in terms of *iteration count*, but Value Iteration is often faster in *total computational time* due to the simpler inner loop.
2. **In-place Updates:** Updating values in-place propagates information through the state space significantly faster than using a `V_new` copy, as it utilizes "fresher" data within the same sweep.
3. **The Power of Truncation:** Modified Policy Iteration proved that we don't need perfect evaluation to improve a policy; even a few steps of calculation are sufficient to nudge the policy toward optimality.
4. **The Model-Free Shift:** Solving `FrozenLake` with Q-Learning without accessing `env.P` provided a direct bridge to Week 5, highlighting how agents can learn through trial and error rather than pure mathematical prediction.

---
*Completed by: **Brajaraj Pal***
