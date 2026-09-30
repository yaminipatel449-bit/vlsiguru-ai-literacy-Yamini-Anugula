# Week 01 Questions
_____________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________________

### Q1 — AI vs ML vs DL vs GenAI vs Agents

### A — Answer
**Artificial Intelligence (AI):**
The overarching field of building smart machines that can mimic human-like intelligence, decision-making, or problem-solving.
Ex: Non-player characters (NPCs) in video games following scripted logic.

**Machine Learning (ML):** 
A specific approach inside AI where we feed algorithms data so they can spot patterns on their own, rather than writing code with endless if-else statements.
Ex: My bank detecting unusual card transactions and flagging potential fraud.

**Deep Learning (DL):**
A specialized branch of ML that uses multi-layered neural networks to handle really complex, unstructured data like images, audio, and text.
Ex: Google Photos grouping photos of my face automatically over time.

**Generative AI (GenAI):** 
A targeted type of Deep Learning that doesn't just recognize patterns—it actually creates brand-new content like text, code, or images based on what it learned.
EX: Asking Gemini to draft a reply to an email or rewrite a paragraph.

**AI Agent:** 
A proactive setup built on top of AI models that can plan steps, use external tools, make decisions, and complete a multi-step task on its own.
Ex: An AI assistant that reads my schedule, finds open slots, sends meeting invites to my team, and attaches relevant files without me doing each step manually.


### E — Evidence

### Concept Map:

[ Artificial Intelligence (AI) ]---> [ Machine Learning (ML) ]---> [ Deep Learning (DL) ]---> [ Generative AI (GenAI) ]---> System/Workflow Level: [ AI Agent ]  - (Uses GenAI/LLM as the thinking core + connects to tools & memory to take action)

### V — Verification
# I cross-checked these definitions with two primary technical resources:
1. IBM Cloud Education: "AI vs. Machine Learning vs. Deep Learning" — verified that ML sits inside AI, and DL is a deeper branch focused on complex neural networks.
2. DeepLearning.AI (Andrew Ng's AI for Everyone): Confirmed that GenAI models focus on creating content, while Agentic workflows add planning, execution, and tool usage to achieve specific goals.

### R — Reflection
1. What I Learned: AI isn't just one big monolith; it's a series of focused subfields. Moving from ML to DL lets us skip manual feature extraction, and GenAI moves us from plain prediction to creation.
2. GenAI vs. Agentic Systems: A basic GenAI model is purely reactive—it takes a prompt, outputs text, and stops. An AI Agent uses that model as its central brain but adds an active loop: it can call APIs, run checks, correct its own errors, and carry out a full task from start to finish.

## Q2 — Is Everything That Looks Intelligent Actually AI?

### A — Answer

#### Scenario Classification Table:

| Scenario | Classification | Reason / Justification |
| :--- | :--- | :--- |
| **A. Calculator ($25 \times 16 = 400$)** | Deterministic / Traditional Software | Executes fixed arithmetic logic programmed directly into hardware/software circuits. Zero learning or pattern matching involved. |
| **B. Temperature Alert ($>80^\circ\text{C}$ Warning)** | Deterministic / Traditional Software | Follows a strict, human-written conditional rule (`IF temp > 80 THEN warning`). It cannot adapt or evaluate context beyond this hardcoded threshold. |
| **C. Email Spam Filter** | Machine Learning-Based AI | Analyzes incoming email features against statistical patterns learned from millions of past spam and non-spam messages to predict probability. |
| **D. AI Assistant Summary** | Generative AI | Uses a large language model to interpret context, extract key meaning, and generate fresh explanatory text. |
| **E. Navigation ETA Prediction** | Machine Learning-Based AI | Dynamically processes real-time traffic data, weather, historical speeds, and route patterns to predict estimated travel duration. |

#### Deterministic Software vs. AI Systems:
Traditional deterministic software relies entirely on explicit, human-coded instructions (`if/else` logic) where the exact outcome for any given input is pre-engineered. An AI system, by contrast, relies on statistical models trained on data. Instead of following fixed hardcoded paths, it infers patterns, learns general rules, and generalizes to handle unseen inputs or generate novel outputs based on probability.

### E — Evidence

- **Scenario B vs Scenario C Comparison:** A rule-based spam filter would fail if spammers simply altered one word (e.g., spelling "FREE" as "F R E E"). An ML-based spam filter detects semantic patterns across multiple features (sender domain, token distributions, link structures) without needing a manual rule for every variation.
- **Observation:** Deterministic programs always produce identical, predictable outputs for a given input, whereas AI models evaluate probabilities and can handle nuance or variability in real-world data.

### V — Verification

I verified this conceptual distinction using two standard educational references:
1. **Google Cloud AI/ML Fundamentals:** *"Introduction to Machine Learning"* — explicitly defines the shift from traditional programming (Input + Rules = Output) to Machine Learning (Input + Output = Rules/Model).
2. **MIT OpenCourseWare (6.0001):** Confirms that deterministic algorithms execute explicit instructions step-by-step, whereas machine learning systems approximate functions and adapt decisions based on training data distributions.

### R — Reflection

- **What I Learned:** Calling every smart feature "AI" is a common marketing mistake. Automation and intelligence are not the same thing—if a system just checks a pre-written rule or runs a fixed formula, it is traditional software, no matter how fast or useful it is.
- **Key Takeaway:** An AI label requires that the system learns from data, detects probabilistic patterns, or generates content rather than merely executing human-written conditional code.
