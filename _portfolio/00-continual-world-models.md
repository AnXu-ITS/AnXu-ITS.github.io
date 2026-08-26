---
title: "Toward Continually Growing World Models: An OaK-Inspired Architecture for Learned Abstraction and Planning"
excerpt: "Structural Continual World Modeling (SCWM) operationalizing Richard Sutton's OaK architecture and FC-STOMP lifecycle to overcome catastrophic forgetting and plasticity loss in lifelong world models."
collection: portfolio
date: 2026-02-25
header:
  teaser: "scwm-architecture.png"
---

<p align="center">
  <img src="/images/scwm-architecture.png" alt="SCWM Architecture" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 14px rgba(0,0,0,0.12);" />
  <br/>
  <em><b>Figure 1:</b> The Structural Continual World Modeling (SCWM) architecture combining a Fast Online Interaction Loop (1-step latent dynamics) with a Slow Structural Continual Loop (OaK FC-STOMP progression).</em>
</p>

## 📌 Project Overview

Learned world models increasingly empower autonomous agents to predict transitions, imagine rollouts, and plan behaviors in complex environments. However, conventional continual world modeling paradigms predominantly formulate lifelong adaptation along a single parametric axis: updating neural network weights ($\theta_t \to \theta_{t+1}$) over a static, fixed-dimensional latent substrate and a fixed single-step temporal granularity. When deployed in non-stationary or open-ended environments, this parameter-only adaptation is vulnerable to loss of plasticity, capacity saturation, and compounding rollout errors over extended horizons.

In this project, we formulate **Structural Continual World Modeling (SCWM)**, introducing an explicit **structural adaptation axis** ($\mathcal{K}_t \to \mathcal{K}_{t+1}$) grounded in Richard Sutton's **OaK architecture** and its **FC-STOMP** lifecycle (**F**eature Construction $\to$ **S**ub**T**ask $\to$ **O**ption $\to$ **M**odel $\to$ **P**lanning).

---

## 🏛️ Dual-Loop Architecture

The SCWM framework coordinates two coupled dynamical loops operating across complementary time scales:

1. **Fast Online Interaction Loop (1-Step Latent Dynamics)**:
   * Encodes continuous observations into latent state $z_t = E_\phi(o_{\le t})$.
   * Dynamically augments the state vector with discovered features: $\tilde{z}_t = [z_t^\top, \mathcal{F}_t(z_t)]^\top$.
   * Executes 1-step primitive dynamics $p_\theta(\tilde{z}_{t+1}, r_{t+1} \mid \tilde{z}_t, a_t)$ and multi-scale planning over hybrid actions $\mathcal{A}^+_t = \mathcal{A} \cup \mathcal{O}_t$.

2. **Slow Structural Continual Loop (OaK FC-STOMP Progression)**:
   * **(F) Feature Construction**: Persistent prediction surprises trigger constructive units $f_{\text{new}} \in \mathcal{F}_{t+1}$.
   * **(S) SubTask Formulation**: Induces reward-respecting subtasks $g_i = (C_t = R_t, z_i)$ with terminal stopping bonuses.
   * **(O) Option Learning**: Acquires closed-loop temporal skills $\pi_i(a \mid \tilde{z})$ and termination conditions $\beta_i(\tilde{z})$.
   * **(M) Option Models**: Learns jump-ahead predictive models $\mathcal{M}_{o_i}: (\tilde{z}_t, o_i) \mapsto (\hat{\tilde{z}}_{t+\tau}, \hat{R}_{t:t+\tau}, \hat{\tau})$.
   * **(P) Multi-Scale Planning**: Replaces compounding 1-step rollouts with temporally abstracted $\tau$-step jumps.
   * **Utility Lifecycle (GrowPrune)**: Computes multi-objective utility $U(k) = \lambda_1 U_{\text{pred}} + \lambda_2 U_{\text{plan}} + \lambda_3 U_{\text{reuse}} - \lambda_4 C_{\text{comp}}$ to retain valuable abstractions and prune redundant representations.

---

## 🔗 Links & Resources

* 📄 **Publication Details**: [View Paper Page](/publication/2026-oak-continual-world-model)
* 🌐 **Zenodo DOI**: [10.5281/zenodo.22103257](https://doi.org/10.5281/zenodo.22103257)
* 💻 **GitHub Repository**: [AnXu-ITS/OaK-World-Model](https://github.com/AnXu-ITS/OaK-World-Model)
* 📥 **PDF Download**: [Download Preprint PDF](/files/Toward_Continually_Growing_World_Models_Preprint.pdf)
