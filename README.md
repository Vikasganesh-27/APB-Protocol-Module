# APB-Protocol-Module

This repository contains the APB (Advanced Peripheral Bus) verification environment, including an APB slave module and a SystemVerilog testbench implementing a UVM-like structure.

## APB Slave Module
The APB slave module implements a simple APB interface with standard signals such as `paddr`, `pwdata`, `prdata`, `psel`, `penable`, `pwrite`, `pready`, and `pslverr`.

### Features:
- Supports read and write transactions.
- Implements a ready signal to indicate transaction completion.
- Handles errors through the `pslverr` signal.


## SystemVerilog Testbench
The testbench is written in SystemVerilog and includes a transaction-based verification environment with:
- **Transaction Class**: Defines the transaction data structure.
- **Generator Class**: Randomly generates transactions.
- **Driver Class**: Drives transactions to the APB interface.
- **Monitor Class**: Passively observes the APB signals.
- **Scoreboard Class**: Compares expected and actual data.
- **Environment Class**: Instantiates and connects all components.
- **Testbench Module**: Implements clock generation, DUT instantiation, and test execution.


## How to Run the Simulation
1. Compile the testbench and APB slave module using a SystemVerilog-compatible simulator (e.g., VCS, Questa, ModelSim).
2. Run the simulation and observe the output logs.
3. Analyze the generated waveforms using a waveform viewer (e.g., GTKWave, DVE).

## License
This project is released under the MIT License.



