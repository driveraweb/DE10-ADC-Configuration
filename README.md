# DE10-ADC
This repository has the HDL and a guide for configuring the on-board ADC on DE-series FPGAs for 2MHz sampling rate using Quartus Platform Designer (formerly Qsys).



### Created By New Mexico State University ECE Student

* Derrick Rivera


## Getting Started

These instructions will get you a copy of the project up and running on your local machine for development and testing purposes. See deployment for notes on how to deploy the project on a live system.



### Hardware 

This software was designed and implemented using the following hardware:
* RaspberryPi 3 B+
* 16GB Micro SD Card
* Pi NoIR Camera V2 
* Roscolux #2007 Storaro Blue filter
* Pi Camera V2
* IVPort V2 Pi Camera Multiplexer 
* Waveshare 7" Touchscreen Display
* 3W Infrared Illuminator (2)
* Common collector current amplifier (2) 
* RAVPower 22000mAH 4.5A Portable Phone Power Pack



## Deployment

This is where we add additional notes about how to deploy this on a live system

* Install Raspbian Jessie
* Enable Pi Camera
* Enable I2C
* In */boot/conf.txt* append:
```
    max_usb_current = 1
    hdmi_group=2
    hdmi_mode = 1
    hdmi_cvt 1024 600 60 6 0 0 0
```


### Installing Software

A step-by-step series that tells you how to get a Plant Health imaging software running

Make sure Python3.x is installed.

[Install git](https://projects.raspberrypi.org/en/projects/getting-strated-with-git/4)

[Introduction to git](https://product.hubspot.com/blog/git-and-github-tutorial-for-beginners)

Install the dependencies:
```
chmod +x install.sh
./install.sh
```
[Install numpy using this method](https://hunseblog.wordpress.com/2014/09/15/installing-numpy-and-openblas/) 
```
pip install -r requirements.txt
```
[Install IVPort-v2](https://github.com/ivmech/ivport-v2) to /home/pi/Downloads

[Install picamera](https://github.com/waveform80/picamera) 



### Auto-start Application at Startup

Use your favorite method to run ./bin/run.sh or [see this link](https://www.dexterindustries.com/howto/run-a-program-on-your-raspberry-pi-at-startup/)


## Built With

**Python Packages**

* six
* wheel
* setuptools
* numpy
* numexpr
* opencv-python
* wxPython 
* threading
* picamera
* picamera[array]
* ivport
* datetime
* RPi.GPIO

**C++ Libraries** (see 'Install Numpy using this method')

* BLAS
* LAPACK
