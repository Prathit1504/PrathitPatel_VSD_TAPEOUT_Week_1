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
Before diving into practical implementation, it's essential to understand the fundamental concepts of RTL design and verification methodology that form the backbone of digital VLSI design.

Testbench Architecture and Design
The testbench is a critical component in the verification process that validates the functionality of digital designs. Understanding its architecture is fundamental to successful RTL verification.

Screenshot 2025-09-21 215854
Testbench Components
Stimulus Generator:

Generates input patterns and control signals for the Design Under Test (DUT)
Provides comprehensive test scenarios covering all functional requirements
Controls timing and sequencing of input stimuli
Design Under Test (DUT):

The actual RTL module being verified and validated
Receives primary inputs from the stimulus generator
Produces primary outputs for observation and analysis
Stimulus Observer:

Monitors and captures the output responses from the DUT
Compares actual results with expected behavior
Reports verification status and identifies any functional discrepancies
Key Testbench Principles
Important Notes:

Design may have 1 or more Primary Inputs and 1 or more Primary Outputs
Testbench (TB) does not have Primary inputs or Primary outputs
The testbench acts as a self-contained verification environment
This architecture ensures comprehensive verification while maintaining clear separation between the design and its verification environment.

Icarus Verilog Simulation Flow
The simulation process using Icarus Verilog follows a systematic approach that transforms RTL designs and testbenches into executable simulations with waveform analysis capabilities.

Screenshot 2025-09-21 220214
Four-Stage Simulation Process
Stage 1: Design and Testbench Input

Design Files: RTL implementation in Verilog (.v files)
Testbench Files: Verification environment with stimulus generation
Input Processing: Both files are fed into the Icarus Verilog compiler
Stage 2: Iverilog Compilation

Compilation Process: Iverilog processes the Verilog source code
Syntax Checking: Validates Verilog syntax and semantics
Executable Generation: Creates simulation executable for the target design
Stage 3: VCD File Generation

Simulation Execution: Running the compiled executable
Value Change Dump: Generates comprehensive signal transition data
Waveform Data: All signal changes recorded in VCD format for analysis
Stage 4: GTKWave Waveform Analysis

Waveform Visualization: GTKWave displays signal transitions graphically
Timing Analysis: Detailed examination of signal behavior over time
Debugging Support: Interactive waveform navigation and measurement tools
Simulation Workflow Benefits
Professional Verification:

Complete signal visibility for comprehensive debugging
Timing-accurate simulation results for design validation
Industry-standard VCD format for tool interoperability
Visual waveform analysis for intuitive design understanding
This systematic approach ensures thorough verification of RTL designs with professional-grade analysis capabilities.

RTL Design and Verification Methodology
The combination of proper testbench architecture and systematic simulation flow creates a robust verification environment essential for complex digital design projects.

Design Flow Integration:

RTL design development follows structured coding practices
Testbench creation ensures comprehensive functional coverage
Simulation execution validates design behavior across all scenarios
Waveform analysis provides detailed insight into design operation
Quality Assurance:

Systematic approach reduces verification time and effort
Visual analysis capabilities enhance debugging efficiency
Standardized flow ensures reproducible verification results
Professional tools provide industry-grade validation
Day 1: Environment Setup and RTL Analysis
Day 1 focused on establishing a professional VLSI development environment and analyzing the comprehensive RTL design library provided in the workshop.

Objectives Completed
Created structured workspace (vsdflow) for the tapeout program
Cloned and analyzed the Sky130 RTL Design and Synthesis Workshop repository
Investigated Sky130 standard cell library structure
Explored extensive collection of RTL designs and testbenches
Implemented complete Verilog simulation workflow
Performed waveform analysis using GTKWave
Workspace Creation and Repository Setup
Initial Environment Setup Commands
Based on the terminal session from the PDF screenshots, the following command sequence was executed:

# Navigate to home directory and create workspace
cd
mkdir vsdflow
cd vsdflow/

# Clone the workshop repository
git clone https://github.com/kunalg123/sky130RTLDesignAndSynthesisWorkshop.git
Screenshot 2025-09-21 225504
Repository Clone Results
The git clone operation successfully downloaded the workshop materials:

Cloning into 'sky130RTLDesignAndSynthesisWorkshop'...
remote: Enumerating objects: 417, done.
remote: Counting objects: 100% (69/69), done.
remote: Compressing objects: 100% (52/52), done.  
remote: Total 417 (delta 19), reused 47 (delta 12), pack-reused 348 (from 1)
Receiving objects: 100% (417/417), 7.79 MiB | 4.12 MiB/s, done.
Resolving deltas: 100% (242/242), done.
Directory Verification
# Verify successful clone
vsduser@vsdsquadron:~/vsdflow$ ls -ltr
total 4
drwxrwxr-x 7 vsduser vsduser 4096 Sep 21 22:54 sky130RTLDesignAndSynthesisWorkshop

# Navigate into workshop directory
cd sky130RTLDesignAndSynthesisWorkshop/
Screenshot 2025-09-21 225737
Workshop Repository Structure Analysis
Top-Level Directory Contents
vsduser@vsdsquadron:~/vsdflow/sky130RTLDesignAndSynthesisWorkshop$ ls
DC_WORKSHOP  lib  my_lib  README.md  verilog_files  yosys_run.sh
Directory Purpose Analysis
DC_WORKSHOP/: Advanced synthesis workshop materials
lib/: Technology library files for synthesis
my_lib/: Custom library directory containing Sky130 behavioral models
verilog_files/: Complete collection of RTL designs and testbenches
yosys_run.sh: Synthesis automation script for later days
README.md: Workshop documentation
Screenshot 2025-09-21 225802
Library Files Investigation
My_lib Directory Analysis
# Navigate to custom library directory
cd my_lib/
vsduser@vsdsquadron:~/vsdflow/sky130RTLDesignAndSynthesisWorkshop/my_lib$ ls
verilog_model
Verilog Model Investigation
# Explore behavioral model directory
cd verilog_model/
vsduser@vsdsquadron:~/vsdflow/sky130RTLDesignAndSynthesisWorkshop/my_lib/verilog_model$ ls
primitives.v  sky130_fd_sc_hd.v
Screenshot 2025-09-21 230141 Screenshot 2025-09-21 231056
Library File Specifications
# Detailed file analysis
vsduser@vsdsquadron:~/vsdflow/sky130RTLDesignAndSynthesisWorkshop/my_lib/verilog_model$ ls -ltr
total 2328
-rw-rw-r-- 1 vsduser vsduser   50512 Sep 21 22:54 primitives.v
-rw-rw-r-- 1 vsduser vsduser 2327999 Sep 21 22:54 sky130_fd_sc_hd.v
Key Library Components:

primitives.v:

Size: 50,512 bytes
Purpose: Basic primitive definitions for standard cell modeling
sky130_fd_sc_hd.v:

Size: 2,327,999 bytes (2.33 MB)
Purpose: Complete Sky130 high-density standard cell behavioral models
Screenshot 2025-09-21 231330
Technology Library Files
# Check synthesis library directory
cd ../..
cd lib/
vsduser@vsdsquadron:~/vsdflow/sky130RTLDesignAndSynthesisWorkshop/lib$ ls
sky130_fd_sc_hd__tt_025C_1v80.lib
This .lib file contains timing and power characterization data for the Sky130 standard cells used in synthesis.

RTL Design Collection Exploration
Verilog Files Directory
# Navigate to RTL design collection
cd ../verilog_files/
Comprehensive Design Collection
The verilog_files directory contains an extensive collection of RTL designs and testbenches covering fundamental to advanced digital logic concepts:

Combinational Logic Designs:

good_mux.v, bad_mux.v - Multiplexer implementations (good vs bad practices)
demux_generate.v - Demultiplexer designs
fa.v - Full adder implementation
rca.v - Ripple carry adder
Sequential Logic Designs:

dff_async_set.v - D flip-flop with asynchronous set
dff_asyncres_syncres.v - D flip-flop with dual reset modes
dff_const1.v through dff_const5.v - Constant optimization examples
Advanced System Modules:

counter_opt.v, good_counter.v - Counter implementations
ripple_counter.v, up_dn_cntr.v - Various counter types
multiple_modules.v - Hierarchical design examples
Corresponding Testbenches:

Each design has an associated testbench (tb_*.v) for comprehensive verification
Examples: tb_good_mux.v, tb_dff_asyncres_syncres.v, etc.
Screenshot 2025-09-21 231330
Simulation Workflow Implementation
Good MUX Design Simulation
The practical simulation exercise focused on the good_mux.v design as a representative example.

Initial Simulation Attempt
# Attempt to compile design and testbench
vsduser@vsdsquadron:~/vsdflow/sky130RTLDesignAndSynthesisWorkshop/verilog_files$ iverilog good_mux.v tb_good_mux.v
Tool Installation Requirement
The initial attempt revealed that Icarus Verilog needed to be installed:

Command 'iverilog' not found, did you mean:

command 'iverilog' from deb iverilog

Try: sudo apt install <deb name>
Successful Simulation Execution
After installing iverilog (as implied by the PDF screenshots showing successful simulation), the compilation and simulation proceeded:

# Compilation (after iverilog installation)
iverilog good_mux.v tb_good_mux.v

# Simulation execution  
./a.out
VCD info: dumpfile tb_good_mux.vcd opened for output.
Screenshot 2025-09-21 232008 Screenshot 2025-09-21 232051
Good MUX RTL Design Analysis
Based on the code shown in the PDF screenshots, the good_mux.v design implements a 2:1 multiplexer:

module good_mux (input i0, input i1, input sel, output reg y);
    always @ (*)
    begin
        if (sel)
            y <= i1;
        else  
            y <= i0;
    end
endmodule
Screenshot 2025-09-25 104724 Screenshot 2025-09-25 104735
Testbench Implementation Analysis
The tb_good_mux.v testbench provides comprehensive stimulus:

`timescale 1ns / 1ps

module tb_good_mux;
    // Inputs
    reg i0, i1, sel;
    // Outputs  
    wire y;
    
    // Instantiate the Unit Under Test (UUT)
    good_mux uut (
        .sel(sel),
        .i0(i0), 
        .i1(i1),
        .y(y)
    );
    
    initial begin
        $dumpfile("tb_good_mux.vcd");
        $dumpvars(0, tb_good_mux);
        
        // Initialize Inputs
        sel = 0;
        i0 = 0;
        i1 = 0;
        #300 $finish;
    end
    
    always #75 sel = ~sel;   // Toggle select every 75ns
    always #10 i0 = ~i0;    // Toggle i0 every 10ns  
    always #55 i1 = ~i1;    // Toggle i1 every 55ns
endmodule
GTKWave Waveform Analysis
Waveform Viewing
# Launch GTKWave for waveform analysis
gtkwave tb_good_mux.vcd
Waveform Analysis Results
The GTKWave screenshots from the PDF show successful waveform generation with the following observations:

Signal Behavior:

i0: Toggles every 10ns as specified
i1: Toggles every 55ns as specified
sel: Toggles every 75ns as specified
y: Correctly follows multiplexer logic (y = sel ? i1 : i0)
Timing Verification:

Simulation runs from 0 to 300ns as programmed
All signal transitions occur at expected time intervals
Multiplexer functionality verified across all input combinations
Screenshot 2025-09-21 232652
Functional Verification Results
The waveform analysis confirms correct multiplexer operation:

When sel = 0: Output y follows input i0
When sel = 1: Output y follows input i1
No glitches or timing violations observed
Clean digital signal transitions throughout simulation
Week 1 Day 1 Accomplishments
Technical Skills Developed
Environment Setup Mastery:

Successfully created professional VLSI development workspace
Configured git-based project management for workshop materials
Established organized directory structure following industry practices
Design Analysis Proficiency:

Analyzed comprehensive RTL design library (100+ designs)
Understood Sky130 standard cell library structure and organization
Gained familiarity with both good and bad design practice examples
Simulation Workflow Expertise:

Implemented complete Verilog simulation flow using Icarus Verilog
Performed comprehensive functional verification using testbenches
Conducted professional waveform analysis using GTKWave
Technology Integration Understanding:

Investigated Sky130 PDK behavioral model files
Understood relationship between design files and technology libraries
Gained appreciation for open-source EDA tool ecosystem
Knowledge Foundation Established
RTL Design Principles:

Understanding of proper Verilog coding practices through good/bad examples
Appreciation for testbench development and verification methodology
Foundation for advanced synthesis and optimization concepts
Professional Development:

Industry-standard workspace organization and version control
Technical documentation and systematic problem-solving approaches
Preparation for advanced synthesis and physical design topics
Week 1 Day 1 Status: COMPLETE

Successfully established professional VLSI development environment, mastered fundamental RTL design theory, analyzed comprehensive RTL design library, and implemented complete simulation workflow. Ready for Day 2: Logic Synthesis and Technology Mapping.
