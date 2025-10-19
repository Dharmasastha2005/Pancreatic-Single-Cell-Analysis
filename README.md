# Pancreatic-Single-Cell-Analysis

# Pancreas Single-Cell Omics — From Clusters to Dynamics

A compact end-to-end single-cell analysis pipeline focusing on **human pancreatic biology**, integrating:
- High-throughput **single-cell transcriptomics**
- **Machine Learning–based cell-type classification**
- **Cellular dynamics and predictive modeling**
- Drug-target overlay analysis

Designed to be **runnable in under an hour**, using either synthetic or real pancreas datasets (e.g., `Combined_HumanPancreas_data_alligned.csv`).

---

## Project Overview

| Module | Description | Key Outputs |
|---------|--------------|--------------|
| **Data Preprocessing** | Reads scRNA-seq data, normalizes, log-transforms | Summary stats, gene count distributions |
| **Clustering & Visualization** | Leiden clustering + UMAP dimensionality reduction | UMAP plots, cluster annotation |
| **Marker Gene Analysis** | Identifies top marker genes per cluster | Heatmaps, ranked marker tables |
| **Machine Learning Classifier** | Random Forest model to classify cell types | Accuracy score, feature importance plot |
| **RNA Velocity (Mock)** | Simulated spliced/unspliced dynamics | Velocity streamplot |
| **State Transition Model** | Builds simple Markov transition graph | State-transition network visualization |
| **Drug Target Overlay** | Matches top expressed genes with DrugBank entries | DataFrame summary |
| **Quantitative Dynamics Models** | β-cell secretion ODE, Monte Carlo cell-state transitions, PCA-based predictive smoothing | Simulation plots & trajectories |

---

## Example Outputs (10+ Visuals)
1. Gene count distribution  
2. UMAP of cell clusters  
3. Cluster composition pie chart  
4. Violin plots of marker genes (INS, GCG, SST)  
5. Heatmap of top markers per cluster  
6. RandomForest feature importance bar chart  
7. Confusion matrix / accuracy metrics  
8. RNA velocity streamplot (mock)  
9. State transition graph  
10. β-cell ODE secretion curve  
11. Monte Carlo transition heatmap  
12. PCA trajectory smoothing plot  

---

## Requirements

| Library | Version (tested) |
|----------|------------------|
| `scanpy` | ≥ 1.9 |
| `scvelo` | ≥ 0.2 |
| `numpy`, `pandas`, `matplotlib`, `seaborn` | latest |
| `sklearn` | ≥ 1.4 |
| `networkx` | optional (for transition graph) |

Install:
```bash
pip install scanpy scvelo numpy pandas matplotlib seaborn scikit-learn networkx
