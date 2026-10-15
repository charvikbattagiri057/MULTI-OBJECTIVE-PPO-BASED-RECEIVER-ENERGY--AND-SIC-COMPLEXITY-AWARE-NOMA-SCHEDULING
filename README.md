# Multi-Objective PPO-Based Receiver Energy- and SIC-Complexity-Aware NOMA Scheduling

[![Python 3.10+](https://img.shields.io/badge/python-3.10+-blue.svg)](https://www.python.org/downloads/)
[![Gymnasium](https://img.shields.io/badge/Gymnasium-v0.29.1-green.svg)](https://gymnasium.farama.org/)
[![Stable-Baselines3](https://img.shields.io/badge/Stable--Baselines3-v2.2.1-orange.svg)](https://stable-baselines3.readthedocs.io/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

> **Machine Learning Course Project (25SC2107E) — KL University**  
> **Team:** Ranga Charvik Battagiri, A. Dhanush, R. Gnaneshwar  
> **Supervisor:** Mr. N Lava Prasad, Assistant Professor, Department of ECE  

---

## 📌 Overview

Non-Orthogonal Multiple Access (NOMA) is a key spectral-efficiency enabler for 5G/6G massive machine-type communication (mMTC). However, receiver **Successive Interference Cancellation (SIC)** imposes steep computational and battery burdens that escalate linearly with cluster size. 

Existing schedulers optimize purely for throughput, remaining "battery-blind" and rapidly exhausting energy-depleted IoT nodes. This repository introduces an end-to-end Reinforcement Learning framework featuring:
* A custom **Gymnasium** environment modeling imperfect Channel State Information (CSI), multi-cell interference, and dynamic user battery degradation.
* A **Proximal Policy Optimization (PPO)** agent trained on a multi-objective reward balancing throughput, energy cost, SIC complexity, and Jain's fairness index.
* A proven **51% improvement** in overall system utility score over standard channel-gain greedy schedulers.

---

## 🗂️ Repository Structure

```text
├── 1_Abstract/
│   └── Abstract_template.docx                  # Project abstract and problem statement
├── 2_Literature_Survey/
│   └── Literature_Survey.docx                  # Background research and IEEE paper summaries
├── 3_Presentations/
│   ├── Final_Expo_Presentation.pptx            # Final expo slide deck
│   ├── Multi-Objective PPO NOMA Final Expo.pptx # Additional presentation deck
│   └── NOMA_Project_Presentation_Updated.pptx  # Project update presentation
├── 4_Implementation_Code/      
│   ├── README.md                               # Code-specific documentation
│   ├── baselines.py                            # Random, Fixed, and Greedy baseline schedulers
│   ├── download.png                            # Example generated performance plot
│   ├── evaluate.py                             # 30-episode comparative benchmarking script
│   ├── noma_env.py                             # Custom Gymnasium NOMA environment
│   └── train_ppo.py                            # PPO training pipeline
├── 5_Final_Report/
│   └── NOMA_Project_Report_Final_with_Refs.docx # Comprehensive 15-page final project report
└── 6_Dataset_and_EDA/
    ├── EDA_Report.docx                         # Exploratory Data Analysis report
    ├── battery_dist.png                        # Battery depletion distribution plot
    ├── channel_dist.png                        # Channel fading distribution plot
    └── simulated_noma_dataset.csv              # Simulated telemetry dataset (12,000 rows)
