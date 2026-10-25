# Mission 2: Understand Data - What Does an ML System Learn From?

## 1. Core Data Terminology

* **Dataset:** A structured collection of observations used for training, validating, or testing an ML model.

* **Sample / Observation:** A single data record or row representing an individual entity (e.g., one layout block run).

* **Feature:** An individual measurable property or variable used as input ($X$) to predict an outcome (e.g., cell count, wirelength).

* **Label / Target:** The true ground-truth outcome or value ($Y$) that a supervised model aims to learn and predict (e.g., Pass/Fail status or total power consumption).

* **Structured vs. Unstructured Data:** Structured data lives in organized tables with clean columns (e.g., CSV files of timing reports). Unstructured data lacks fixed tabular formats (e.g., raw layout image bitmaps or GDSII streams).

* **Numerical vs. Categorical Features:** Numerical features are continuous or discrete numbers (e.g., clock frequency = 1.2 GHz), while Categorical features represent discrete groups or types (e.g., Process Corner = TT, FF, SS).

---

## 2. Illustrative Dataset: Physical Design Timing & Power Runs

| Run_ID | Cell_Count (Numerical Feature) | Clock_Freq_GHz (Numerical Feature) | Process_Corner (Categorical Feature) | Total_Wirelength_mm (Numerical Feature) | WNS_Slack_ps (Target / Label) | Timing_Status (Target / Label) |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| 1 | 150,000 | 1.2 | TT | 45.2 | +12.5 | Pass |
| 2 | 150,000 | 1.5 | SS | 48.7 | -45.2 | Fail |
| 3 | 320,000 | 1.0 | FF | 112.0 | +85.0 | Pass |
| 4 | 320,000 | 1.4 | SS | 125.4 | -110.1 | Fail |
| 5 | 85,000 | 2.0 | TT | 28.9 | -12.0 | Fail |
| 6 | 85,000 | 1.8 | FF | 26.4 | +34.2 | Pass |

---

## 3. Data Quality Impact on Model Performance

* **Inconsistent Labels / Noisy Targets:** If run logs mistakenly report a Pass for a run that actually suffered hold violations due to log-parsing errors, the model will learn false patterns and fail to generalize accurately.

* **Missing Values & Feature Outliers:** Missing wirelength metrics or corrupted negative capacitance readings distort mathematical optimization during training, pulling regression lines away from physical reality.
