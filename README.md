# DE10-ADC
This repository has the hardware description files and a guide for configuring the on-board ADC on DE-series FPGAs for 2MHz sampling rate.

This guide is using Quartus Prime 16.0 and Qsys IP tool, but should also be supported for Platform Designer (formerly Qsys) and a newer version of Quartus.

**FPGA Configuration Information**

The board used for this configuration is the DE10-Lite (10M50DAF484C7G) which has two on-board FPGAs but only ADC0 is used. See the user manual and configuration guide for pin assignments, and ADC configurations if you are using a different board. 

This project uses SW[2:0] for selecting which of the analog inputs the ADC samples from and is shown on HEX5.

The 12 ADC bit values are displayed in hexidecimal format on the HEX3, HEX2, and HEX1 displays.



### Created By New Mexico State University ECE Student

(Updated May 8, 2019)  

 Derrick Rivera


## ADC IP Configuration

This section describes the process of configuring the ADC core control module and necessary PLL.

### Configuring the soft-IP
* Open Qsys or Platform Designer
* In the IP Catalog search bar, search for Altera Modular ADC core
![IP Catalog Search Image](https://github.com/driveraweb/DE10-ADC/Images/ip_search_adc)
* Double-click it to open the configuration window. Configure it as follows
![ADC Configuration](https://github.com/driveraweb/DE10-ADC/Images/config_adc)




## Interfacing with the ADC

The ADC interface is I2C, but this project uses a wrapper based on the ADC controller synthesis. The source Verilog is the top-level entitiy of the Quartus project (see adc_2M.v). This is a modified version of the ADC_RTL Template that can be downloaded from Terasic's website.



## Deployment

**Uploading HDL to the FPGA**

The process for programming the FPGA is the standard method using the Quartus Programmer tool and USB Blaster.
