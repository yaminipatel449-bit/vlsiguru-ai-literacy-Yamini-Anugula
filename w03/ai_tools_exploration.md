# AI Tools Exploration & Verification Log

## 1. Tools Explored & Primary Use Cases
* **ChatGPT (OpenAI):** Used for breaking down complex Python concepts and generating structured practice quizzes.
* **Gemini (Google):** Used for cross-referencing concepts and analyzing documentation snippets.
* **Claude (Anthropic):** Used for analyzing technical writing and refining prompt structures.
* **NotebookLM (Google):** Grounded study using imported notes (W02 assignment) to query concepts with direct source citations.
* **Perplexity:** Used for initial technical research to discover direct primary documentation and source links.

---

## 2. Prompt Engineering Experiments

### Example 1: Concept Explanation
* **Initial Prompt:**  
  > "Explain static timing analysis."
* **Improved Prompt (Adding Context, Constraints, and Output Format):**  
  > "Act as a VLSI engineering mentor. Explain Static Timing Analysis (STA) to a beginner python/VLSI student. Use an analogy, keep it under 200 words, and structure the output into three parts: Definition, Key Metric (Setup/Hold time), and Why it matters."
* **Improvement Observed:** The initial prompt gave a dense, textbook-level response with heavy jargon. The improved prompt provided a clear, digestible explanation using a race-track analogy, making setup/hold timing immediately clear.

### Example 2: Active Recall & Finding Knowledge Gaps
* **Prompt Used:**  
  > "Act as a Python interviewer. Ask me 3 beginner-to-intermediate questions on Python dictionary methods one by one. Wait for my answer before asking the next question, and provide constructive feedback after each answer."
* **Outcome:** Created an interactive quiz loop that immediately highlighted gaps in my understanding of `.get()` default fallbacks versus key checking.

---

## 3. AI Claim Verification & Fact-Checking Experiment

* **Tool Tested:** Perplexity / ChatGPT
* **AI Claim:** *"OpenSTA is a standalone Static Timing Analysis engine that supports multi-corner multi-mode (MCMM) timing analysis out of the box."*
* **Verification Process:** Checked the statement against the official OpenSTA GitHub repository / documentation.
* **Primary Source URL:** `https://github.com/parallaxsw/OpenSTA`
* **Verification Finding:** The claim is **correct**. The official documentation confirms OpenSTA is an open-source, gate-level static timing verifier capable of handling scale-up designs and multi-corner analysis.
* **Takeaway:** Verifying against primary repository documentation ensures that AI assertions are backed by actual source capabilities before integration into engineering workflows.
