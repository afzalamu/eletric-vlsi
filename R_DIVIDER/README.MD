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
2. Design the resistor divider circuit schematic using the software's schematic editor.
3. Save the schematic file with a relevant name (e.g., `resistor_divider.sch`).
4. Generate the layout for the designed circuit using Electric's layout generation tools.
5. Save the layout file with a relevant name (e.g., `resistor_divider_layout.layout`).

### Writing SPICE Code
1. Open the schematic  Electric and annotate the components with reference designators.
2. Export the annotated schematic to a netlist format compatible with LTspice (e.g., `.cir` or `.net`).

### Performing Transient Analysis
1. Open LTspice and create a new schematic.
2. Import the exported netlist into the LTspice schematic.
3. Set up the transient analysis parameters, such as simulation time and time step.
4. Run the transient analysis simulation.
5. Analyze the simulated waveform to observe the behavior of the resistor divider circuit.

## Screenshots
Include relevant screenshots of the created schematic, layout, SPICE code, and LTspice simulation results. Place these images in a separate folder within the repository.

## Conclusion
By following this process, you successfully designed a resistor divider circuit using Electric Binary Software, generated its layout, wrote SPICE code, and simulated its waveform behavior using LTspice. This project showcases the seamless integration between schematic design, layout generation, and circuit simulation.
