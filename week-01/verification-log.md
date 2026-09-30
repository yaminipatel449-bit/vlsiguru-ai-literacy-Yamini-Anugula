# Verification Log — Week 01

## Claim 1: Hold Time Violation Behavior in Flip-Flops
- **Source Prompt / Origin:** Generated during Q4 hallucination experiment.
- **Initial AI Output:** Model claimed that violating hold time causes metastability and "destroys the physical circuit hardware."
- **Verification Strategy:** Cross-checked claim against standard digital design textbook literature (*Digital Design: Principles and Practices* by John F. Wakerly) and IEEE academic course notes on VLSI timing analysis.
- **Finding:** **Partly False / Overstated.** Hold time violations cause metastability and functional logic/data corruption, but they do NOT physically damage or destroy silicon hardware.
- **Action Taken:** Corrected the claim in Q4 to reflect functional timing failure/metastability rather than physical damage.

---

## Claim 2: Asynchronous Reset Glitch and Recovery Timing Hazards
- **Source Prompt / Origin:** Generated during Q5 comparison between AI, Search, and Textbooks.
- **Initial AI Output:** Model explained synchronous vs. asynchronous reset definitions but omitted recovery/removal timing hazards when deasserting an asynchronous reset.
- **Verification Strategy:** Cross-checked against Xilinx Application Note WP272 (*"Get Smart About Resets"*).
- **Finding:** **Incomplete.** Deasserting an asynchronous reset near a clock edge can cause metastability if reset recovery/removal time is violated, requiring a reset synchronizer circuit in actual ASIC/FPGA designs.
- **Action Taken:** Updated Q5 verification notes to highlight reset recovery timing hazards as a boundary condition missed by basic AI summaries.

---

## Claim 3: Building Blocks of Autonomous AI Agents
- **Source Prompt / Origin:** Generated during Q6 agent architecture definition.
- **Initial AI Output:** Described AI agents as "advanced chatbots that use APIs."
- **Verification Strategy:** Cross-checked against Lilian Weng's (OpenAI) architectural reference guide (*"LLM Powered Autonomous Agents"*).
- **Finding:** **Verified & Refined.** An AI Agent architecture specifically consists of four distinct components: Brain (LLM), Memory (Short/Long term), Planning (Goal decomposition), and Tool Use (APIs).
- **Action Taken:** Structured Q6 around the formal 4-part architectural definition and included the ASCII workflow diagram.
