# Changelog

All notable changes to this project will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/), and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [1.0.0] - 2024-12-28

### Added

#### General
- **LICENSE**
- **README.md**

#### Design Modules (src/design/)
- **ALU.v**: Arithmetic Logic Unit
- **ALUController.v**: ALU Controller
- **Controller.v**: Controller (for all non-ALU submodules)
- **DataMem.v**: Data Memory
- **Datapath.v**: Datapath container
- **FlipFlop.v**: Flip Flop
- **HalfAdder.v**: Half Adder
- **ImmGen.v**: Immediate Generator
- **InstrMem.v**: Instruction Memory
- **Mux2_1.v**: 2-to-1 Multiplexer
- **Processor.v**: Processor (i.e., parent container)
- **RegFile.v**: Register File

#### Test Bench (src/testbench/)
- **tb_Processor.v**: Processor Test Bench

#### Documentation (doc/)
- **datapath-diagram.png**: Block diagram for Datapath stages and submodules
- **processor-diagram.png**: Block diagram for Processor parent container
- **instruction-specifications.png**: Tables for instruction formatting

#### Simulation Output (sim/)
- **tb_Processor_behav.wcfg**: Waveform output of successful simulation
- **tb_Processor_behav.png**: Image of waveform output
- **tcl-output-example.txt**: Examples of Tcl output messages
