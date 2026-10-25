# Open-Source VLSI Tool Investigation: OpenROAD / OpenSTA

## 1. Tool Overview
* **Tool Name:** OpenSTA (via OpenROAD project)
* **Target Track:** Physical Design (PD) / Design Implementation
* **Problem Solved:** Performs Static Timing Analysis (STA) to ensure integrated circuit designs satisfy setup and hold time requirements across specified process corners without running full gate-level simulations.

## 2. Inputs and Outputs
* **Main Inputs:**
  * Gate-level Netlist (`.v` / `.sv`)
  * Standard Cell Timing Libraries (`.lib`)
  * Design Constraints (`.sdc` file specifying clock frequencies, input/output delays)
  * Parasitic extraction data (`.spef`)
* **Main Outputs:**
  * Timing Slack Reports (Setup and Hold violations)
  * Critical Path Reports
  * Worst Negative Slack (WNS) and Total Negative Slack (TNS) summary metrics

## 3. Practical Exploration / Workflow Understanding
* Examined the tool documentation and example scripts provided in the OpenROAD repository.
* Reviewed how Liberty (`.lib`) files define cell delays and how SDC constraint files set operational limits for clock domains.
* Traced the basic TCL command sequence used to load libraries, set constraints, and execute `report_checks`.

## 4. Potential AI/ML Integration
* **ML Application in STA / Timing Closure:** Machine learning models can predict interconnect wire parasitics (RC values) and timing slack violations *prior* to full detailed routing. This enables faster floorplanning iterations without incurring the runtime penalty of full 3D parasitic extraction and full STA loops.
