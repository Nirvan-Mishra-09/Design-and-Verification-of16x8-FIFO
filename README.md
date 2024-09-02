# Design and Verification of 16x8-FIFO

This repository contains the design and verification of a 16x8 FIFO (First-In-First-Out) memory buffer implemented using SystemVerilog. The project includes both the FIFO design code and a comprehensive testbench to ensure the correctness of the FIFO operation.

## Table of Contents
- [Overview](#overview)
- [Design Details](#design-details)
- [Testbench](#testbench)
- [Waveform](#Waveform)


## Overview
The 16x8 FIFO module is designed to manage data storage and retrieval in a synchronized manner, ensuring that data is read in the order it was written. This project also includes a verification environment to validate the FIFO design, checking its functionality under various scenarios. EDA Playground link https://www.edaplayground.com/x/ALjD

## Design Details
### FIFO Module
- **Width:** 8 bits
- **Depth:** 16 entries
- **Features:**
  - **Empty and Full Flags:** Indicators for FIFO status.
  - **Write and Read Pointers:** Used to track the next write and read positions.
  - **Count Register:** Tracks the number of entries in the FIFO.

### Interface Signals
- `clk`: Clock signal
- `rst`: Reset signal (active high)
- `wr`: Write enable
- `rd`: Read enable
- `din`: 8-bit input data
- `dout`: 8-bit output data
- `empty`: Empty flag (active high)
- `full`: Full flag (active high)

## Testbench
The testbench is written using SystemVerilog and includes:
- **Interface:** Defines the connection between the FIFO and the testbench.
- **Transaction Class:** Represents read/write operations.
- **Generator:** Randomly generates transactions.
- **Driver:** Drives inputs to the FIFO based on generated transactions.
- **Monitor:** Observes and records FIFO operations.
- **Scoreboard:** Checks the correctness of the FIFO operation by comparing expected and actual outputs.
- **Environment:** Integrates all the components of the verification environment.


## Waveform
![image](https://github.com/user-attachments/assets/1e3bda6f-484f-4a34-aca0-d218336b9d00)

