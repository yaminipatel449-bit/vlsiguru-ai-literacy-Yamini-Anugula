# Missions 5 to 9 Log

## Mission 5: Can AI Be Confidently Wrong?

* **Prompt Used:** "What is the exact TCL command in OpenSTA to set max transition constraint on a clock net?"
* **AI Answer:** set_max_transition 0.5 [get_clocks clk]
* **Verification Source:** Official OpenSTA Documentation / Manual.
* **Verification Result:** Incomplete / Incorrect syntax context. In SDC/OpenSTA standard syntax, set_max_transition applies to design ports, pins, or clock domains, but setting constraints directly on internal nets requires specific target object validation.
* **Lesson Learned:** Highly structured syntax must always be validated against official EDA manuals; persuasive formatting does not guarantee functional execution.

---

## Mission 6: Chatbot vs. Agent Workflows

User Prompt ---> AI Model (LLM) ---> Tool / Retrieval (RAG)
                  ^                        |
                  |                        v
               Response <-------------- Result

| Term | Definition |
| :--- | :--- |
| **LLM** | The core probabilistic text prediction model (e.g., GPT-4, Gemini). |
| **AI Application** | The user-facing software wrapper incorporating an LLM (e.g., ChatGPT web interface). |
| **RAG** | Retrieval-Augmented Generation; fetching external document chunks to ground the LLM's response. |
| **Tool-Using Assistant** | An LLM equipped with access to external functions (e.g., web search, calculator, code interpreter). |
| **Agent** | An autonomous system that plans, executes multi-step workflows, evaluates tool outputs, and adjusts actions toward a goal. |

* **Everyday Agentic Workflow Example:** An automated travel booking assistant that searches flight options, verifies user calendar availability, queries weather forecasts, selects optimal options, and submits a booking reservation.

---

## Mission 7: What Actually Runs AI? (Hardware Fundamentals)

1. **CPU:** General-purpose processor optimized for low-latency sequential tasks and complex logic branch processing.
2. **GPU:** Highly parallel hardware designed to process thousands of matrix multiplication operations concurrently, ideal for deep learning tensor compute.
3. **NPU / AI Accelerator:** Purpose-built domain-specific silicon optimized specifically for matrix operations, low-bit precision quantization (INT8/FP16), and low-power inference.
4. **Parallel Computation:** Executing thousands of compute operations simultaneously across parallel cores rather than sequentially.
5. **Compute & Memory Dependence:** Deep learning involves millions to billions of matrix parameters; training/inference requires massive FLOPS and memory bandwidth (HBM) to prevent memory bottlenecks.
6. **Training vs. Inference:**
   * **Training:** Computationally intensive, backpropagation-heavy, gradient updates requiring high precision (FP32/FP16) across GPU clusters.
   * **Inference:** Forward-pass execution of a pre-trained model on new input data, often quantized for edge efficiency.

AI Application ---> AI Framework (PyTorch/TensorFlow) ---> Hardware (CPU/GPU/NPU) <---> Memory (HBM/DRAM)

* **Workload Example:** Running floorplanning routability prediction. A GPU / NPU is ideal due to heavy grid-matrix convolutions and parallel spatial data evaluations.

---

## Mission 8: Application to Physical Design (PD)

| PD Task | Repetitive / Search Task | How AI Helps | Why Domain Knowledge Still Matters |
| :--- | :--- | :--- | :--- |
| **Floorplanning & Placement** | Searching high-dimensional design space for optimal macro placement to minimize congestion and wirelength. | Reinforcement learning models can evaluate thousands of placement options faster than manual floorplanning. | PD engineers must verify thermal density, power delivery network (PDN) integrity, and DRC tapeout compliance. |

---

## Mission 9: AI Working Agreement (5 Personal Rules)

1. **Verification Rule:** Never execute AI-generated scripts or TCL/Python commands in EDA tools without line-by-line inspection and syntax verification against primary documentation.
2. **Confidentiality Rule:** Never paste proprietary RTL, netlists, timing constraints (.sdc), or commercial EDA license data into public AI chat interfaces.
3. **Responsibility Rule:** I am solely responsible for engineering decisions, tapeout checks, and code submitted in my assignments—AI is only an assistant.
4. **Grounded Learning Rule:** Use AI to explain unfamiliar concepts or build active recall quizzes, but verify core engineering definitions against trusted engineering textbooks or official manuals.
5. **Code Review Rule:** Test and step-debug all AI-suggested scripts on minimal toy datasets before scaling to larger workloads.
