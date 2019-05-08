# DE10-ADC
This repository has the HDL and a guide for configuring the on-board ADC on DE-series FPGAs for 2MHz sampling rate.

This guide is using Quartus Prime 16.0 and Qsys IP tool, but should also be supported for Platform Designer (formerly Qsys) and a newer version of Quartus.

** FPGA Configuration Information **

The board used for this configuration is the DE10-Lite (10M50DAF484C7G) which has two on-board FPGAs but only ADC0 is used. See the user manual and configuration guide for pin assignments, and ADC configurations if you are using a different board. 

### Created By New Mexico State University ECE Student

(Updated May 8, 2019)  

 Derrick Rivera


## ADC IP Configuration

This section describes the process of configuring the ADC core control module and necessary PLL.



### Interfaceing with the ADC

The ADC interface is I2C. The source Verilog is the top-level entitiy of the Quartus project (see adc_2M.v).



## Deployment

** Uploading HDL to the FPGA **

The process for programming the FPGA is the standard method using the Quartus Programmer tool and USB Blaster.

** Visualizing the ADC values **

The 8 MSBs (out of 12) are displayed on the HEX displays of the FPGA.
