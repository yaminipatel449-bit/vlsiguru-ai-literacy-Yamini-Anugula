# Week 02 Reflection

### 1. Most Clear ML Concept
The distinction between **Learning Paradigms** (Supervised, Unsupervised, Reinforcement Learning) and **Task Types** (Classification, Regression, Clustering) became completely clear this week. Learning paradigms define *how* feedback is provided during training, while task types define *what* mathematical output the model produces.

### 2. Concepts Easily Confused
**Overfitting** and **High Variance** are often discussed separately, but understanding that overfitting happens when a model memorizes training noise at the expense of test generalisation made the connection clear.

### 3. Claim Verification Insight
Verified the claim that "accuracy is an insufficient metric for imbalanced datasets" using Google's ML Crash Course. Tested this with a worked 95:5 imbalanced DRC violation scenario, proving that a naive model can score 95% accuracy while being completely useless in production.

### 4. Underestimated ML Lifecycle Stage
The **Data Preparation and Cleaning** stage is easiest to underestimate. Model accuracy is strictly bounded by data quality; bad labels or unrepresentative training data guarantee deployment failures regardless of model architecture complexity.

### 5. Question for Saturday Masterclass
How do EDA tool developers handle concept drift and node migration when training ML models on older technology nodes (e.g., 16nm) for use on unreleased nodes (e.g., 2nm)?
