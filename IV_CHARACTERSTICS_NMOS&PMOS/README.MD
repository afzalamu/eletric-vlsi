
# NMOS and PMOS IV Characteristics : Electric Binary Software and LTspice Simulation

This README.md file documents the process of creating schematic setups for plotting NMOS and PMOS IV characteristics, along with their layouts, using Electric Binary Software. It also covers writing SPICE code for the schematic and layout, followed by simulating IV characteristics using LTspice.

## Table of Contents
- [Overview](#overview)
- [Prerequisites](#prerequisites)
- [Instructions](#instructions)
  - [Creating Schematic and Layout](#creating-schematic-and-layout)
  - [Writing SPICE Code](#writing-spice-code)
  - [Performing DC Analysis](#performing-dc-analysis)
- [Screenshots](#screenshots)
- [Conclusion](#conclusion)

## Overview
This project demonstrates the process of designing schematic setups for NMOS and PMOS IV characteristics, generating their layouts, writing SPICE code, and simulating IV characteristics using LTspice. The key steps involve schematic design, layout generation, SPICE modeling, and DC analysis.

## Prerequisites
- [Electric Binary Software](https://link-to-electric.com) Click here to Install
- [LTspice](https://www.analog.com/en/design-center/design-tools-and-calculators/simulation-tools/lts.html) Click here to Install
- [C5 MODEL FILE](http://cmosedu.com/videos/electric/tutorial2/C5_models.txt) Download C5.txt model file 

## Instructions

### Creating Schematic and Layout
1. Open Electric Binary Software and create a new library `tutorial_2.jelib`.
2. Create New cell `Cell >> New cell >> NMOS_IV >> schematic`. Similarly, a new cell as `PMOS_IV`.
3. Create New cell `Cell >> New cell >> NMOS_IV >> Layout`. Similarly, a new cell as `PMOS_IV`.
4. Design schematic setups for both NMOS and PMOS IV characteristics using the software's schematic editor `Components >> NMOS(4 terminal) `
    Set its spice model for NMOS and PMOS  `Tools >> Spice Model >> NMOS` `Tools >> Spice Model >> PMOS` and edit its properties `length=2 ans width = 10`
    and export the pins as given in schematic setup for both NMOS and PMOS schematics and save them.
4. Generate layouts for both NMOS and PMOS setups using Electric's layout generation tools.
    select NMOS and PMOS from component, For NMOS Source and Drain are made with `nact` and for Gate Metal to polysilicon contact is required select it        and for body terminal select `Pwell` and make their x sizes same as with i.e 10. set the spice model and make the proper connections and export the        pins. 
    Similarly, for PMOS Source and Drain are made with `Pact` and one metal to polysilicon contact is required for Gate and for body `Nwell` is required       and adjust the sizes and make the proper connections ad export the pins. 
5. Save the Schematic and layout files.

### Writing SPICE Code
1. To write the spice code `Comonents >> Misc. >> Spice Code` for both Schematic and Layouts.
2. For NMOS Schematics and Layouts 
   `VS S 0 DC 0 
    VW W 0 DC O 
    VG G 0 DC 0 
    VD D 0 DC 0 
    .dc VD 0 5 1 VG 0 5 1 
    .INCLUDE "Path to c5 model file" `
2. For PMOS Schematics and Layouts 
   `VS S 0 DC 0 
    VW W 0 DC O 
    VG G 0 DC 0 
    VD D 0 DC 0 
    .dc VD 0 -5 -1 VG 0 -5 -1 
    .INCLUDE "Path to c5 model file" `

### Performing DC Analysis
1. Now we are readt to simulate and obtain IV characterstics of both PMOS and NMOS
   Go to `Tools >> Spice >> write Spice deck` and Ltspice will automatically get invoked and plot the characterstics.
5. Observe and analyze the simulated IV characteristics for both NMOS and PMOS setups.

## Screenshots

## Conclusion
By following this process, you successfully designed schematic setups for NMOS and PMOS IV characteristics using Electric Binary Software, generated their layouts, wrote SPICE code, and simulated IV characteristics using LTspice. This project demonstrates the integration between schematic design, layout generation, SPICE modeling, and DC analysis.
