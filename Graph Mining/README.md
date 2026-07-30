
# Graph Mining and Network Analysis: Structural Properties and Dynamics

This repository contains a comprehensive set of implementations and analyses for large-scale networks, completed as part of the Graph Mining curriculum. The project is divided into two major phases: structural analysis of real-world networks and the simulation of dynamic behaviors such as information diffusion and ranking algorithms.

## Repository Overview

The codebase is organized into two primary modules:
- **Assignment 1:** Focuses on structural topology, generative models (Random and Small-World), and Kleinberg’s navigation theory.
- **Assignment 2:** Explores cascading behavior (LTM/ICM), scale-free growth models, PageRank/RWR in biological networks, and Granovetter’s theory of weak ties.

---

## Technical Implementations

### Module 1: Structural Analysis and Navigability

#### 1. Real-World Network Topology
A comparative study of multiple datasets (including the STRING database) to identify fundamental graph properties. Key metrics computed include:
- Degree Distribution and Power-Law fitting.
- Average Path Length and Diameter.
- Local and Global Clustering Coefficients.
- Degree Assortativity and Connected Components analysis.

#### 2. Generative Network Models
Implementation and comparison of synthetic models against real-world data:
- **Erdős–Rényi (ER) Model:** Implementation of $G(n, p)$ to study random graph behavior.
- **Watts–Strogatz (WS) Model:** Analysis of the "Small-World" phenomenon by tuning the rewiring probability $p$ to balance high clustering with low average path length.

#### 3. Kleinberg’s Navigation and Local Search
Simulation of greedy decentralized search in a grid-based small-world network.
- Evaluation of search efficiency across different values of the clustering exponent $r \in \{0, 1, 2, 3\}$.
- Analysis of search complexity (execution time vs. search depth) in relation to network dimensionality.

---

### Module 2: Network Dynamics and Community Structure

#### 1. Information Diffusion and Cascading Models
Implementation of epidemic and influence models to simulate how information spreads through social networks (e.g., Twitter Higgs dataset):
- **Linear Threshold Model (LTM):** Simulates node activation based on neighbor influence thresholds.
- **Independent Cascade Model (ICM):** Probabilistic modeling of information spread.
- Comparison of cascade size and speed across different initial seed sets.

#### 2. Network Growth and Scale-Free Properties
- **Barabási-Albert (BA) Model:** Implementation of the preferential attachment mechanism.
- Analysis of the **DisGeNET** (Gene-Disease) network, verifying the power-law distribution ($P(k) \sim k^{-\gamma}$) and comparing the observed exponent with theoretical BA models.

#### 3. Node Ranking and Similarity (Random Walk)
- **PageRank:** Implemented to rank protein significance in PPI (Protein-Protein Interaction) networks.
- **Random Walk with Restart (RWR):** Used for seed-based similarity measures to identify functional modules in biological networks. Analysis of the impact of the restart probability on node proximity scores.

#### 4. The Strength of Weak Ties and Community Detection
Investigation into Granovetter’s theory regarding the role of "bridges" in network cohesion:
- **Tie Strength Quantification:** Utilizing Jaccard Similarity and edge weights to distinguish between strong and weak ties.
- **Community Impact Analysis:** Evaluating how the removal of weak ties affects the network’s diameter and community isolation.

---

## Dataset Summary

The analyses in this repository utilize a diverse set of networks:
- **STRING Database:** Protein-Protein Interaction networks.
- **Twitter Higgs:** Social interaction and retweet graphs.
- **DisGeNET:** Gene-Disease association networks.
- **Synthetic Graphs:** Generated via ER, WS, and BA algorithms.

## Requirements

The implementations are written in Python, leveraging the following scientific libraries:
- **NetworkX:** For graph construction and topological measurements.
- **NumPy & Pandas:** For data manipulation and statistical analysis.
- **Matplotlib & Seaborn:** For visualizing degree distributions and cascade dynamics.
- **Scipy:** For curve fitting and power-law verification.

## Usage

Each assignment is provided as a self-contained Jupyter Notebook:
1. Navigate to `HW1_codes.ipynb` for structural analysis and Kleinberg's model.
2. Navigate to `HW2_codes.ipynb` for diffusion models, PageRank, and community analysis.
