# Mission 8: Does This Problem Actually Need ML?

## Problem Definition: Post-Placement Wire Congestion Prediction

**Objective:** Predict floorplan regions likely to experience severe routing congestion during detailed routing.

---

## Solution Comparison

| Metric / Dimension | Deterministic Rule-Based Solution | Machine Learning (ML) Solution |
| :--- | :--- | :--- |
| **Core Approach** | Uses explicit mathematical bounding-box estimates (Half-Perimeter Wire Length - HPWL) and static cell density thresholds. | Trains a Convolutional or Graph Neural Network on historical placement density maps paired with actual detailed routing congestion maps. |
| **Development Effort** | Low to Moderate. Uses known physical equations and heuristic rules. | High. Requires collecting, cleaning, and preprocessing hundreds of historical design runs. |
| **Execution Speed** | Extremely fast, deterministic computation. | Fast inference execution, but requires offline GPU training time. |
| **Adaptability** | Rigid. Fails when complex multi-layer routing interactions contradict static rule thresholds. | Adaptive. Automatically learns subtle non-linear spatial relationships across process technology nodes. |
| **Failure Mode** | Produces over-conservative estimates leading to unnecessary area expansion. | May hallucinate low congestion in unfamiliar floorplan topologies absent from training data. |

---

## Decision Verdict

If a design team works on standard, well-characterized layouts with simple routing rules, a **rule-based HPWL heuristic** is cheaper, faster, and sufficient. However, for advanced FinFET/GAA nodes with extreme multi-layer routing constraints where static heuristics fail, an **ML-based spatial routability model** provides significant value.
