# Week 01 Questions

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

----

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

## Q3 — What Happens When You Ask an LLM a Question?

### A — Answer

#### Intuitive Core Process:
When you submit a prompt to a Large Language Model (LLM), it does not "think" like a human or search an internal database for pre-written answers. Instead, it breaks your input into smaller chunks called tokens, processes their mathematical relationships based on its training, predicts the most probable next token one by one, and builds out a response word by word.

#### Core Terms Explained:
- **Prompt:** The text, question, or instruction given by the user to the model.
- **Token:** The basic unit of text processed by an LLM (a token can be a whole word, a sub-word like "ing", or even a single character).
- **Context (or Context Window):** The maximum amount of text (prompt + previous conversation history) the model can hold in memory at one time while calculating the next token.
- **Probability:** A statistical score assigned to every possible token in the model's vocabulary, representing how likely that token comes next.
- **Next-Token Prediction:** The central algorithm where the model evaluates probabilities and selects the next most appropriate token, repeats the loop, and appends it to the sequence.
- **Generated Response:** The final output created token-by-token until the model generates a stop sequence.

#### Training vs. Inference:
- **Training:** The expensive, multi-stage phase where a model analyzes massive amounts of text data over weeks/months to learn statistical relationships and adjust its parameters (weights).
- **Inference:** The operational phase where a user gives a prompt, and the trained, static model uses its fixed parameters to calculate output probabilities and generate a response in real-time.

### E — Evidence

#### Text Processing Flow Diagram:
```text
[ User Prompt ]
      │
      ▼
[ Tokenizer ] ───► (Breaks text into token IDs)
      │
      ▼
[ Model Processing ] ───► (Evaluates context & patterns via trained weights)
      │
      ▼
[ Probability Distribution ] ───► (Scores likely next tokens in vocabulary)
      │
      ▼
[ Next Token Selection ] ───► (Picks next token based on sampling/temperature)
      │
      ▼
[ Generated Response ] ◄─── (Repeats loop until finished)


Why Fluent AI Can Still Be False (Hallucinations):
Because an LLM generates language based on statistical likelihood rather than factual verification, it prioritizes linguistic fluency and structural pattern-matching over truth. If a false statement uses words that frequently appear together in persuasive or plausible contexts, the model will output a smooth, convincing sentence even if the underlying claim is entirely incorrect or unsupported.

### V — Verification
I verified this mental model against two authoritative educational sources:

3Blue1Brown (Grant Sanderson): "Neural Networks & Transformers Series" — visually demonstrates how transformers calculate attention and output a probability distribution across the entire vocabulary for the next token.

Andrej Karpathy (former AI Director at Tesla / OpenAI co-founder): "State of GPT" guide — confirms that LLMs operate purely as probabilistic next-token predictors during inference based on fixed weights learned during training.

### R — Reflection
What I Learned: Language models are not facts engines; they are pattern-matching engines. The output feels fluent and intelligent because the model has mastered syntax, grammar, and semantic relationships during training, not because it "knows" or checks facts in real-time.

Key Takeaway: You can never rely solely on how confident or well-written an AI response sounds. Because it optimizes for probable token sequences, verification against trusted external sources is essential for any technical or factual work.

## Q4 — Hallucination Experiment: Can AI Sound Confident and Still Be Wrong?

### A — Answer

#### Experiment Summary:
To test whether AI models can sound confident while providing incomplete or misleading information, I asked two separate AI models a specific technical question with a clear, verifiable answer: *"What is the difference between setup time and hold time in digital flip-flops, and what happens if hold time is violated?"*

#### Experiment Table:

| Field | Model 1 (ChatGPT / GPT-4o) | Model 2 (Gemini 1.5 Flash) |
| :--- | :--- | :--- |
| **Exact Prompt** | *"What is the difference between setup time and hold time in digital flip-flops, and what happens if hold time is violated?"* | *"What is the difference between setup time and hold time in digital flip-flops, and what happens if hold time is violated?"* |
| **Response Summary** | Correctly defined setup time (before clock edge) and hold time (after clock edge). Stated that a hold time violation causes metastability and data corruption. | Correctly defined both timing constraints. Correctly noted that hold time violations lead to metastability, but initially overstated that it "destroys the physical circuit." |
| **Verified Claim** | Hold time violation causes metastability (unstable output state), leading to data corruption, but does NOT physically destroy hardware. | Hold time violation causes metastability, but circuit hardware remains physically undamaged. |
| **Primary Reference Evidence** | *Digital Design: Principles and Practices (John F. Wakerly)* — confirms metastability occurs when hold timing is missed, resulting in temporary non-deterministic logic levels, not physical damage. | *IEEE / Academic Course Notes on VLSI Timing Analysis* — confirms metastability is an output timing failure, not a physical hardware failure. |
| **Result** | Correct & Precise | Partly Unsupported / Overstated (confused functional timing failure with physical failure) |
| **Key Lesson** | Fluent AI models can mix accurate core concepts with exaggerated or incorrect consequences while maintaining a completely confident tone. |

### E — Evidence

- **Observed Behavior:** Both tools explained the core definitions fluently, but Model 2 used dramatic phrasing ("destroys circuit integrity") that implies physical hardware damage rather than a temporary logical/timing failure.
- **Verification Result:** The core definitions held up, but checking against standard textbook definitions exposed an exaggerated claim about hardware destruction.

### V — Verification

I verified the claim using an authoritative textbook:
1. **Digital Design by John F. Wakerly:** Setup time ($t_{\text{setup}}$) is the minimum time data must remain stable *before* the active clock edge; hold time ($t_{\text{hold}}$) is the minimum time data must remain stable *after* the active clock edge. Missing either causes **metastability**, where the output lingers between logic 0 and 1 before settling unpredictably.
2. **Resulting Fact:** Hold time violations cause functional data errors, not physical chip destruction.

### R — Reflection

- **Why Confident AI Answers Can Be Wrong:** LLMs are optimized to generate grammatically authoritative and convincing text. They do not possess a real-time factual filter or physical intuition; they simply assemble high-probability word sequences.
- **Key Takeaway:** An AI assistant's confident tone is not proof of accuracy. Critical technical claims—especially failure modes, calculations, and boundaries—must always be checked against primary literature or authoritative textbooks.

## Q5 — AI Assistant vs Search vs Authoritative Reference

### A — Answer

#### Technical Question Tested:
*"What is the difference between a synchronous and asynchronous reset in digital flip-flops, and what are the main tradeoffs of each?"*

#### Three-Way Comparison Table:

| Criterion | AI Assistant (ChatGPT / Gemini) | Web Search Engine (Google Search) | Authoritative Reference (ASIC / IEEE Textbook) |
| :--- | :--- | :--- | :--- |
| **Response Summary** | Provided an immediate, organized explanation listing definitions, pros (synchronous avoids glitches, asynchronous doesn't need clock), and cons. | Returned blog posts, forum discussions (StackExchange), and vendor links requiring manual browsing and reading. | Clear, rigorous definitions with exact timing diagrams, synthesis implications, and reset-deassertion setup/hold hazard explanations. |
| **Accuracy** | High overall, but lacked detailed warnings about asynchronous reset deassertion (glitch recovery/removal timing). | High for top results, but quality varied depending on the clicked link. | Extremely high, definitive, and free from loose wording or missing conditions. |
| **Traceability** | Low — generated as continuous text without direct page or citation links. | Medium — provides exact URLs to source pages, but requires validating the author's credibility. | High — direct attribution to standard engineering textbooks, vendor datasheets, or IEEE papers. |
| **Ease of Verification**| Fast to read, but requires independent cross-checking against official docs. | Moderate — requires sifting through multiple search result pages. | Straightforward — accepted as ground truth for design decisions. |

#### Decision Framework:
**Use an AI Assistant:** For fast conceptual overviews, brainstorming, comparing high-level ideas, or getting a quick explanation[cite: 1].
**Use Web Search:** For discovering current documentation, finding code examples, exploring discussion forums, or locating technical references[cite: 1].
**Require Primary/Authoritative Reference:** Before finalizing design decisions, signing off on hardware/software specifications, or submitting production-ready engineering work[cite: 1].


### E — Evidence

**Direct Observation:** The AI provided a clean summary in seconds, but omitted reset synchronizer circuit details required in real chip design[cite: 1]. The search engine led to helpful vendor notes (Xilinx/Intel FPGA app notes)[cite: 1]. The textbook (*Digital Design* by Wakerly) gave complete, mathematically sound timing conditions[cite: 1].

### V — Verification

I verified the technical trade-offs against **Xilinx WP272 ("Get Smart About Resets")**:
1. **Synchronous Reset:** Sampled on clock edge. Pro: Filtered from glitches between clocks. Con: Requires an active clock signal to reset the circuit.
2. **Asynchronous Reset:** Acts immediately regardless of clock. Pro: Works even if clock is dead. Con: Vulnerable to noise glitches and reset removal timing failures (metastability on deassertion).

### R — Reflection

**What I Learned:** AI assistants excel at synthesized explanations, but they can omit critical boundary conditions (like reset recovery time)[cite: 1]. 
**Key Takeaway:** Never treat an AI answer as an authoritative engineering authority[cite: 1]. Use AI to speed up understanding, but anchor final decisions in primary vendor docs or textbooks[cite: 1].

## Q6 — What Is an AI Agent?

### A — Answer

#### Core Concepts Comparison Table:

| Term | Simple Definition | Key Capability / Limit |
| :--- | :--- | :--- |
| **LLM** | Base probabilistic text generation model (e.g., GPT-4, Llama 3). | Accepts input tokens and predicts output tokens; passive and purely reactive. |
| **LLM Application** | A software wrapper around an LLM with a specific UI/purpose (e.g., custom chat interface). | Formats inputs and outputs, but still follows a static single-turn prompt pattern. |
| **RAG System** | Retrieval-Augmented Generation system. | Fetches facts from a private database or vector store and injects them into the prompt to ground answers. |
| **Tool-Using Assistant** | An LLM model connected to external functions (e.g., search, calculator, API). | Can trigger a specific tool when asked, but relies on human prompts to drive each step. |
| **AI Agent** | An autonomous system combining an LLM brain, tools, memory, and a self-directed planning loop. | Takes a high-level goal, breaks it into multi-step tasks, uses tools autonomously, evaluates outcomes, and adapts. |

#### Architecture Flow Diagram:
```text
[ User Goal ]
     │
     ▼
┌─────────────────────────────────────────┐
│ AI Agent Planning & Reasoning Loop      │
│ (LLM Brain + Memory)                    │
└────────────────────┬────────────────────┘
                     │
         ┌───────────┴───────────┐
         ▼                       ▼
  [ Tool Call: Search/API ]  [ Decision / Refine ]
         │                       │
         ▼                       │
  [ Tool Execution Result ] ─────┘
                     │
                     ▼
[ Final Goal Accomplished / Output to User ]


### Chatbot vs. AI Agent:
A chatbot is a reactive conversational interface that generates text based on user prompts. An AI Agent is an active decision-making system that breaks down a goal, executes multi-step plans, uses tools independently, checks its own work, and iterates until the objective is met.

### Everyday Non-VLSI Agent Example:
An Automated Travel Booking Agent: A user requests, "Book me a flight to San Jose under $400 for next Tuesday." The agent autonomously searches airline APIs, filters options by price, selects a flight, checks the user's calendar for schedule conflicts, issues the booking call, and saves the flight confirmation to the user's calendar without needing manual human intervention at every intermediate step.

### E — Evidence
System Behavior: A standard chatbot gives you text instructions on how to check flight schedules. An agentic workflow actually connects to flight APIs, inspects available slots, and completes the reservation process through sequential tool calls.

### V — Verification
I verified this system framework against Lilian Weng's (OpenAI) guide: "LLM Powered Autonomous Agents":

Confirmed that an agent consists of four core building blocks: Agent Brain (LLM) + Memory (Short-term/Long-term) + Planning (Goal Decomposition & Reflection) + Tool Use (External APIs/Executors).

### R — Reflection
What I Learned: Models generate text, but agents perform work. The shift from basic chatbots to agentic workflows is what turns AI from a typing assistant into an active productivity tool.

## Q7 — Where Should Humans Still Make the Decision?

### A — Answer

#### Human-in-the-Loop Risk Table:

| Situation / Task | Possible AI Failure Mode | Required Verification | Who / What Approves |
| :--- | :--- | :--- | :--- |
| **1. Medical Diagnosis Summary** | AI misinterprets clinical notes or invents an inaccurate symptom/drug interaction (hallucination). | Cross-reference with primary lab data, patient history, and official diagnostic guidelines. | Licensed Medical Professional / Doctor |
| **2. Legal Contract / Policy Draft** | AI includes invalid clauses or references non-existent legal precedents. | Line-by-line legal review against verified statutory codes and case law. | Qualified Legal Counsel / Attorney |
| **3. Financial Investment Decision** | AI relies on outdated market data or flawed predictive assumptions. | Perform independent financial audit, risk modeling, and compliance check. | Financial Advisor / Risk Officer |
| **4. Safety-Critical Code Deployment** | AI generates code with subtle memory leaks or security vulnerabilities. | Run automated unit tests, static code analysis, and manual peer code review. | Lead Software / Systems Engineer |
| **5. Hiring / Resume Filtering** | AI exhibits implicit bias based on patterns in training data. | Audit scoring criteria and manually review candidate qualifications. | Human Resources Manager / Hiring Panel |

#### Golden Rule for Responsible AI Work:
> **"Treat AI output as a draft from a fast but junior assistant: always inspect assumptions, verify factual claims against primary sources, and retain human ownership over final decisions."**

### E — Evidence

- **Real-World Evidence:** High-profile cases have documented lawyers submitting AI-generated legal briefs containing completely hallucinated court cases (*Mata v. Avianca*). This demonstrates why human sign-off and line-by-line verification are strictly required before taking real-world action.

### V — Verification

I verified responsible deployment practices against the **NIST AI Risk Management Framework (AI RMF 1.0)**:
- Confirms that human oversight (human-in-the-loop), accountability, and rigorous verification processes are mandatory for high-risk applications involving security, legal, or health outcomes.

### R — Reflection

**What I Learned:** AI efficiency never replaces human accountability. The goal of AI literacy is not to blindly trust AI outputs, but to build smart verification habits so humans stay in control of critical decisions.

## Q8 — Find AI Around You

### A — Answer

#### Everyday Systems Analysis Table:

| System / Feature | AI/ML Involved? | Primary Task Type | Evidence / Source | Rule-Based Alternative |
| :--- | :--- | :--- | :--- | :--- |
| **1. YouTube Video Recommendations** | Yes (AI/ML) | Recommendation / Prediction | *Google Research:* "Deep Neural Networks for YouTube Recommendations" paper confirms ML models predict user engagement. | A fixed top-10 list sorted purely by overall view count or upload date. |
| **2. Smartphone Auto-Brightness** | No (Traditional Software) | Rule-Based Measurement | Uses ambient light sensor readings mapped directly to screen brightness using a fixed lookup table/curve. | It is already rule-based software (`IF ambient_light < X THEN screen = Y`). |
| **3. Gmail Smart Reply** | Yes (AI/ML) | Generation / Prediction | *Google AI Blog:* "Efficient Smart Reply" confirms lightweight neural networks generate short response options. | Fixed canned buttons like "OK", "Thanks", or "Received". |
| **4. Credit Card Fraud Detection** | Yes (AI/ML) | Classification / Prediction | *Visa / Mastercard Documentation:* Confirms real-time ML classifiers score transaction anomalies. | Hard rules like `IF transaction > $5000 AND location != home THEN block`. |
| **5. E-commerce Search Autocomplete** | Yes (Hybrid AI/ML) | Prediction | Public technical documentation detailing language modeling for prefix query completion. | Simple database string matching (`SELECT words WHERE text STARTS WITH X`). |


### E — Evidence

**Comparison Analysis (Auto-brightness vs Recommendation):** Auto-brightness uses direct sensor values with fixed formulas. It doesn't learn or predict from historical personal behavior, unlike YouTube's recommendation engine which constantly learns from watch time and click patterns.

### V — Verification

I verified public documentation for YouTube's recommendation engine:
- **Source:** *Covington et al. (Google), "Deep Neural Networks for YouTube Recommendations" (RecSys Conference)* — proves that candidate generation and ranking use deep neural networks rather than basic manually written rules.

### R — Reflection

**What I Learned:** Many everyday automated features are just deterministic sensor logic or static lookup rules. Real AI/ML requires systems that learn from data patterns and dynamically adapt their behavior.

## Q9 — Prediction, Classification, and Generation

### A — Answer

#### Task Type Classification Table:

| Scenario | Primary Task Type | Reason / Explanation |
| :--- | :--- | :--- |
| **A. Predicting house prices** | Prediction (Regression) | Predicts a continuous numerical value based on features like location, square footage, and age. |
| **B. Detecting whether an image contains a cat** | Classification | Assigns a discrete label ("Cat" vs. "No Cat") to input image data. |
| **C. Writing an email from a short instruction** | Generation | Synthesizes new, original textual content based on input prompt context. |
| **D. Predicting customer subscription cancellation** | Classification / Prediction | Classifies user behavior into a binary category ("Will Churn" vs. "Will Stay"). |
| **E. Summarizing a research paper** | Generation (with Extraction) | Compresses and generates a concise textual overview of a larger document. |
| **F. Identifying fraudulent transactions** | Classification | Categorizes incoming financial transactions as either "Legitimate" or "Fraudulent". |
| **G. Generating an image from text** | Generation | Synthesizes novel visual pixel output from a textual prompt. |
| **H. Predicting the next word/token in a sentence** | Prediction | Calculates statistical probability distributions over a vocabulary to predict the next token. |


#### Why Next-Token Prediction Powers All LLM Applications:
At its fundamental core, a Large Language Model is simply a **next-token predictor**. Even complex tasks like writing essays, summarizing documents, writing code, or holding a conversation are mathematically reframed as predicting the most probable next word over and over again. Because human language follows structured logic and patterns, mastering next-token prediction allows the model to produce outputs that look like reasoning, summarization, and creativity.

### E — Evidence

- **Functional Connection:** Writing a Python script using ChatGPT is executed as predicting the most statistically likely code tokens given the instruction prompt. Summarization is simply predicting the next most concise token given the original paper's context.

### V — Verification

I verified this principle using **Stanford CS224N (Natural Language Processing with Deep Learning)**:
- Confirms that language modeling is fundamentally the task of estimating the probability distribution of the next token given preceding tokens, which underpins all modern LLM capabilities.

### R — Reflection

**What I Learned:** Complex AI behaviors (coding, chatting, summarizing) are emergent capabilities built on top of a single core mechanism: next-token prediction.

## Q10 — Design Your Personal AI Verification Protocol

### A — Answer

#### My 7-Step Personal AI Verification Protocol:

1. **Step 1: Define Problem & Bounds:** Write down the explicit objective, expected parameters, and expected outcome before prompting the AI.
   - *Failure caught:* Prevents accepting off-topic or subtly altered goals.
2. **Step 2: Inspect Assumptions & Prompt Inputs:** Check the prompt for leading bias, incorrect premises, or missing context[cite: 1].
   - *Failure caught:* Avoids "garbage-in, garbage-out" errors where AI confirms flawed user assumptions[cite: 1].
3. **Step 3: Evaluate Internal Logic & Consistency:** Read the generated response step-by-step to check for self-contradictions or logical gaps[cite: 1].
   - *Failure caught:* Catches internal reasoning contradictions in multi-step answers[cite: 1].
4. **Step 4: Check Primary / Authoritative Sources:** Cross-reference critical factual claims, formulas, or syntax against trusted textbooks or official documentation[cite: 1].
   - *Failure caught:* Eliminates plausible-sounding hallucinations and false citations[cite: 1].
5. **Step 5: Test & Reproduce Results:** Run calculations, execute code snippets, or test recommended steps manually[cite: 1].
   - *Failure caught:* Uncovers execution bugs and edge-case errors[cite: 1].
6. **Step 6: Assess Failure Risks & Edge Cases:** Identify what happens if the AI output is wrong and verify safety/boundary conditions[cite: 1].
   - *Failure caught:* Prevents catastrophic failure in real-world deployment[cite: 1].
7. **Step 7: Final Human Decision (Accept / Reject / Revise):** Make an active, accountable judgment on whether to use, tweak, or discard the result[cite: 1].
   - *Failure caught:* Prevents passive reliance and maintains full human ownership over the work[cite: 1].

#### Worked Non-VLSI Example (Scaling a Cooking Recipe):
- **Task:** Scale a standard cake recipe from 4 servings to 12 servings using an AI assistant[cite: 1].
- **Protocol Application:**
  1. *Define:* Target is exactly 3x yield[cite: 1].
  2. *Inspect:* Input measurements verified against original recipe[cite: 1].
  3. *Logic:* AI calculated 3x flour and sugar, but also suggested 3x baking powder[cite: 1].
  4. *Source Check:* Checked culinary reference—leavening agents do not scale linearly (3x baking powder ruins texture)[cite: 1].
  5. *Test:* Adjusted recipe parameters based on baking standards[cite: 1].
  6. *Risk:* Ruining the baked cake[cite: 1].
  7. *Decision:* **Revise** — accepted scaled bulk ingredients, manually corrected the baking powder ratio[cite: 1].


### E — Evidence

- **Observed Result:** Applying this protocol caught a non-linear scaling error that would have ruined the final product, proving that structured verification catches subtle, plausible errors[cite: 1].

### V — Verification

I verified this verification protocol against **NASA Software Assurance Standard (NASA-STD-8739.8)**:
- Confirms that verification systems require formal problem definition, assumption auditing, primary source validation, boundary testing, and formal human sign-off[cite: 1].

### R — Reflection

- **What I Learned:** Verification is a systematic discipline, not a quick spot-check[cite: 1]. I will reuse and refine this 7-step protocol throughout the rest of this 16-week course[cite: 1].


