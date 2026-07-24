# Graph-Based Relational Scene Representation for Vision-Language Navigation

## 📌 Project Overview

This project implements a **Graph Neural Network (GNN)-based scene representation** to improve relational reasoning in Vision-Language Navigation (VLN) tasks. The work extends the limitations of hierarchical representations (e.g., Dynam3D) by explicitly modelling object relationships using graph structures.

The system compares a **baseline MLP model** with a **Graph Attention Network (GAT)** and multiple ablation variants to evaluate the importance of relational reasoning.

---

## 🧠 Key Features

* Synthetic dataset simulating spatial environments (corridor, room, open space)
* Graph-based representation using node features and spatial edges
* Implementation of:

  * Baseline (MLP + pooling)
  * Proposed Model (GAT-based GNN)
  * Ablation Models (GCN without attention, shallow GAT)
* Multi-seed evaluation (5 runs) for statistical reliability
* Performance visualization:

  * Box plots
  * Bar charts with error bars



## ⚙️ Requirements

Install dependencies using:

```
pip install torch torchvision torchaudio
pip install torch-geometric
pip install numpy pandas matplotlib seaborn scikit-learn networkx
```

---

## 🚀 How to Run

1. Clone the repository:

```
git clone <your-repo-link>
cd <project-folder>
```

2. Run the experiment:

```
python train.py
```

3. Output:

* Console logs of accuracy across 5 seeds
* Saved visualizations:

  * `ablation_boxplot.png`
  * `ablation_bar_chart.png`

---

## 📊 Models Implemented

| Model                | Description                 |
| -------------------- | --------------------------- |
| Baseline (MLP)       | No relational reasoning     |
| Proposed (GAT-2L)    | Multi-head attention GNN    |
| Ablation (GCN-NoAtt) | Removes attention mechanism |
| Ablation (GAT-1L)    | Tests shallow architecture  |

---

## 📈 Evaluation

* Metric: **Accuracy**
* Statistical evaluation across **5 random seeds**
* Results reported as:

  * Mean Accuracy
  * Standard Deviation

---

## 🧪 Key Findings

* Graph-based models significantly outperform baseline
* Relational reasoning improves spatial understanding
* Model depth impacts performance
* Attention mechanisms show mixed impact depending on structure

---

## ⚠️ Limitations

* Synthetic dataset (not real-world VLN)
* Simplified classification task (not full navigation pipeline)

---

## 🔮 Future Work

* Extend to real VLN datasets (R2R, REVERIE)
* Integrate with Vision-Language Models (e.g., LLaVA)
* Deploy on robotic navigation systems

---

## ⚖️ Ethics & Considerations

* Potential bias in synthetic data design
* Safety concerns in autonomous navigation
* Computational cost of GNN models


## 📜 License

This project is for academic purposes only.
