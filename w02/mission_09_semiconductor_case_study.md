# Mission 9: Connect the Full Map to Semiconductor Engineering

## Case Study: ML-Driven Pre-Routing Congestion and Timing Slack Prediction

**Domain Track:** Physical Design (PD)  
**Target Application:** Early Floorplanning and Routability Prediction  

---

## 1. Engineering Problem
In modern digital IC design flows, detailed routing is one of the most time-consuming EDA steps. If severe routing congestion or timing violations are discovered only *after* detailed routing, physical design engineers must revert to early floorplanning and repeat days of place-and-route (P&R) iterations.

---

## 2. Required Engineering Data
* **Inputs ($X$):** Macro placements, standard cell density maps, pin density distributions, power grid locations, and netlist connectivity graphs.

* **Ground-Truth Target ($Y$):** Detailed routing short counts, total DRC violation maps, and final Static Timing Analysis (STA) Worst Negative Slack (WNS).

---

## 3. Task Type and Machine Learning Paradigm
* **Learning Paradigm:** Supervised Learning (trained on paired historical P&R design runs).

* **Task Type:** Classification (predicting congestion hotspot regions: High Risk vs. Low Risk) and Regression (predicting localized wire routing delay in picoseconds).

---

## 4. Evaluation and Limitations
* **Evaluation Metrics:** Receiver Operating Characteristic (ROC-AUC), Recall (to minimize missed routing hotspots), and Mean Absolute Error (MAE) for delay estimation.

* **Engineering Limitations:** ML models trained on a specific technology node (e.g., 12nm) cannot be directly deployed on advanced nodes (e.g., 3nm) without transfer learning or retraining due to fundamental changes in design rules and interconnect parasitics.

---

## 5. Primary References
1. Synopsys Inc., "Synopsys.ai: AI-Driven EDA Suite for Design, Verification, and Test," Official Technology Overview.
2. Cadence Design Systems, "Cadence Cerebrus Intelligent Chip Explorer: Reinforcement Learning for Floorplanning and PPA Optimization," Technical Whitepaper.
