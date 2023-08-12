# Electric Binary Software and LTspice Simulation: Resistor Divider Circuit

This README.md file documents the process of creating a resistor divider circuit schematic and layout using Electric Binary Software, followed by simulating its waveform using LTspice. The process includes creating the schematic, generating the layout, writing SPICE code, and performing a transient analysis.

## Table of Contents
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Instructions](#instructions)
  - [Creating Schematic and Layout](#creating-schematic-and-layout)
  - [Writing SPICE Code](#writing-spice-code)
  - [Performing Transient Analysis](#performing-transient-analysis)
- [Screenshots](#screenshots)
- [Conclusion](#conclusion)

## Overview
This project demonstrates the process of designing a resistor divider circuit using Electric Binary Software and then simulating its behavior using LTspice. The key steps involve creating the circuit schematic, generating its layout, writing SPICE code, and finally analyzing the transient waveform response.

## Prerequisites
- [Electric Binary Software](https://link-to-electric.com) Click here to Install
- [LTspice](https://www.analog.com/en/design-center/design-tools-and-calculators/simulation-tools/lts.html) Click here to Install

## Instructions

### Creating Schematic and Layout
1. Open Electric Binary Software and create a new project. 
    `Explore >> Library Name >> Tutorial_1.jelib`
2. Ceate New Cell `Cell >> New Cell >> R_divider >> Schematic`
3. Design the resistor divider circuit schematic using the software's schematic editor using N well Resistor from Components option.
4. Edit its properties `Ctrl + I` in my case I have taken `LENTGTH=187.5 UNITS AND WIDTH=15 UNITS` AND Scale was 300 nanometer.
5. Now again create new cell , give its name same `R_divider` and type should be `Layout`.
6. Generate the layout for the designed circuit using Electric's layout generation tools using n well resitor from components option and make its properties same as schematic.
7. Now, we can perform Design Rule Check (DRC), Also do the Network Consistency Check (NCC) And check wells too. If there is eny error view it and debug it.

### Writing SPICE Code
1. Write spice code in both schematic and Layout for simulation. Spice code can be written by going to components >> Misc.
2. I have written it for the above R_divier 
`vin vin 0 DC 1 
.tran 0 1` 

### Performing Transient Analysis
1. We can invoke LTspice from Electric only for eg. let us simulate R_divider schematic . Go to `Tools >> Spice/CDL >> write spice 
2. Now , LT Spice is invoked and plot the Vout and Vin using add plots and its waveform will be visisbl.
3. Analyze the simulated waveform to observe the behavior of the resistor divider circuit.

## Screenshots
![Schematic of R_divider](./electric-vlsi/R_DIVIDER/images/schematic.jpg) 

![Laout of R_divider](./electric-vlsi/R_DIVIDER/images/layout.jpg) 

![Transient Analysis](./electric-vlsi/R_DIVIDER/images/waveform.jpg) 

## Conclusion
By following this process, you successfully designed a resistor divider circuit using Electric Binary Software, generated its layout, wrote SPICE code, and simulated its waveform behavior using LTspice. This project showcases the seamless integration between schematic design, layout generation, and circuit simulation.
