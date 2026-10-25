# Mission 3: Understand the Main ML Approaches

## 1. Major Learning Paradigms Comparison

| Paradigm | Core Idea | Training Signal | Primary Output | Main Limitation | Suitable Use Case |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Supervised Learning** | Learns mapping from inputs to known targets using labeled historical examples. | Ground-truth labels ($Y$) paired with inputs ($X$). | Predictive mapping function ($f(X) \approx Y$). | High cost of collecting accurate, high-quality ground-truth labels. | Predicting post-routing timing slack from floorplan features. |
| **Unsupervised Learning** | Finds intrinsic hidden patterns, clusters, or structures in unlabeled data. | Structural patterns, distances, and data distributions. | Cluster assignments or reduced dimensions. | Evaluation is subjective; no objective ground-truth label to verify accuracy directly. | Grouping design runs with similar placement properties to detect anomaly outliers. |
| **Reinforcement Learning** | Learns optimal action sequences through trial-and-error environment interaction. | Scalar reward/penalty signals based on outcome state. | Optimal policy / action selection sequence. | Extremely sample-inefficient; requires millions of simulated trial environments. | Exploring macro placement choices to optimize Power-Performance-Area (PPA). |
| **Self-Supervised Learning** | Generates pseudo-labels from the structural properties of raw data itself. | Automatically masked or pretext task signals within the data. | Learned feature representations / embeddings. | Requires massive datasets and high compute to pre-train effective representations. | Pre-training transformer models on raw Verilog code corpora before fine-tuning. |

---

## 2. Simplified Workflows

* **Supervised Learning:** Inputs (X) + Labels (Y) ---> [ Training Algorithm ] ---> Trained Model ---> New Inputs (X) ---> Predicted Label (Y)

* **Unsupervised Learning:** Unlabeled Inputs (X) ---> [ Clustering Algorithm ] ---> Discovered Clusters / Underlying Patterns

* **Reinforcement Learning:** Agent ---> Takes Action ---> Environment ---> Provides Reward Signal + New State ---> Agent Updates Policy

---

## 3. Self-Supervised vs. Unsupervised Learning

While Unsupervised Learning focuses purely on finding structural clusters without targets, **Self-Supervised Learning** creates artificial supervised tasks (e.g., masking 15% of tokens in a netlist script and asking the model to predict the missing tokens). It converts an unlabeled problem into a supervised framework without requiring human labeling.
