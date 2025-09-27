# PrathitPatel_VSD_TAPEOUT_Week_1
RISC-V SoC Tapeout Program - Week 1
RTL Design and Simulation Fundamentals
Date: September 21, 2025

Table of Contents
Week 1 Overview
RTL Design Theory and Concepts
Day 1: Environment Setup and RTL Analysis
Workspace Creation and Repository Setup
Workshop Repository Structure Analysis
Library Files Investigation
RTL Design Collection Exploration
Simulation Workflow Implementation
GTKWave Waveform Analysis
Week 1 Day 1 Accomplishments
Repository Structure and Screenshots
Week 1 Overview
Week 1 of the RISC-V SoC Tapeout Program establishes fundamental RTL design and simulation skills. This week focuses on mastering Verilog HDL, understanding standard cell libraries, and implementing comprehensive simulation workflows using open-source EDA tools.

Week 1 Structure
Day 1 (Completed): RTL Design and Simulation Environment Setup
Day 2 (Upcoming): Logic Synthesis and Technology Mapping
Day 3 (Upcoming): Combinational and Sequential Optimizations
Day 4 (Upcoming): Gate Level Simulation and Synthesis-Simulation Mismatch
Day 5 (Upcoming): Design for Testability and If-Case Constructs
RTL Design Theory and Concepts
# RISC-V SoC Design & Tapeout Journey
### Week 1: RTL Design & Simulation Fundamentals

![Status](https://img.shields.io/badge/Day%201-Complete-green)
![Focus](https://img.shields.io/badge/Focus-RTL%20&%20Verification-blue)
![Tools](https://img.shields.io/badge/Tools-Icarus%20&%20GTKWave-lightgrey)

This week marks the transition from environment setup to hands-on RTL design. The focus is on mastering the fundamentals of Verilog HDL, understanding the role of standard cell libraries, and executing a complete simulation and verification workflow using Icarus Verilog and GTKWave.

---

### ## 🧠 Core Concepts: RTL Design & Verification

Before writing code, it's essential to understand the "why" behind the process. This week's theory focused on two pillars of digital design: how to test a design (Testbenches) and the workflow for running those tests (Simulation Flow).

#### **Testbench Architecture**

A testbench is a self-contained Verilog module that acts like a virtual lab bench for your design. Its only job is to verify that your **Design Under Test (DUT)** works correctly. It has three main parts:

1.  **Stimulus Generator:** This block acts like the "hands" of the testbench. It generates all the input signals and clocks needed to exercise the DUT's functionality.
2.  **Design Under Test (DUT):** This is your actual Verilog module (e.g., `good_mux.v`). It's instantiated inside the testbench.
3.  **Stimulus Observer:** This block acts as the "eyes." It watches the output signals from the DUT to ensure they match the expected results. In our case, `GTKWave` serves as our primary observer.



#### **The Icarus Verilog Simulation Flow**

We use a systematic, four-stage process to go from Verilog code to a visual waveform that we can analyze.

1.  **Input:** Provide the `iverilog` compiler with two key files: your design (`design.v`) and its corresponding testbench (`testbench.v`).
2.  **Compilation:** The `iverilog` command compiles your code, checks for syntax errors, and produces a compiled, executable simulation file (typically named `a.out`).
3.  **Execution & VCD Generation:** Running the compiled file (`./a.out`) executes the simulation defined in the testbench. As it runs, it "dumps" all the signal activity into a **Value Change Dump** (`.vcd`) file.
4.  **Analysis:** The `gtkwave` command opens this `.vcd` file, allowing us to visually inspect every signal's behavior over time and debug our design.
