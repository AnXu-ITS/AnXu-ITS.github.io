---
title: "Toward Continually Growing World Models: An OaK-Inspired Architecture for Learned Abstraction and Planning"
collection: publications
category: preprints
permalink: /publication/2026-oak-continual-world-model
excerpt: 'A position paper introducing Structural Continual World Modeling (SCWM), operationalizing Richard Sutton’s OaK architecture and FC-STOMP lifecycle to overcome plasticity loss and compounding error in lifelong world models.'
date: 2026-02-25
venue: "Zenodo Preprint / Workshop on Continual World Models, NeurIPS 2026"
paperurl: "https://doi.org/10.5281/zenodo.22103257"
citation: 'Xu, An. (2026). &quot;Toward Continually Growing World Models: An OaK-Inspired Architecture for Learned Abstraction and Planning.&quot; <i>Zenodo Preprint</i>. doi:10.5281/zenodo.22103257.'
header:
  teaser: "scwm-architecture.png"
---

<p align="center">
  <img src="/images/scwm-architecture.png" alt="SCWM Architecture" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 14px rgba(0,0,0,0.12);" />
  <br/>
  <em><b>Figure 1:</b> The Structural Continual World Modeling (SCWM) architecture combining a Fast Online Interaction Loop (1-step latent dynamics) with a Slow Structural Continual Loop (OaK FC-STOMP progression).</em>
</p>

## Abstract

Learned world models increasingly empower autonomous agents to predict transitions, imagine rollouts, and plan behaviors in complex environments. However, conventional continual world modeling paradigms predominantly formulate lifelong adaptation along a single parametric axis: updating neural network weights ($\theta_t \to \theta_{t+1}$) over a static, fixed-dimensional latent substrate and a fixed single-step temporal granularity. When deployed in non-stationary or open-ended environments, this parameter-only adaptation is vulnerable to loss of plasticity, capacity saturation, and compounding rollout errors over extended horizons.

In this position paper, we argue that genuine continual world modeling requires introducing a second, **structural adaptation axis** ($\mathcal{K}_t \to \mathcal{K}_{t+1}$), wherein the model's predictive state abstractions, temporal abstractions, and option models continually grow, evaluate, and reorganize over time. Grounding this dual-axis formulation in Richard Sutton's **OaK architecture** and its **FC-STOMP** lifecycle (**F**eature Construction $\to$ **S**ub**T**ask $\to$ **O**ption $\to$ **M**odel $\to$ **P**lanning), we formulate **Structural Continual World Modeling (SCWM)**. Under SCWM, discovered state features dynamically expand the world model's predictive state representation, inducing reward-respecting subtasks, closed-loop options, and predictive option models, with retention and pruning governed by downstream planning utility. We formulate five falsifiable research hypotheses and an experimental agenda to guide the development of continually growing world models.

---

## 🚀 Key Contributions

1. **Dual-Axis Framework:** Formalized Structural Continual World Modeling (SCWM), augmenting parameter-level adaptation ($\theta_t \to \theta_{t+1}$) with an explicit structural adaptation axis $(\theta_t, \mathcal{K}_t) \to (\theta_{t+1}, \mathcal{K}_{t+1})$.
2. **Constructive Dynamics:** Discovered features $\mathcal{F}_t$ dynamically expand the world model's predictive state representation ($\tilde{z}_t = \Phi_t(z_t)$), inducing reward-respecting subtasks with terminal stopping bonuses, predictive option models, and multi-scale planning.
3. **Actionable Agenda:** Five falsifiable hypotheses (**H1–H5**) and experimental protocols evaluating planning depth, plasticity retention, and Pareto-optimal utility pruning.

---

## 🔗 Links & Resources

* **Zenodo DOI**: [10.5281/zenodo.22103257](https://doi.org/10.5281/zenodo.22103257)
* **GitHub Repository**: [AnXu-ITS/OaK-World-Model](https://github.com/AnXu-ITS/OaK-World-Model)
* **Preprint PDF**: [Download PDF](/files/Toward_Continually_Growing_World_Models_Preprint.pdf)

---

## 📖 BibTeX Citation

```bibtex
@article{xu2026continually,
  title={Toward Continually Growing World Models: An OaK-Inspired Architecture for Learned Abstraction and Planning},
  author={Xu, An},
  journal={Zenodo Preprint},
  year={2026},
  doi={10.5281/zenodo.22103257},
  url={https://doi.org/10.5281/zenodo.22103257},
  note={Workshop on Continual World Models, NeurIPS 2026}
}
```
