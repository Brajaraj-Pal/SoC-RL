# 📂 Week 2: Mathematical Foundations of RL

This directory contains the completed exercises for Week 2 of the Summer of Code (SoC) Reinforcement Learning project. The focus this week was on establishing the rigorous mathematical grounding required for advanced RL algorithms, specifically covering probability, stochastic processes, and the exploration-exploitation dilemma.

## 🎯 Objective
To master the statistical and mathematical models that underpin agent behavior and environment dynamics, bridging the gap between theoretical probability and programmatic simulations.

---

## 📁 Repository Contents & Technical Execution

| Focus Area | Technical Implementation |
| :--- | :--- |
| **Probability & Statistics** | Implemented foundational probability distributions and expected value calculations essential for stochastic environments. |
| **Markov Chains** | Simulated discrete-time Markov Chains, mapped transition matrices, and verified stationary distributions programmatically. |
| **Multi-Armed Bandits** | Coded the classic k-armed bandit problem to analyze the fundamental trade-off between exploration and exploitation. |
| **`04_random_walk.ipynb`** | Simulated 1D and 2D random walks. Implemented the classic Sutton & Barto 5-state random walk environment, successfully validating empirical simulation results against true analytical state values ($V(s)$). |

---

## 🧠 Core Concepts Mastered
* **Stochastic Processes:** Understanding how sequences of random variables evolve over time without deterministic outcomes.
* **Transition Matrices:** Using linear algebra (NumPy) to compute the probability of moving from state $i$ to state $j$.
* **Analytical vs. Empirical:** Bridging mathematical theory with Monte Carlo simulations to prove that large-sample simulations converge to true analytical probabilities.
* **First Passage Time:** Calculating and plotting the distribution of steps required for a stochastic agent to reach a specific target state.

---

## 🚀 Key Insights & Observations
1. **Unbiased vs. Biased Walks:** Simulating random walks proved that even a slight bias ($p > 0.5$) drastically alters the long-term trajectory and variance of an agent's position.
2. **Sutton & Barto 5-State Verification:** By calculating the analytical values of the 5 non-terminal states ($1/6, 2/6, 3/6, 4/6, 5/6$) and running a 2000-episode empirical simulation, I verified that programmatic rollouts perfectly converge to the mathematical truth.
3. **Law of Large Numbers:** Across all exercises, increasing the number of simulation steps explicitly demonstrated the reduction of variance, a critical concept for stabilizing RL training loops.

---
*Completed by: **Brajaraj Pal***
