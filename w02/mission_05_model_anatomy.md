# Mission 5: Understand the Anatomy of an ML Model

## 1. Algorithm vs. Model vs. Learned Parameters

* **ML Algorithm:** The mathematical procedure or optimization framework used to learn patterns from data (e.g., Linear Regression, Random Forest, Gradient Descent).

* **ML Model:** The specific predictive instance resulting from running an algorithm on a dataset (contains fixed mathematical rules and learned weights).

* **Learned Parameters:** The internal weights ($w$) and biases ($b$) adjusted automatically during training to minimize prediction errors ($y = wx + b$).

---

## 2. Model Lifecycle Flow

Dataset (X, Y) ---> [ Training Process ] ---> [ Calculate Loss ] ---> [ Update Parameters ] ---> Trained Model ---> Inference on New Input (X_new) ---> Prediction (Y_hat)

---

## 3. Training vs. Inference

* **Training:** The computationally intensive phase where the model iteratively reads historical data, computes predictions, measures errors using a loss function, and updates parameters to minimize loss.

* **Inference:** The operational phase where a fully trained, frozen model receives new, unseen inputs to generate immediate predictions without updating its parameters.

---

## 4. Intuition Behind Linear Regression

Linear Regression learns the mathematical relationship between input features ($x$) and continuous numerical targets ($y$) by fitting a line or hyperplane through data points:

$$y = w_1 x_1 + w_2 x_2 + ... + b$$

During training, the loss function (e.g., Mean Squared Error) measures the vertical distance between predicted points and actual target points. Optimization algorithms (like Gradient Descent) iteratively adjust weights ($w$) and bias ($b$) until the error is minimized.
