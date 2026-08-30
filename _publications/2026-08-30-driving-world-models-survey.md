---
title: "From Foresight to Reactive Traffic Worlds: A Survey of Driving World Models for Closed-Loop Simulation"
collection: publications
category: preprints
permalink: /publication/2026-driving-world-models-survey
excerpt: 'A comprehensive survey establishing a Simulation-Closure framework (Replay-Constrained, Ego-Responsive, Traffic-Reactive) and a 5-layer validity stack for learned driving world models in closed-loop autonomous driving simulation.'
date: 2026-08-30
venue: "Preprint / Open Research Resource"
paperurl: "https://github.com/AnXu-ITS/driving-world-models-survey"
citation: 'Xu, An, Jin, Zekai, Zhang, Hanrong, Sun, Xiaoning, Zhang, Chengbo, and Yin, Yunfei. (2026). &quot;From Foresight to Reactive Traffic Worlds: A Survey of Driving World Models for Closed-Loop Simulation.&quot; <i>Preprint</i>. https://github.com/AnXu-ITS/driving-world-models-survey.'
header:
  teaser: "figure1_feedback_paths.png"
---

<p align="center">
  <img src="/images/figure1_feedback_paths.png" alt="Three feedback regimes for learned driving simulation" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 14px rgba(0,0,0,0.12);" />
  <br/>
  <em><b>Figure 1:</b> Three feedback regimes for learned driving simulation: Replay-Constrained, Ego-Responsive, and Traffic-Reactive feedback paths under off-log ego interventions.</em>
</p>

## Overview & Motivation

Every driving log records one realized future. Once a candidate policy brakes, merges, or yields differently, the log no longer specifies what the ego vehicle will do or how surrounding road users will respond. Learned driving environments are increasingly used to generate this unobserved continuation, but terms such as *world model*, *closed loop*, *action conditioned*, and *reactive* are often applied to systems with materially different feedback relations.

This survey asks a fundamental functional question:
> **After the ego vehicle departs from the recorded action, what does the environment recompute, can the policy act again, and what conclusion does the reported evidence actually support?**

The central argument is that **visual plausibility, executable feedback, empirical validity, and transportation scale are different scientific properties** that must be decoupled and evaluated separately.

---

## 🔄 Core Finding 1: Closed-Loop Feedback Regimes

| Regime | What changes after an off-log ego intervention? | What remains anchored? | Defensible interpretation |
|---|---|---|---|
| **Replay-Constrained** | The returned observation or queried viewpoint may change. | The behavioral future remains prescribed by a log or external trajectory. | Tests observation replacement or rendering around a prescribed future; does not establish ego execution or traffic response. |
| **Ego-Responsive** | The ego command changes the realized ego motion. | Relevant non-ego behavior remains prescribed or is not independently shown to respond. | Establishes ego controllability within the tested action range; does not establish reciprocal interaction. |
| **Traffic-Reactive** | Relevant non-ego behavior changes when the counterfactual ego trajectory is varied. | Nothing relevant to the tested interaction is assumed to remain on the logged future. | Supports local interactive claims only for the tested behavior families and intervention conditions. |

> **Policy recurrence is a separate axis:** Repeatedly calling a generator is not equivalent to showing that an updated state enters another policy decision and changes an uncommitted continuation.

---

## 📊 Core Finding 2: Capability vs. Validity Hierarchy

<p align="center">
  <img src="/images/figure4_validity_stack.png" alt="Claim-specific validity layers" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 14px rgba(0,0,0,0.12);" />
  <br/>
  <em><b>Figure 4:</b> Claim-specific validity layers for learned driving environments, from observation fidelity to corridor/network transportation scale.</em>
</p>

| Claim layer | Decisive evidence | Evidence that is insufficient on its own | Highest defensible scope |
|---|---|---|---|
| **Observation fidelity** | Held-out viewpoints, geometric consistency, temporal alignment, and multi-sensor agreement tied to state transitions. | In-distribution image similarity or task agreement without explicit state-transition checks. | Policy-relevant sensing within the measured sensor and viewpoint envelope. |
| **Ego controllability** | Target-to-realized trajectory tracking across commands, with physical and kinematic feasibility checks. | Action tokens, visually diverse clips, or command-conditioned generation without motion verification. | Action-consistent ego dynamics within the tested maneuver range. |
| **Traffic-response validity** | Matched counterfactual ego interventions, repeated rollouts, synchronized joint states, and response timing/severity measurements. | Plausible open-loop rollouts, prompt diversity under a fixed ego path, or log replay. | Attributable traffic response within the tested interactions and behavior models. |
| **Closed-loop policy validity** | Stable rankings or transfer across independent simulators, benchmarks, controlled physical tests, or deployment references. | Strong performance inside one simulator or self-consistency alone. | Policy ranking, selection, or training claims within the validated environment distribution. |
| **Transportation scale** | Demand-conditioned composition of local responses with validated queues, shockwaves, throughput, and delay. | Isolated encounter realism or aggregate matching without microscopic causal checks. | Corridor or network conclusions only up to the highest empirically validated scale. |

---

## 🛑 Scope Boundaries

* **Visual fidelity** does not by itself establish physically correct ego response.
* **Action conditioning** does not by itself establish ego controllability.
* **Joint generation** does not by itself establish intervention-conditioned traffic response.
* **Local interactive validity** does not automatically scale to corridor or network performance.
* A simulator is best treated as an **experimental instrument** whose claims are bounded by its demonstrated feedback dependencies and evidence.

---

## 🔗 Links & Resources

* **GitHub Repository**: [AnXu-ITS/driving-world-models-survey](https://github.com/AnXu-ITS/driving-world-models-survey)
* **Preprint PDF (24 pages)**: [Download PDF](/files/From_Foresight_to_Reactive_Traffic_Worlds_Survey.pdf)
* **Editable Figures (PPTX)**: [Download on GitHub](https://github.com/AnXu-ITS/driving-world-models-survey/tree/main/editable_figures)
* **LaTeX Source**: [Browse on GitHub](https://github.com/AnXu-ITS/driving-world-models-survey/tree/main/paper)

---

## 👥 Authors & Affiliations

* **An Xu** — School of Transportation Science and Engineering, Harbin Institute of Technology (`AnX.RTL2324@tum-asia.edu.sg`)
* **Zekai Jin** — Department of Civil Engineering, McGill University (`zekai.jin@mail.mcgill.ca`)
* **Hanrong Zhang** — Department of Computer Science, University of Illinois Chicago (`hzhan135@uic.edu`)
* **Xiaoning Sun** — Department of Civil Engineering, McGill University (`xiaoning.sun@mail.mcgill.ca`)
* **Chengbo Zhang** — Department of Civil Engineering, McGill University (`chengbo.zhang@mail.mcgill.ca`)
* **Yunfei Yin (Corresponding Author)** — School of Transportation Science and Engineering, Harbin Institute of Technology (`yunfeiyin@hit.edu.cn`)

---

## 📖 BibTeX Citation

```bibtex
@misc{xu2026foresight,
  title  = {From Foresight to Reactive Traffic Worlds: A Survey of Driving World Models for Closed-Loop Simulation},
  author = {Xu, An and Jin, Zekai and Zhang, Hanrong and Sun, Xiaoning and Zhang, Chengbo and Yin, Yunfei},
  year   = {2026},
  url    = {https://github.com/AnXu-ITS/driving-world-models-survey}
}
```
