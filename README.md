# PWM Generator with Variable Duty Cycle

## Overview
This VHDL project implements a PWM generator with adjustable duty cycle control. The duty cycle can be modified in steps of 10% using input buttons. A testbench is provided for simulation.

## Features
- Adjustable duty cycle (increment or decrement by 10%).
- Debouncing mechanism for button inputs.
- Testbench for functional verification.
- Compatible with Xilinx Vivado and other VHDL simulators.


## Tools Required
- Xilinx Vivado (preferred) or other VHDL simulators like GHDL or ModelSim.


## How to Use
1. **Open the VHDL Files in Your Simulation Tool**  
   - Load the `.vhd` files (`PWM_Generator.vhd` and `tb_PWM_Generator.vhd`) into your VHDL simulation tool (e.g., Xilinx Vivado, GHDL, or ModelSim).  

2. **Simulate `tb_PWM_Generator.vhd` to Verify Functionality**  
   - Run the testbench to observe the PWM waveform and ensure that the duty cycle adjustment behaves as expected.  

3. **Deploy to FPGA (Optional)**  
   - Synthesize and implement the design on an FPGA board to test the real-world functionality.  

---

## Design Details
- **Input Clock**: 100 MHz  
- **PWM Output Frequency**: 10 MHz  
- **Duty Cycle Adjustment**:  
  - Controlled using `DUTY_INCREASE` and `DUTY_DECREASE` buttons, which modify the duty cycle in steps of 10%.  
- **Debouncing**:  
  - Implemented with D-Flip-Flops to eliminate noise from button presses.  

---

## Notes
- Ensure the clock input frequency matches 100 MHz for proper operation.  
- Use appropriate simulation and debugging tools to analyze the PWM waveform and duty cycle transitions.  
- For FPGA deployment, map input signals (`clk`, `DUTY_INCREASE`, and `DUTY_DECREASE`) and output signal (`PWM_OUT`) to the corresponding pins of your FPGA board.  
