---
title: "Conditional Effects of Connected-Vehicle Requests in Reinforcement-Learning Traffic Signal Control"
collection: publications
category: preprints
permalink: /publication/2026-cv-request-rl-traffic-signal-control
excerpt: 'A controlled factorial study disentangling queue-responsive RL adaptation from connected-vehicle request conditioning across 2,730 simulation runs and 2D crossed-bootstrap uncertainty analysis.'
date: 2026-06-15
venue: "Preprint / In Submission"
paperurl: "/files/Conditional_Effects_of_Connected_Vehicle_Requests.pdf"
citation: 'Xu, An. (2026). &quot;Conditional Effects of Connected-Vehicle Requests in Reinforcement-Learning Traffic Signal Control.&quot; <i>Preprint</i>.'
header:
  teaser: "request_conditioning_effect.png"
---

<p align="center">
  <img src="/images/request_conditioning_effect.png" alt="Request conditioning is demand- and training-sensitive, not penetration-monotonic" style="width: 100%; border-radius: 8px; box-shadow: 0 4px 14px rgba(0,0,0,0.12);" />
  <br/>
  <em><b>Figure 1:</b> Paired differences ($\text{Full DQN} - \text{Queue-only DQN}$) in average queue across 21 demand $\times$ penetration conditions with 95% 2D Crossed-Bootstrap error bars (50,000 resamples). Negative values favor the complete request mechanism; hollow markers at 0% denote a training-history diagnostic.</em>
</p>

## Abstract

Connected vehicles can provide upstream observations and priority cues, but a request mechanism is useful only if it improves decisions beyond queue-responsive adaptation. We test this distinction at one site-derived SUMO intersection with a request-aware deep Q-network (DQN) and a matched queue-only ablation. The variants share the architecture, base congestion objective, training schedule, and 10--20~s timing shield; the request-aware variant additionally incorporates request-state inputs and an auxiliary request-shaped reward term. Five training realizations per variant were evaluated against fixed-time, presence-actuated, and max-pressure control at three demand levels, seven connected-vehicle penetrations, and ten paired traffic realizations, yielding 2,730 one-hour runs. 

To represent both stochastic sources, we independently resample the training and traffic axes of each $5\times10$ crossed result matrix. Queue-only DQN reduced mean queue relative to each of the three conventional baselines in all 21 demand--penetration conditions, with all 21 crossed-bootstrap intervals per baseline (63 in total) excluding zero. The request-aware DQN had lower point estimates than the same baselines in all conditions, but one interval at nominal demand and 50% penetration included zero because training-realization dispersion was large. Relative to queue-only control, the 95% crossed intervals excluded zero in only eight of 21 conditions: three favored the complete request mechanism (Full DQN) and five favored Queue-only DQN. At 0% penetration, no request occurs online, so that contrast is a training-history diagnostic rather than an online request effect. Request counts show that policies approved 75--81% of hold requests and 27--37% of switch requests; these diagnostics describe policy behavior but do not identify the cause of performance differences. Across this sweep, queue-responsive adaptation is the reproducible gain; the incremental effect of request conditioning is demand- and training-sensitive and is not monotonic in penetration.

---

## 🚀 Key Empirical Insights

1. **Adaptivity Advantage:** Both Full and Queue-only DQN substantially outperform Fixed-time, Actuated, and Max-pressure baselines across all 21 demand $\times$ penetration conditions (queue reduction of $0.40$–$0.93$ veh/lane; all 63 crossed-bootstrap 95% CIs exclude zero).
2. **Request Fragility:** Adding the complete request mechanism does not monotonically improve performance. At nominal design demand (1,000 veh/h), Full DQN exhibits longer queues than Queue-only DQN across 0%–80% penetrations.
3. **Demand Inversion:** The marginal effect of request conditioning flips sign with demand level: beneficial under low demand ($700$ veh/h at 20% and 80%), but detrimental or neutral under nominal and saturated regimes.
4. **Approval Asymmetry:** Trained policies approve 75%–81% of HOLD requests but only 27%–37% of SWITCH requests, causing request-induced state perturbations that conflict with queue clearing.
5. **Retraining Dispersion:** Training stochasticity dominates traffic stochasticity in specific regions (e.g. 50% penetration), causing wide confidence bands due to outlier policy convergence.

---

## 🔗 Links & Resources

* **GitHub Repository**: [AnXu-ITS/cv-request-dqn-tsc](https://github.com/AnXu-ITS/cv-request-dqn-tsc)
* **Preprint Manuscript (PDF)**: [Download Full Paper (13 Pages)](/files/Conditional_Effects_of_Connected_Vehicle_Requests.pdf)

---

## 📖 BibTeX Citation

```bibtex
@article{xu2026conditional,
  title={Conditional Effects of Connected-Vehicle Requests in Reinforcement-Learning Traffic Signal Control},
  author={Xu, An},
  journal={Preprint},
  year={2026},
  url={https://github.com/AnXu-ITS/cv-request-dqn-tsc}
}
```
