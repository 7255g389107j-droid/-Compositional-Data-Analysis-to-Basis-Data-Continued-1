# -Compositional-Data-Analysis-to-Basis-Data-Continued-1
Itagaki Ensemble Engine is a commercial-grade R framework for compositional deconvolution. It restores absolute scaling factors from relative abundance without spike-ins. Features: automated subcomposition pruning, elbow-based anchor selection, 95% bootstrap CIs, and sample-wise Reliability Score (Consensus R2) to overcome closure artifacts. 
# Itagaki Ensemble Engine (V7.0) 🚀
**Ultimate Compositional Deconvolution & Basis Data Estimation**

Developed by **Tatsuki Itagaki**, this engine is a high-fidelity analytical framework designed to overcome the **"Compositional Closure"** problem. It reconstructs absolute scaling factors (Relative Total Mass) from relative abundance data without the need for physical spike-ins.

## ⚖️ Scientific Philosophy
> "Physical standards are often new sources of noise. The true reference exists within the data—the ensemble of components that remain statistically motionless. This is the **Natural Internal Standard**."

## 🛠 Key Features
- **Automated Subcomposition Pruning**: Filters sparse/unstable taxa to ensure log-ratio integrity.
- **Multi-Metric Stability Scoring**: Combines **Ohta (2011) CV-Asymmetry** and **Aitchison Purity Index (PI)**.
- **Dynamic Elbow-Cliff Logic**: Automatically determines the optimal number of anchors by detecting the stability "cliff".
- **95% Bootstrap Confidence Intervals**: Quantifies reconstruction uncertainty via 1,000 iterations.
- **Sample-wise Reliability Score (Consensus R2)**: Provides a 0–1 score identifying where anchor consensus fails.
- **Smart Staggered Labeling**: Prevents label overlap in dense plots for publication-quality output.

## 📊 Evaluation Metrics
- **IR (Invariance Ratio)**: Physical stability against the Poisson noise floor.
- **PI (Purity Index)**: Geometric center of the compositional simplex.
- **Consensus R2**: Statistical agreement between selected anchors for a specific sample.

## 🚀 Quick Start

1. **Prepare Data**: Load your proportion matrix (Samples as Rows, Taxa as Columns) as `Dataset`.
2. **Run the Engine**: Execute the V7.0 R script.
3. **Interpret Windows**:
   - **Window 1**: Restored Total Mass (Scaling Factors) with 95% CI.
   - **Window 2**: Individual Reliability Scores and Anchor Weights.
   - **Window 3**: Elbow Plot and Mass-Library Correlation Diagnosis.

## 📦 Requirements
- **Language**: Pure Base R (Zero External Dependencies)
- **Input**: A non-negative numeric matrix or data frame (`Dataset`).

## 📜 License
MIT License - Copyright (c) 2026 Tatsuki Itagaki

## 🎓 Academic Citation
If you use this software in your research, please cite:
*Ohta, T. (2011). DOI: 10.1007/s11004-011-9332-y. Itagaki, T (2026). DOI: 10.13140/RG.2.2.21953.93284. Implementation: Itagaki Ensemble Engine.*
