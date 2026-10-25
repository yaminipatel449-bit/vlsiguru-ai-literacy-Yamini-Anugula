# Missions 1 to 4 Log

## Mission 1: Find AI Around You

| System / Feature | Main Function | Evidence / Verification | Could a Rule-Based Program Do This? |
| :--- | :--- | :--- | :--- |
| Google Maps Traffic ETA | Predicts travel time and classifies route congestion. | Google official documentation confirms Graph Neural Networks (GNNs) analyze historical and live speed patterns. | Partially, but simple static rules cannot dynamically adapt to real-time non-linear traffic changes. |
| Gmail Spam Filter | Classifies incoming emails into 'Spam' or 'Inbox'. | Google Security docs specify TensorFlow models analyze text embeddings and sender reputational vectors. | Basic keyword rules work for simple spam, but fail against modern adversarial phishing attempts. |
| YouTube Recommendations | Recommends relevant videos based on user watch history. | Deep Neural Network architecture published in research papers (Covington et al.). | No, deterministic rules cannot scale to personalize billions of dynamic video-user interactions. |

**Conclusion:** AI/ML is most effective when handling high-dimensional, non-linear pattern recognition where hardcoded if-else rules are impractical or unscalable.

---

## Mission 2: AI, ML, Deep Learning & GenAI Hierarchy

* Artificial Intelligence (AI)
  └── Machine Learning (ML)
         └── Deep Learning (DL)
                └── Generative AI (GenAI)

### Explanations:
* **Artificial Intelligence (AI):** The broad field of computer science focused on building systems capable of performing tasks that typically require human intelligence (e.g., decision making, problem solving).
* **Machine Learning (ML):** A subset of AI where algorithms learn patterns from data to make predictions or decisions without being explicitly programmed.
* **Deep Learning (DL):** A specialized branch of ML based on multi-layered artificial neural networks capable of learning complex representations from vast datasets.
* **Generative AI (GenAI):** A subfield of Deep Learning focused on creating new, original content (text, code, images, audio) based on learned patterns from training data.

---

## Mission 3: Is It Really AI?

| Application | Classification | Justification |
| :--- | :--- | :--- |
| Calculator | Rule-based / Traditional Software | Operates on deterministic arithmetic logic; no data learning involved. |
| Temperature Warning Rule | Rule-based / Traditional Software | Simple if temp > threshold logic. |
| Spam Filter | ML-based AI | Learns feature representations to classify emails as spam or legitimate. |
| Document Summariser | Generative AI | Uses Large Language Models (LLMs) to synthesize and generate novel text summaries. |
| Traffic ETA Prediction | ML-based AI | Uses predictive models trained on historical and real-time temporal spatial data. |

* **Easy Classification:** **Calculator.** It follows hardcoded, deterministic mathematical rules where inputs always produce identical, exact outputs.
* **Difficult Classification:** **Traffic ETA Prediction.** While simple distance/speed calculations exist, modern ETA relies heavily on historical ML predictions combined with real-time routing algorithms.
* **Custom Example:** **Synthesizable Netlist Verification Rule Check.** Running a strict DRC/LVS check in layout is **rule-based software**; predicting congestion hotspots during pre-placement floorplanning using trained GNNs is **ML-based AI**.

---

## Mission 4: Make AI Explain Itself & Test It

### Simplified Explanation of LLM Output Generation:
A Large Language Model (LLM) predicts text one token (word or word piece) at a time. Think of it like an advanced predictive keyboard: given an input prompt, it calculates the statistical probability of what token should come next based on patterns learned during training on billions of text examples.

### Fact-Checking Verification:
* **Claim:** LLMs calculate exact next-token probability distributions using attention mechanisms.
* **Sources Checked:** Transformer Architecture Paper ("Attention Is All You Need", Vaswani et al.) and official OpenAI documentation.
* **Finding:** Verified correct.
* **Clarification Needed:** The AI initially implied LLMs "think" or "retrieve database answers." I had to clarify that LLMs perform probabilistic autoregressive inference, not database lookup.
