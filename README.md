# 🚀 SoC-RL: Reinforcement Learning (Seasons of Code)

Welcome to the repository for my progress in the **Reinforcement Learning** track of Seasons of Code (SoC) 2026, IIT Bombay. This project, mentored by **Aditya Sanapala**, covers the transition from mathematical probability models to practical RL planning and learning.

## 📊 Progress Roadmap (As of June 29, 2026)

| Week | Focus Area | Status | Technical Core |
| :--- | :--- | :--- | :--- |
| **Week 1** | Python & Scientific Computing | ✅ Done | NumPy, Pandas, Matplotlib, Colab workflows. |
| **Week 2** | Markov Chains & Random Walks | ✅ Done | Transition matrices, stationary distributions, 1D/2D walks. |
| **Week 3** | RL Fundamentals & MDPs | ✅ Done | MDP 5-tuple, custom `GridWorld` engineering, return ($G_t$) calculation. |
| **Week 4** | Dynamic Programming (DP) | ✅ Done | Policy Evaluation, Policy Iteration, Value Iteration, FrozenLake DP. |
| **Week 5** | Model-Free Learning | 🚧 Active | Temporal Difference (TD) Learning, Q-Learning, SARSA. |

---

## 🛠️ Repository Structure

* **`Week 1/`**: Python/NumPy/Matplotlib initialization and basic scientific computing exercises.
* **`Week 2/`**: Simulation of Markov Chains, Multi-Armed Bandits, and Random Walk behaviors.
* **`Week 3/`**: MDP formulation, implementation of `GridWorld` from scratch, and Bellman Equation validation.
* **`Week 4/`**: Planning via Dynamic Programming—Policy Iteration (standard/modified) and Value Iteration for optimal policy extraction.

---

## 🧠 Technical Milestones

### 1. Planning & Optimization (Model-Based)
* **MDP Engineering:** Built custom transition tensors and reward matrices to simulate environment dynamics[cite: 3, 5].
* **Policy Evaluation:** Implemented in-place updates, demonstrating convergence advantages over standard sweeps[cite: 3].
* **Policy Iteration:** Engineered Modified Policy Iteration (MPI) with truncated evaluation, proving that exact convergence is not necessary for successful policy improvement[cite: 3].
* **Value Iteration:** Achieved 100% win rate on non-slippery `FrozenLake-v1` and performed 3D topological mapping of optimal value functions $V^*$[cite: 4, 5].

### 2. Transition to Model-Free Learning
* **Bypassing the Model:** Moved from relying on `env.P` (DP) to implementing tabular **Q-Learning** via `env.step()`[cite: 5].
* **Stochastic Handling:** Engineered $\epsilon$-greedy strategies to manage high-variance outcomes in `FrozenLake-v1` (slippery version), maintaining agent stability without knowing transition dynamics[cite: 5].

---
*Maintained by: **Brajaraj Pal***
*Last updated: 29 June 2026*
