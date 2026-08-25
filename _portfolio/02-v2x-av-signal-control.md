---
title: "Simulation-Based Bidirectional Control between AVs and Adaptive Traffic Signal Control"
excerpt: "Master's Thesis & IABG-MIC Project: DQN-based traffic signal optimization with connected autonomous vehicles via SUMO/TraCI & V2X."
collection: portfolio
date: 2026-01-15
---

## 📌 Project Overview

* **Context**: Master's Thesis at **TUM Asia** & R&D Project with **IABG Industrieanlagen-Betriebsgesellschaft mbH**
* **Location**: Mobility Innovation Campus (MIC), Munich, Germany
* **Keywords**: Autonomous Vehicles (AVs), V2X Communication, SUMO, TraCI, Reinforcement Learning (DQN), Adaptive Signal Control.

---

## 🚦 Core Innovation & Methodology

1. **Bidirectional Coordination Framework**:
   * Integrated connected autonomous vehicle trajectories with roadside unit (RSU) sensors.
   * Enabled real-time bidirectional negotiation between oncoming AVs and traffic signal controllers.

2. **SUMO/TraCI Microscopic Simulation**:
   * Built high-fidelity microscopic simulation environments mirroring the MIC test site geometry and real-world V2X message flows (SPaT, MAPEM, CAM/BSM).
   * Automated co-simulation pipelines using Python and TraCI APIs.

3. **DQN-Based Adaptive Signal Control**:
   * Formulated signal phase selection as a Markov Decision Process (MDP).
   * Designed reward functions balancing overall intersection throughput, individual vehicle delay, and queue length.
   * Validated robustness under varying traffic demands (peak/off-peak) and mixed V2X penetration rates (0% to 100%).
