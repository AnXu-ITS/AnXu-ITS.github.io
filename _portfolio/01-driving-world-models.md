---
title: "Driving World Models for Closed-Loop Simulation and Responsive Traffic Worlds"
excerpt: "Survey and architectural framework on generative driving world models as learned closed-loop simulators with responsive environmental feedback."
collection: portfolio
date: 2026-06-01
---

## 📌 Project Overview

Traditional autonomous driving simulation often relies heavily on log-replay or heuristic traffic models, which suffer from a fundamental limitation: **lack of reactivity when the ego vehicle executes counterfactual, off-log decisions**. 

This research investigates **Driving World Models (DWMs)** as learned closed-loop simulators, analyzing how generative video/latent world models can synthesize plausible future traffic states and sensor observations conditioned on ego actions.

---

## 🔄 Simulation-Closure Framework

We formulate a three-stage progressive spectrum of simulation closure:
1. **Replay-Constrained**: Replaying recorded background trajectories with static environmental responses.
2. **Ego-Responsive**: The immediate environment (e.g. ego dynamics and viewpoints) updates accurately with ego control inputs.
3. **Traffic-Reactive**: Surrounding dynamic agents (pedestrians, vehicles) reactively yield, overtake, or brake in response to ego deviations from the historical log.

---

## 🏗️ 4-Layer Abstraction Architecture

We abstract closed-loop driving world models into four decoupled layers:
* **World-State Dynamics**: Latent space transitions capturing temporal physical laws.
* **Traffic Response Layer**: Multi-agent behavior synthesis under counterfactual ego actions.
* **Sensor Rendering Layer**: High-fidelity multi-view camera / LiDAR point cloud generation.
* **Policy Interface Layer**: Action conditioning and feedback loop for autonomous driving policy evaluation.

---

## 📊 Comprehensive Evaluation Metric Dimensions

1. **Observation Fidelity**: Photorealism, geometric consistency, and spatio-temporal coherence.
2. **Ego-Response Fidelity**: Dynamic vehicle response and kinematics validity.
3. **Traffic Reactivity**: Plausibility of interactive behaviors (collision avoidance, yielding).
4. **Closed-Loop Validity**: Policy transfer performance from world-model simulation to real-world execution.
