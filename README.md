
# RISC-V 32-bit Sequential Processor

## Overview
This repository contains the design and simulation resources for a 32-bit sequential RISC-V processor -- developed with Vivado -- and a series of design schematics. For a high-level description of the processor development, visit the [RISC-V Single-Cycle Processor](https://kirbyburkejr.com/projects/verilog-risc-v-processor) page on my portfolio site.

## Features

### Sequential Processing

This processor's sequential processing design passes a discrete instruction through each of the following five RISC stages to calculate and return a 32-bit result before processing subsequent instructions.
- Instruction Fetch (IF)
- Instruction Decode (ID)
- Execution (EX)
- Memory Access (MEM)
- Write Back (WB)

### Supported RISC-V Instructions

This processor contains the following subset of RISC-V instructions. All arithmetic operations use signed values, and logical operations use bitwise evaluations.

**R-Type**
- add
- and
- nor+
- or
- seq+ (set if equal)
- slt (set less than)
- sub (subtract)

+ The nor and seq instructions are custom. They're not included within the standard RISC-V ISA, but are compatible with it.

**I-Type**
- addi
- andi
- lw (load word)
- ori
- slti (set less than)

**S-Type**

- sw (store word)

## Directories

**docs/**
- datapath-diagram.png
- processor-diagram.png
- instruction-specifications.png

**src/design/**

Contains all Verilog module designs.

**src/testbench/**

Contains the Processor test bench design.

**sim/**
- example-tcl-output.txt
- tb_Processor_behav.png
- tb_Processor_behav.wcfg

## Instructions

### Cloning the Repository
```bash
git clone https://github.com/kirbyburkejr/verilog-risc-v-processor.git
cd verilog-risc-v-processor
```

### Running the Simulation

The simulation includes a sequence of tests for 20 instructions.

1. Open Vivado and create a new project.
2. Add the files in the `src/design/` and `src/testbench/` directories.
3. Run the simulation using the `tb_Processor.v` test bench file.

Simulation output includes a waveform diagram and Tcl output, including conditional alerts for specific instruction failures and a summary with the count of successful instructions.

## Documentation

Detailed block diagrams, including internal bus signals and port mapping:
- Processor (i.e., the parent container)
- Datapath, including stages and submodules

Tables with bit allocation for each instruction type.

### Tools Used

- [Vivado v2023.2 (64-bit)](https://www.xilinx.com/support/download/index.html/content/xilinx/en/downloadNav/vivado-design-tools/2023-2.html) for Verilog module design and waveform generation.
- [Lucidchart](https://www.lucidchart.com/pages/) for module block designs.

## License
This project is licensed under the [MIT License](LICENSE).

## Contributing
Feel free to submit issues or pull requests to improve this project.
