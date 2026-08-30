---
title: "Conditional Effects of Connected-Vehicle Requests in Reinforcement-Learning Traffic Signal Control"
excerpt: "A 2,730-run factorial evaluation disentangling queue-responsive RL adaptation from connected-vehicle request conditioning under 2D crossed-bootstrap uncertainty analysis."
collection: portfolio
date: 2026-06-15
header:
  teaser: "request_conditioning_effect.png"
---

<p align="center">
  <img src="/images/request_conditioning_effect.png" alt="Request Conditioning Effect" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 14px rgba(0,0,0,0.12);" />
  <br/>
  <em><b>Figure 1:</b> Paired differences ($\text{Full DQN} - \text{Queue-only DQN}$) across 21 demand $\times$ penetration conditions with 95% 2D Crossed-Bootstrap error bars (50,000 resamples).</em>
</p>

## 📌 Research Overview

Connected vehicles (CVs) can transmit upstream kinematics and priority requests to roadside traffic signal controllers. While reinforcement learning (RL) has shown promise in adaptive traffic signal control, standard literature often conflates **queue-responsive adaptation** with the **marginal value of vehicle-to-infrastructure (V2I) request conditioning**.

This research addresses a fundamental scientific question:
> **Does an upstream connected-vehicle request mechanism provide reproducible operational improvements over queue-responsive adaptation alone, or does the observed benefit stem primarily from the adaptive timing policy?**

---

## 🔬 Controlled Factorial Design & Benchmark Protocol

* **Benchmark Scale**: **2,730 one-hour simulation runs** conducted in Eclipse SUMO on a site-derived 4-approach intersection from the Munich Mobility Innovation Center (MIC).
* **Controlled DQN Ablations**: Matched comparison between a **Request-Aware Deep Q-Network (Full DQN)** and an exact **Queue-Only DQN Ablation** sharing identical network architectures, base congestion objectives, training schedules, and 10–20s green-time action shields.
* **Multi-Axis Uncertainty Modeling**: 2-dimensional **Crossed-Bootstrap protocol** (50,000 resamples) independently resampling across 5 training realizations and 10 paired traffic realizations.
* **Multi-Condition Generalization**: Stress-tested across 21 conditions (3 demand levels: 700, 1,000, 1,300 veh/h $\times$ 7 CV market penetrations: 0% to 100%).

---

## 📊 Key Empirical Findings

1. **Adaptivity Advantage**: Both Full and Queue-only DQN substantially outperform Fixed-time, Actuated, and Max-pressure baselines across all 21 conditions (all 63 crossed-bootstrap 95% CIs exclude zero).
2. **Request Fragility**: Adding requests does not monotonically improve performance. At nominal demand (1,000 veh/h), Full DQN exhibits longer queues than Queue-only DQN across 0%–80% penetrations.
3. **Demand Inversion**: The marginal effect of request conditioning flips sign with demand level: beneficial under low demand ($700$ veh/h at 20% and 80%), but detrimental or neutral under nominal and saturated regimes.
4. **Approval Asymmetry**: Trained policies approve 75%–81% of HOLD requests but only 27%–37% of SWITCH requests.
5. **Retraining Dispersion**: Training stochasticity dominates traffic stochasticity in specific regions (e.g. 50% penetration), causing wide confidence bands due to outlier policy convergence.

---

## 🔗 Resources & Publications

* **Publication Page**: [View Publication Details](/publication/2026-cv-request-rl-traffic-signal-control)
* **Full Manuscript (13 Pages PDF)**: [Download PDF](/files/Conditional_Effects_of_Connected_Vehicle_Requests.pdf)
* **GitHub Repository**: [AnXu-ITS/cv-request-dqn-tsc](https://github.com/AnXu-ITS/cv-request-dqn-tsc)
