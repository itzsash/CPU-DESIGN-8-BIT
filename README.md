# 8-Bit CPU Design in Logisim

This repository contains the design of a simple 8-bit CPU created using Logisim. The CPU is designed to perform basic arithmetic operations, specifically adding two numbers and storing the result. This project demonstrates core principles of CPU design, including instruction fetch, addition, result storage, and output display on a 7-segment display.

![connections-between-the-processor-and-the-mm](https://github.com/user-attachments/assets/664d3a83-108a-4f37-baba-f4a18afc85f9)

## Overview

The 8-bit CPU is a minimalistic design that focuses on performing addition operations, storing the results in a register, and displaying the output. The CPU executes the following steps:
1. **Fetch Instruction**: Retrieve the operation instruction from memory.
2. **Add Operation**: Perform addition of two numbers.
3. **Store Result**: Save the result in the output register.
4. **Display Result**: Output the result on a 7-segment display using a decimal decoder.

## Design Components

### 1. Control Unit
   - The control unit automates the process, handling the sequence of operations without manual intervention.
   - It manages the instruction fetch, addition operation, and result storage in the output register.

### 2. Program Counter (PC)
   - Keeps track of the current instruction address in memory, enabling sequential instruction execution.

### 3. Instruction Register (IR)
   - Stores the fetched instruction for processing by the control unit.

### 4. Register A and Register B
   - These registers hold the operands for the addition operation.
   - Register A and Register B are fed into the Arithmetic Logic Unit (ALU) for computation.


### 5. Arithmetic Logic Unit (ALU)
   - Responsible for performing the addition operation.
   - Outputs the sum of the values in Register A and Register B.


### 6. Output Register (OP REG)
   - Stores the result of the addition operation for further processing or display.
   - The result is accessible to the decimal decoder for visualization on the 7-segment display.

### 7. Memory Address Register (MAR) and Memory Buffer Register (MBR)
   - MAR holds the address of data or instructions being accessed from memory.
   - MBR temporarily holds data read from or written to memory.

### 8. Decimal Decoder and 7-Segment Display
   - The decimal decoder converts binary output from the OP REG to a format readable by the 7-segment display.
   - This allows for a visual representation of the result on a digital display.

## Design Flow

1. **Fetch**: The control unit triggers the program counter to load the instruction into the instruction register.
2. **Add**: The CPU reads values from Register A and Register B and performs addition via the ALU.
3. **Store**: The result of the addition is stored in the OP REG.
4. **Display**: The value in the OP REG is sent through a decimal decoder and displayed on the 7-segment display.

![main_cpu](https://github.com/user-attachments/assets/d2972ff4-00bf-449c-9383-3465ab3eee68)

## Key Specifications

- **Data Width**: 8-bit
- **Operation**: Addition
- **Control Unit**: Automated instruction fetch, addition, and result storage
- **Output**: Result is displayed on a 7-segment display using a decimal decoder
- **Pipeline**: No pipelining; the CPU executes instructions sequentially

## Design Choices

- **Automated Control**: The inclusion of a control unit simplifies the operation by managing the instruction sequence without manual input.
- **Decimal Decoder for Display**: Using a decimal decoder allows easy visualization of the CPU’s output on a 7-segment display.

## Future Enhancements

- Expand the CPU to support additional operations (e.g., subtraction, multiplication, etc.)
- Implement pipelining for improved efficiency and performance.
- Introduce more complex control logic for advanced instruction handling.

## Getting Started

1. Open the CPU.circ file in Logisim.
2. Enable Simulation and set the tick frequency to 1Khz
3. Observe the Simulation to see the fetch, add, store, and display sequence.
4. The result of the addition operation will appear on the 7-segment display.

![Screenshot 2024-11-01 154529](https://github.com/user-attachments/assets/98cc3399-ae6a-4303-a633-060b1b4647e8)


## Contributing

Feel free to open issues, suggest improvements, or contribute to the design. Your feedback and contributions are welcome!
