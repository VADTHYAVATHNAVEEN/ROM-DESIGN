**ROM Design in Verilog**
**Overview**
This project implements a Read-Only Memory (ROM) using Verilog. The ROM module stores pre-defined data and supports synchronous data access based on an address input. ROM is widely used in applications where constant or lookup table data is required, such as microcontroller firmware, lookup tables, and fixed coefficients.

**Features**
Synchronous Read Operation: Data is accessed on the positive clock edge.
Enable Control: Data output is valid only when the enable signal is active.
Fixed Data Content: Initialized with 16 predefined 4-bit data values.
Efficient Memory Mapping: Uses a 4-bit address space to access 16 memory locations.
**Design Details**
ROM Module
The ROM module has the following interface:

Clock Input (clk): Synchronous read operation.
Enable Input (en): Controls the data output.
Address Input (addr): 4-bit address to access one of the 16 locations.
Data Output (data): 4-bit data output corresponding to the given address
****Block Diagram ****
          +-------------------+
          |       ROM         |
          |                   |
    clk --|                   |
     en --|                   |
  addr --|                   |--> data
          +-------------------+

    
**The testbench verifies:**

Correct Read Operations: Data is correctly read based on the address.
Enable Signal Functionality: Output is set to 4'bxxxx when disabled.
Data Integrity: Verifies that pre-defined ROM contents are correctly loaded.
**Applications**
Microcontroller Firmware Storage
Fixed Lookup Tables
Memory-Mapped Constants
Coefficient Storage for DSP
**Contributions**
Contributions are welcome! Feel free to fork the project and submit a pull request. For significant changes, please open an issue first to discuss the proposed improvements.

**Contact**
For any questions or suggestions, please open an issue on GitHub or reach out via email.
