---
title: "Driving World Models for Closed-Loop Simulation and Reactive Traffic Worlds"
excerpt: "A comprehensive survey formulating a Simulation-Closure framework and claim-specific validity stack for learned driving world models."
collection: portfolio
date: 2026-08-30
header:
  teaser: "figure1_feedback_paths.png"
---

<p align="center">
  <img src="/images/figure1_feedback_paths.png" alt="Three Feedback Regimes" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 14px rgba(0,0,0,0.12);" />
  <br/>
  <em><b>Figure 1:</b> Three feedback regimes for learned driving simulation: Replay-Constrained, Ego-Responsive, and Traffic-Reactive.</em>
</p>

## 📌 Project Overview

Every driving log records one realized future. Once a candidate policy brakes, merges, or yields differently, the log no longer specifies what the ego vehicle will do or how surrounding road users will respond. Learned driving environments are increasingly used to generate this unobserved continuation, but terms such as *world model*, *closed loop*, *action conditioned*, and *reactive* are often applied to systems with materially different feedback relations.

This project delivers a comprehensive research survey and open resource repository clarifying the exact scientific capabilities and validity boundaries of learned driving world models.

---

## 🔄 The Simulation-Closure Framework

We formalize three distinct feedback regimes across learned driving simulators:

1. **Replay-Constrained:** The returned observation or queried viewpoint may change, but the behavioral future remains prescribed by a log or external trajectory.
2. **Ego-Responsive:** Ego control commands genuinely modify realized ego motion, but surrounding non-ego actors remain anchored or non-reactive.
3. **Traffic-Reactive:** Relevant non-ego actors actively yield, overtake, or brake in response to counterfactual ego trajectory deviations.

<p align="center">
  <img src="/images/figure4_validity_stack.png" alt="Claim-Specific Validity Layers" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 14px rgba(0,0,0,0.12);" />
  <br/>
  <em><b>Figure 2:</b> Claim-specific validity hierarchy from local observation fidelity up to network transportation scale.</em>
</p>

---

## 📊 5-Layer Validity Hierarchy

* **Observation Fidelity:** Evaluated on held-out viewpoints, geometric consistency, and temporal multi-sensor alignment.
* **Ego Controllability:** Evaluated by target-to-realized tracking accuracy and kinematic feasibility across commands.
* **Traffic-Response Validity:** Evaluated via matched counterfactual ego interventions and repeated multi-agent rollouts.
* **Closed-Loop Policy Validity:** Evaluated through cross-simulator transfer, benchmark stability, and real deployment correlation.
* **Transportation Scale:** Evaluated by demand-conditioned network metrics (queues, shockwaves, macroscopic throughput).

---

## 🔗 Resources & Publications

* **SSRN Working Paper**: [SSRN: 7383662](https://ssrn.com/abstract=7383662) | [DOI: 10.2139/ssrn.7383662](https://dx.doi.org/10.2139/ssrn.7383662)
* **Publication Page**: [View Publication Details](/publication/2026-driving-world-models-survey)
* **Preprint PDF (24 pages)**: [Download PDF](/files/From_Foresight_to_Reactive_Traffic_Worlds_Survey.pdf)
* **GitHub Repository**: [AnXu-ITS/driving-world-models-survey](https://github.com/AnXu-ITS/driving-world-models-survey)
* **Editable Figures**: [Download PPTX Sources](https://github.com/AnXu-ITS/driving-world-models-survey/tree/main/editable_figures)
