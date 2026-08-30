---
layout: archive
title: "Curriculum Vitae"
permalink: /cv/
author_profile: true
redirect_from:
  - /resume
---

{% include base_path %}

<p><a href="{{ base_path }}/files/An_Xu_CV.pdf" class="btn btn--primary"><i class="fas fa-file-pdf"></i> Download Full CV (PDF)</a></p>

## 🎓 Education

* **Harbin Institute of Technology (HIT)**, China
  * **Ph.D. Student (Incoming)**
* **Technical University of Munich Asia (TUM Asia)**, Singapore & Germany
  * **Master of Science (M.Sc.) in Railway Engineering (ITS Focus)** *(Sep 2023 – Feb 2026)*
  * *Thesis*: Simulation-Based Bidirectional Control between AVs and Adaptive Traffic Signal Control Using Real-World V2X-Infrastructure
  * *Relevant Courses*: Traffic Operation and Control (ITS), Transportation Modelling and Simulation Tools, Rolling Stock, Trackwork, Public Transport.
* **Southwest Jiaotong University / University of Leeds (Joint Program)**, China & UK
  * **Bachelor of Engineering (B.Eng.) in Civil Engineering with Transport** *(Sep 2019 – Jul 2023)*
  * *Thesis*: Influence of Sasobit on Physical and Chemical Properties of Asphalt
  * *Relevant Courses*: Structural Design and Analysis, Railway Engineering, Highway Engineering, Transport Planning and Modelling.

---

## 💼 Work Experience

* **AI Agent Developer** | **Sihe Information Technology Co., Ltd.**, Harbin, China
  * *Jun 2026 – Present*
  * Designed and developed Long-horizon Task Agents and reusable Agent Skills (SOPs) for complex task decomposition, sustained execution, state management, and tool calling.
  * Researched fundamental LLM mechanisms (Tokenization, BPE) and model distillation (Teacher–Student, knowledge transfer, model lightweighting).
  * Drove rapid prototyping on complex projects using agent tools (Codex, Hermes, pi) for vibe coding, code generation, and automated workflows.

* **L4 Autonomous Driving & ITS Engineering Intern** | **IABG mbH**, Munich, Germany
  * *Jul 2025 – Feb 2026*
  * Worked on the Mobility Innovation Campus (MIC) L4 autonomous driving test site, conducting R&D and engineering validation of autonomous driving and ITS.
  * Fused Camera, LiDAR, Radar, and V2X infrastructure information with Bird's-Eye-View (BEV) scene representations for complex traffic scene understanding and intersection coordination.
  * Developed Python-based data processing and real-time traffic interaction/control logic (RSU/OBU, SPaT, V2X), supporting trajectory analysis, L4 system testing, and scenario validation.

* **Traffic Engineer Intern** | **ST Engineering Urban Solutions Ltd.**, Singapore
  * *Aug 2024 – Feb 2025*
  * Automated VISSIM simulation workflows in Python and built, calibrated, and optimized PTV VISUM/Optima models for traffic operations analysis and control optimization.
  * Integrated multi-source road network, GIS, detector, and OD data (QGIS, GeoPandas, Pandas, SQL) for ITS model optimization, traffic state analysis, and travel demand forecasting.

---

## 🔬 Research Experience & Projects

* **Toward Continually Growing World Models: An OaK-Inspired Architecture for Learned Abstraction and Planning** *(Aug 2026)*
  * Formulated *Structural Continual World Modeling (SCWM)*, integrating parameter-level adaptation ($\theta_t \to \theta_{t+1}$) with a structural adaptation axis ($\mathcal{K}_t \to \mathcal{K}_{t+1}$) based on Richard Sutton's OaK architecture and FC-STOMP lifecycle.
  * Formalized predictive state representation expansion with constructed features, reward-respecting subtasks with terminal bonuses, predictive option models, and Pareto-optimal utility pruning.
  * Published preprint with Zenodo DOI: [`10.5281/zenodo.22103257`](https://doi.org/10.5281/zenodo.22103257) | GitHub: [`AnXu-ITS/OaK-World-Model`](https://github.com/AnXu-ITS/OaK-World-Model).

* **From Foresight to Reactive Traffic Worlds: A Survey of Driving World Models for Closed-Loop Simulation** *(Aug 2026)*
  * Authored comprehensive survey investigating Driving World Models as learned closed-loop simulators, focusing on counterfactual off-log environmental feedback and multi-agent reactivity.
  * Formulated a 3-regime Simulation-Closure framework (*Replay-Constrained* $\rightarrow$ *Ego-Responsive* $\rightarrow$ *Traffic-Reactive*) and established a 5-layer claim-specific validity stack spanning observation fidelity, ego controllability, traffic-response validity, policy validity, and corridor/network scale.
  * Released complete preprint, reproducible LaTeX package, and editable PowerPoint figures. GitHub: [`AnXu-ITS/driving-world-models-survey`](https://github.com/AnXu-ITS/driving-world-models-survey) | PDF: [`Download Full Survey`](/files/From_Foresight_to_Reactive_Traffic_Worlds_Survey.pdf).

* **Conditional Effects of Connected-Vehicle Requests in Reinforcement-Learning Traffic Signal Control** *(Jun 2026)*
  * Disentangled queue-responsive RL adaptation from connected-vehicle request conditioning through matched DQN ablations across 2,730 one-hour SUMO evaluation runs.
  * Conducted 2-dimensional Crossed-Bootstrap uncertainty quantification (50,000 resamples) across 5 training seeds $\times$ 10 paired traffic seeds over 3 demand levels and 7 CV penetrations.
  * Released open-source benchmark codebase, pre-trained weights, and full evaluation logs. GitHub: [`AnXu-ITS/cv-request-dqn-tsc`](https://github.com/AnXu-ITS/cv-request-dqn-tsc) | PDF: [`Download Manuscript (PDF)`](/files/Conditional_Effects_of_Connected_Vehicle_Requests.pdf).

* **Simulation-Based Bidirectional Control between AVs and Adaptive Traffic Signal Control Using Real-World V2X-Infrastructure** *(Aug 2025 – Jan 2026)*
  * *Master's Thesis / IABG-MIC Project*
  * Built a bidirectional AV–signal control coordination framework on MIC's real-world V2X infrastructure using a SUMO/TraCI microscopic simulation environment.
  * Designed a DQN-based adaptive traffic signal control algorithm for dynamic phase optimization in mixed traffic, evaluating queue length, delay, efficiency, and robustness under varying V2X penetration rates.

* **AI-Driven Transformation of Modern Transportation Systems** *(TUM Asia Workshop)*
  * Analyzed AI's transformative impact across ITS, autonomous driving, smart railways, and urban traffic management.
  * Authored the paper *AI's Transformation of Transportation in Modern Society*.

* **Influence of Sasobit on Physical and Chemical Properties of Asphalt** *(Bachelor's Thesis, Oct 2022 – Apr 2023)*
  * Experimental testing and performance evaluation of the Sasobit additive on the physical and chemical properties of asphalt mixtures.

---

## 🛠️ Skills & Expertise

* **AI Agent Engineering**: Long-horizon Task Agents, Agent Skill & SOP Design, Tool Use, Workflow Orchestration, Vibe Coding (Codex, Hermes, pi)
* **AI/LLM & Algorithms**: Continual Learning, World Models, OaK Architecture, Reinforcement Learning (DQN, Options), Model Distillation, Tokenization/BPE
* **Programming & Data Science**: Python, SQL, MATLAB, Git, Pandas, NumPy, GeoPandas, Matplotlib
* **Autonomous Driving & ITS**: V2X (RSU/OBU, SPaT), Sensor Fusion (LiDAR, Camera, Radar), BEV Representation, Trajectory Analysis, SUMO, TraCI, PTV VISSIM, PTV VISUM, PTV Optima
* **Engineering Tools**: QGIS, AutoCAD, ANSYS, LaTeX, Markdown

---

## 🌐 Languages

* **Chinese**: Native
* **English**: Fluent

---

## 👥 Referees

* **Dr. Martin Margreiter** — IABG Industrieanlagen-Betriebsgesellschaft mbH, Munich, Germany (Email: `margreiter@iabg.de`)
* **Liu Xiaodong** — (Email: `xiaodong.liu@outlook.com`)
