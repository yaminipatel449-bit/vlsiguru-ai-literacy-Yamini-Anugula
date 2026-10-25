# Mission 6: Understand Evaluation and Generalisation

## 1. Data Splitting & Generalisation

To evaluate whether a model genuinely learns underlying patterns rather than memorizing training data, datasets are partitioned into three independent sets:

* **Training Set (~70%):** Used directly by the algorithm to update model parameters and weights.

* **Validation Set (~15%):** Used during development to tune hyperparameters and check for overfitting.

* **Test Set (~15%):** Held out completely until final evaluation to measure true generalisation on unseen data.

---

## 2. Model Fitting Behaviors

* **Underfitting (High Bias):** The model is too simple to capture underlying patterns (e.g., fitting a linear model to a highly non-linear parasitic timing distribution). Both training and test accuracy are poor.

* **Overfitting (High Variance):** The model memorizes training noise and specifics rather than general patterns. Training accuracy is extremely high, but test performance drops significantly.

* **Optimal Generalisation:** The model strikes a balance, achieving low error on both training and unseen test data.

---

## 3. Worked Example: Class Imbalance & Evaluation Metrics

### Scenario: DRC Violation Predictor
A dataset contains **1,000 layout regions**, where **950 regions are DRC-Clean** and **50 regions have DRC Violations** (imbalanced 95:5 ratio).

#### Naive Baseline Model:
A naive model simply predicts DRC-Clean for every single input without learning anything.
* **Accuracy:** 950 / 1000 = 95.0%

Despite achieving 95% accuracy, the model fails completely at its core objective because it missed **100% of the actual DRC violations**.

#### Evaluation Metrics Analysis:
* **Precision:** Out of all regions predicted as violations, how many were true violations?
  $$\text{Precision} = \frac{TP}{TP + FP}$$

* **Recall (Sensitivity):** Out of all actual violations present, how many did the model catch?
  $$\text{Recall} = \frac{TP}{TP + FN}$$

* **Why Precision/Recall Matter:** In semiconductor manufacturing and design verification, missing a defect (False Negative) is catastrophic. Metrics like **Recall** and **F1-Score** provide an accurate measure of model utility where simple accuracy fails.
