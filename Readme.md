
---

## 🧠 Methodology

### 1️⃣ Multi-Armed Bandit (MAB) Framework

- Each channel is modeled as an "arm"
- Successful detection of a vacant channel is treated as a "reward"
- Exploration–Exploitation trade-off handled via:

  - **Epsilon-Greedy (Sequential Baseline)**
  - **UCB1 (Parallel Learning-Based Strategy)**

---

### 2️⃣ Simulation Environment

The system is built using a custom event-driven MATLAB simulator.

**Primary Users (PUs):**
- Modeled as a two-state Markov process
- ON (busy) and OFF (idle) durations follow exponential distributions

**Secondary Users (SUs):**
- Packet arrivals follow a Poisson process
- Channel sensing and switching modeled explicitly

**Statistical Validation:**
- Monte Carlo averaging across multiple independent runs
- Ensures statistically stable and meaningful conclusions

---

# 📊 Results

Our simulations validate that intelligent, parallel learning significantly improves CRN performance.

---

### 🔹 Figure 4: Cooperative Sensing Performance (ROC Curve)

*(Trade-off between detection probability and false alarm for OR, AND, and N-out-of-M fusion rules.)*

<p align="center">
  <img src="results/fig4_roc_curve.png" width="600"/>
</p>

---

### 🔹 Figure 5: Channel Finding Delay

*(Parallel UCB1 significantly reduces delay in identifying vacant channels.)*

<p align="center">
  <img src="results/fig5_delay_comparison.png" width="600"/>
</p>

---

### 🔹 Figure 6: Channel Switching Rate

*(UCB1 requires fewer sensing actions, improving stability and efficiency.)*

<p align="center">
  <img src="results/fig6_switching_rate.png" width="600"/>
</p>

---

### 🔹 Figure 7: Network Throughput (Greedy Baseline)

<p align="center">
  <img src="results/fig7_throughput_greedy.png" width="600"/>
</p>

---

### 🔹 Figure 8: Network Throughput (UCB1 Parallel Strategy)

<p align="center">
  <img src="results/fig8_throughput_ucb.png" width="600"/>
</p>

The reduced sensing delay from UCB1 directly translates into improved throughput performance.

---

# ▶️ How to Run the Simulations

## Prerequisites
- MATLAB (Tested on R2020a and later)

---

## Clone the Repository

```bash
git clone https://github.com/YourUsername/cognitive-radio-channel-selection.git
