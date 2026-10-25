# Mission 4: Understand ML Task Types

## 1. Paradigm vs. Task Type Distinction

A **Learning Paradigm** describes *how* the system obtains feedback during training (e.g., Supervised vs. Reinforcement Learning). A **Task Type** defines *what problem* the model is trying to solve (e.g., predicting a continuous number vs. classifying a discrete category).

---

## 2. Real-World Task Classifications

| Task Type | Core Function | Input Data ($X$) | Expected Output ($Y$) | Domain Example |
| :--- | :--- | :--- | :--- | :--- |
| **Classification** | Predicts a discrete categorical class label. | Floorplan metrics, density maps, clock networks. | Discrete status: DRC Pass vs. DRC Fail. | **Semiconductor:** Predicting whether a placement configuration will cause detailed routing violations. |
| **Regression** | Predicts a continuous real numerical value. | Gate counts, parasitic RC values, buffer counts. | Continuous value: Dynamic power consumption in mW. | **Semiconductor:** Estimating total power consumption prior to full gate-level simulation. |
| **Clustering** | Groups similar unlabelled observations together. | Unlabelled manufacturing wafer test measurements. | Group ID: Wafer pattern cluster assignment. | **Manufacturing:** Grouping silicon wafers exhibiting similar defect spatial patterns. |
| **Anomaly Detection** | Flags unusual data points deviating from normal distributions. | Real-time voltage, current, and temperature sensor streams. | Binary flag: Normal vs. Anomalous. | **Hardware:** Identifying hardware trojans or abnormal silicon power spikes during testing. |
| **Dimensionality Reduction** | Projects high-dimensional feature spaces to lower dimensions. | 50+ extraction metrics from parasitic extraction files. | 2D/3D visual latent projection space. | **EDA:** Simplifying high-dimensional timing path vectors for visual layout exploration. |
| **Recommendation / Ranking** | Ranks candidates based on relevance or utility scores. | Library cell attributes, delay constraints, area requirements. | Ordered list of recommended standard cells. | **EDA:** Ranking optimal buffer insertion candidate locations to fix setup timing. |
