# Missions 1 to 4 Log

## Mission 1: Find AI Around You

| System / Feature | Main Function | Evidence / Verification | Could a Rule-Based Program Do This? |
| :--- | :--- | :--- | :--- |
| Google Maps Traffic ETA | Predicts travel time and classifies route congestion. | Google official documentation confirms Graph Neural Networks (GNNs) analyze historical and live speed patterns. | Partially, but simple static rules cannot dynamically adapt to real-time non-linear traffic changes. |
| Gmail Spam Filter | Classifies incoming emails into 'Spam' or 'Inbox'. | Google Security docs specify TensorFlow models analyze text embeddings and sender reputational vectors. | Basic keyword rules work for simple spam, but fail against modern adversarial phishing attempts. |
| YouTube Recommendations | Recommends relevant videos based on user watch history. | Deep Neural Network architecture published in research papers (Covington et al.). | No, deterministic rules cannot scale to personalize billions of dynamic video-user interactions. |

**Conclusion:** AI/ML is most effective when handling high-dimensional, non-linear pattern recognition where hardcoded `if-else` rules are impractical or unscalable.

---

## Mission 2: AI, ML, Deep Learning & GenAI Hierarchy

```text
[ Artificial Intelligence (AI) ]
   └── [ Machine Learning (ML) ]
          └── [ Deep Learning (DL) ]
                 └── [ Generative AI (GenAI) ]
