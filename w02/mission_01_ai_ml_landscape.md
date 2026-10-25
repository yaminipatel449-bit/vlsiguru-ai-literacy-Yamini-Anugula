# Mission 1: Build the AI and ML Landscape

## 1. AI vs. Rule-Based Programming vs. Machine Learning

* **Conventional Rule-Based Programming:** Engineers explicitly write deterministic logic (e.g., `if-else` statements, physical design rule checks) that transforms input data into outputs. The system cannot handle scenarios outside hardcoded rules.
* **Machine Learning (ML):** Instead of hand-coding rules, engineers feed paired input data and target outputs into an algorithm. The system automatically learns mathematical patterns (parameters) from data to produce a predictive model.
* **Artificial Intelligence (AI):** The overarching field encompassing any system that demonstrates intelligent behavior—including hardcoded expert systems, heuristics, search algorithms, and machine learning models.

---

## 2. Concept Hierarchy Map

```text
[ Artificial Intelligence (AI) ]
   └── [ Machine Learning (ML) ]
          └── [ Deep Learning (DL) ]
                 ├── [ Generative AI (GenAI) ]
                 └── [ Large Language Models (LLMs) ]

`````

3. Five Key Conceptual Distinctions
   Automation ≠ AI: Automating a repetitive sequence of CAD tool clicks via a TCL shell script is automation, but it is deterministic and does not involve AI or learning.
   AI ≠ ML: Expert systems like A* pathfinding algorithms or deterministic state machines are AI techniques, but they do not use machine learning or learn from data.
   ML Paradigm vs. ML Task: Supervised Learning is a learning paradigm (how a model receives training signals), while Classification is a task type (predicting a discrete category).
   Deep Learning vs. Traditional ML: Traditional ML (e.g., Linear Regression, Random Forests) relies heavily on hand-engineered features, whereas Deep Learning automatically extracts hierarchical feature representations using deep neural networks.
   Generative AI vs. Discriminative AI: Discriminative ML models predict labels or numerical values based on input features ($P(Y\vert{}X)$), whereas Generative AI models generate new novel data distributions ($P(X)$).

