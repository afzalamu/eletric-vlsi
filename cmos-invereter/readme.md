

# CMOS INVERETR SCHEMATIC, LAYOUT AND  ANALYSIS : Electric Binary Software and LTspice Simulation

This README.md file documents the process of creating schematic setups for CMOS INVERETR, along with Tthe layout, using Electric Binary Software. It also covers writing SPICE code for the schematic and layout, followed by simulating Voltage Transfer Characteristics using LTspice.

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
This project demonstrates the process of designing schematic setups for CMOS INVERTER, generating their layouts, writing SPICE code, and simulating  Voltage Transfer Characteristics using LTspice. The key steps involve schematic design, layout generation, SPICE modeling, and DC analysis.

## Prerequisites
- [Electric Binary Software](https://link-to-electric.com) Click here to Install
- [LTspice](https://www.analog.com/en/design-center/design-tools-and-calculators/simulation-tools/lts.html) Click here to Install
- [C5 MODEL FILE](http://cmosedu.com/videos/electric/tutorial2/C5_models.txt) Download C5.txt model file 

## Instructions

### Creating Schematic and Layout
1. Open Electric Binary Software and create a new library `tutorial_3.jelib`.
2. Create New cell `Cell >> New cell >> inv_20_10 >> schematic`.
3. Create New cell `Cell >> New cell >> inv_20_10 >> Layout`.
4. Design schematic setups for CMOS INVERTER using the software's schematic editor `Components >> NMOS(4 terminal) `
    Set the spice model for NMOS and PMOS  `Tools >> Spice Model >> NMOS` `Tools >> Spice Model >> PMOS` and edit its properties `length=2 ans width = 10` and `length=2 ans width = 20` respectively.
    and export the pins as given in schematic setup for CMOS Inverter schematic and save them.
4. Generate layouts for CMOS inverter setup using Electric's layout generation tools.
    select NMOS and PMOS from component, For NMOS Source and Drain are made with `nact` and for Gate Metal to polysilicon contact is required select it and for body terminal select `Pwell` and make their x sizes same as with i.e 10. set the spice model and make the proper connections and export the pins. 
    Similarly, for PMOS Source and Drain are made with `Pact` and one metal to polysilicon contact is required for Gate and for body `Nwell` is required and adjust the sizes and make the proper connections ad export the pins. Refer to the pictures attached.
5. Save the Schematic and layout files.
6. Perform the Design Rule Check (DRC) using `F5`, also do the Network Consistency Check (NCC) and check the wells (ERC) too. 
After all the tests are successfully passed we go to the next step.
We can make an icon for the CMOS Inverter by simply going to `view >> make icon view`
Then icon view gets added to the top right hand side of the cell.This doesn’t look like an inverter so we’ll change it.
We need to change the icon so that it looks like an inverter.

In the schematic view an instance of the icon is placed.
We can open the icon view by double clicking on the name above or
by selecting this view and going to the menu Cell -> Down Hierarchy -> Down Hierarchy (or Ctrl+D)
Let’s select the icon view in the drawing area and press Ctrl+D to get the following.
To go back up in the hierarchy we can use Ctrl+U or Cell -> Up Hierarchy -> Up Hierarchy
Press Ctrl+U now to go back up to the inverter schematic (the only cell using the icon view)
Select this view again and then Ctrl+D to back into the icon view (knowing can use the Explorer to move between cells too)
Next select and delete the box/text leave the pins and next from component menu can select triangle and circle and rotate the output pin and make the symbol of an inverter.
Now using this symbol we can simulate the inverter.
7 . Create New cell `Cell >> New cell >> inv_sim>> schematic`.
in this schematic use the symbol and export the pins .
then we write the spice code .

### Writing SPICE Code
1. To write the spice code `Components >> Misc. >> Spice Code` for both Schematic and Layouts.
2. For CMOS Inverter Schematic and Layout
`vdd vdd 0 DC `
`vin in 0 DC 0`
`.dc vin 0 5 1m`
`.include "path to model file" `

### Performing DC Analysis
1. Now we are ready to simulate and obtain IV characterstics of both PMOS and NMOS
   Go to `Tools >> Spice >> write Spice deck` and Ltspice will automatically get invoked and plot the characterstics.
5. Observe and analyze the simulated VTC for CMOS Inverter setups.

## Screenshots
NMOS SCHEMATIC SETUP 
![NMOS SCHEMATIC SETUP ](https://github.com/afzalamu/eletric-vlsi/blob/main/IV_CHARACTERSTICS_NMOS%26PMOS/images/NMOS_SchematicSetup.png) 
NMOS LAYOUT SETUP
![NMOS LAYOUT SETUP ](https://github.com/afzalamu/eletric-vlsi/blob/main/IV_CHARACTERSTICS_NMOS%26PMOS/images/NMOS_LayoutSetup.png) 
PMOS SCHEMATIC SETUP
![PMOS SCHEMATIC SETUP ](https://github.com/afzalamu/eletric-vlsi/blob/main/IV_CHARACTERSTICS_NMOS%26PMOS/images/PMOS_SchematicSetup.png) 
PMOS LAYOUT SETUP
![PMOS LAYOUT SETUP ](https://github.com/afzalamu/eletric-vlsi/blob/main/IV_CHARACTERSTICS_NMOS%26PMOS/images/PMOS_LayoutSetup.png) 
NMOS IV CHARACTERSTICS
![NMOS IV CHARACTERSTICS](https://github.com/afzalamu/eletric-vlsi/blob/main/IV_CHARACTERSTICS_NMOS%26PMOS/images/NMOS_iD.jpg) 
PMOS IV CHARACTERSTICS
![PMOS IV CHARACTERSTICS](https://github.com/afzalamu/eletric-vlsi/blob/main/IV_CHARACTERSTICS_NMOS%26PMOS/images/PMOS_IS.jpg)

## Conclusion
By following this process, you successfully designed CMOS Inverter using Electric Binary Software, generated their layouts, wrote SPICE code, and simulated  its Voltage Transfer characteristics using LTspice. This project demonstrates the integration between schematic design, layout generation, SPICE modeling, and DC analysis.
