FPGA-Based Image Blur Filter using Parallel Matrix Computation
 Overview
This project implements an FPGA-based Image Blur Filter using Parallel Matrix Computation in Verilog HDL.  
The design performs real-time image blurring using a 3×3 averaging convolution filter architecture.

The system is developed using Xilinx Vivado and focuses on improving processing speed and efficiency through parallel hardware computation.

Objectives
- Design an FPGA-based image blur filter
- Implement parallel matrix computation
- Reduce execution time compared to sequential processing
- Improve hardware efficiency
- Simulate and verify the design using Verilog HDL



Problem Statement
Image processing operations such as blurring require large matrix computations.  
Traditional software-based processing is slower and consumes more power for real-time applications.

This project proposes a hardware-based FPGA solution that performs parallel convolution operations to achieve faster image processing.

---

System Architecture

The system consists of:

- Input Image Memory
- Address Generator
- Line Buffers
- 3×3 Sliding Window
- Parallel Adder Tree
- Output Register
- Output Image Memory

The blur filter uses a 3×3 averaging kernel.

Blur Formula:

O(r,c) = (P1 + P2 + P3 + P4 + P5 + P6 + P7 + P8 + P9) / 9


Technologies Used
- Verilog HDL
- Xilinx Vivado
- FPGA Design
- Digital System Design
- Parallel Processing

 Leaf Cell Modules
 1. D Flip-Flop
Used for:
- Data storage
- Synchronization
- Shift registers

Formula:
Q(t+1) = D

 2. Shift Register
Used to:
- Move pixel data
- Form sliding window architecture

Formula:
Q(t+1) = Qi-1(t)

3. 8-Bit Full Adder
Used in:
- Parallel adder tree
- Pixel summation

Formula:
Sum = A ^ B ^ Cin

Carry = A·B + B·Cin + A·Cin

 Output Register
Used to:
- Store final blurred pixel
- Remove glitches
- Synchronize output

 Simulation & Verification

All modules were verified using dedicated Verilog testbenches.

Verified Components:
- D Flip-Flop
- Shift Register
- 8-Bit Adder
- Output Register

Verification Methods:
- Functional Simulation
- RTL Schematic Analysis
- Waveform Verification

 
