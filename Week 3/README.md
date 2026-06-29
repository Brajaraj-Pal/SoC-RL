# 📂 Week 3: RL Fundamentals & Environments

This directory contains the completed assignments and exercises for Week 3 of the Summer of Code (SoC) Reinforcement Learning project. This week marked the transition from basic probability to the foundational architecture of RL: **Markov Decision Processes (MDPs)** and simulation environments.

## 🎯 Objective
To formally define sequential decision-making problems using the MDP framework and bridge the gap between theoretical math and programmatic environments (custom-built and Gymnasium).

---

## 📁 Repository Contents

| Notebook | Focus Area | Technical Implementation |
| :--- | :--- | :--- |
| **`01_mdp_formulation.ipynb`** | MDP Foundations | Formalized problems into the 5-tuple $(S, A, R, T, \gamma)$. Constructed 3D transition probability tensors and reward matrices for a recycling robot simulation. |
| **`02_grid_world_env.ipynb`** | Custom Environments | Engineered a 5x5 GridWorld environment class strictly using standard Python/NumPy. Implemented stochastic mechanics (slippery floor), terminal states, and dynamic reward mapping. |
| **`03_returns_and_discount.ipynb`** | Returns & Discounting | Validated the core Bellman equation. Implemented both $O(N)$ backward-pass and $O(N^2)$ forward-pass algorithms to compute discounted returns ($G_t$) for arbitrary reward trajectories. |
| **`04_frozen_lake_exploration.ipynb`** | Gymnasium API | First integration with the `gymnasium` library (`FrozenLake-v1`). Evaluated and plotted the performance of random, deterministic, and safe heuristics to analyze the exploration-exploitation trade-off. |

---

## 🧠 Core Concepts Mastered
* **The MDP 5-Tuple:** Mapping real-world problems (States, Actions, Transition Probabilities, Rewards, Discount Factor).
* **Environment Architecture:** Understanding the internal mechanics of `env.step()` and `env.reset()` before relying on abstraction libraries.
* **Return Calculation:** Understanding how the discount factor ($\gamma$) mathematically bounds infinite series in continuing tasks and dictates the agent's "horizon."
* **Stochasticity:** Handling environments where $P(s' | s, a) < 1.0$.

---

## 🚀 Key Insights & Observations
1. **The "Black Box" of Gym is Just an MDP:** Building the `GridWorld` class from scratch demystified Gym. It proved that environments are simply state machines returning `(next_state, reward, terminated, truncated, info)` based on a predefined transition matrix.
2. **Stochasticity Breaks Determinism:** A perfectly optimized, hardcoded deterministic policy completely fails in a stochastic environment (like the slippery Frozen Lake). The agent must optimize for *expected* returns, factoring in environmental noise.
3. **The Necessity of $\gamma < 1$:** In continuing tasks, setting $\gamma=1$ causes the cumulative return to diverge to infinity, making policy comparison mathematically impossible.
4. **Monte Carlo Variance:** When evaluating a random policy on a stochastic environment, plotting the distribution revealed that the estimate of the win rate requires >1000 episodes to truly stabilize (demonstrating the Law of Large Numbers).

---
*Completed by: **Brajaraj Pal***
