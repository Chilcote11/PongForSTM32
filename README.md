# PongForSTM32
Last Updated: August 2019

**Contents**
- Application Description
- Resources Used
- Individual Contributions
- Deployment Instructions


## Application Description: 

Welcome to the PongForSTM32 application!  
This application is the offspring of Purdue University's ECE 362: Microcontroller Systems and Interfacing, an upper level 4-credit hour enegineering lab.  The course was structured such that my peers and I learned all about microcontroller instruction sets, assembly language programming, microcontroller interfacing and peripherals, and embedded system design over the first 14 weeks of the course and brought it all together for a final project at the end.  This is that final project, and for ours my team and I chose to use our new-found knowledge to recreate the classic "Pong" video game from the 1970's.  


## Resources Needed
### Hardware
- [STM32FO51R8T6 Microcontroller](https://www.st.com/content/st_com/en/products/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus/stm32-mainstream-mcus/stm32f0-series/stm32f0x1/stm32f051r8.html)
	- Be sure you get the R8T6, not one of the others listed!
- [Graphic LCD 128x64 STN LED Display](https://www.sparkfun.com/products/710)
- [SparkFun Qwiic Joystick](https://www.sparkfun.com/products/15168)
- [One half-size breadboard](https://www.adafruit.com/product/64?gclid=CjwKCAjw-vjqBRA6EiwAe8TCk8S5QXQeIe2bEctszV2AJxYfrKjl6m-pp9JCeR5xFuJB3Cr07XFLvhoCY8YQAvD_BwE)
- [Jumper Wire Kit](https://www.sparkfun.com/products/124)
- Computer Speakers (any kind will work)
- Auxhillary cable (to use your speakers)
- [3.5mm Stereo Female Panel Mount Connector](https://www.showmecables.com/3-5mm-stereo-female-panel-mount-connector-plastic?gclid=CjwKCAjw-vjqBRA6EiwAe8TCk4Y-L9MR9ks_hKQe5znDtQKljaLwwvi-9W5WHRboSuzrpbzpo6gPmBoCWwUQAvD_BwE)

### Software
- System Workbench for STM32 (a version of the Eclipse IDE)(https://www.st.com/en/development-tools/sw4stm32.html)

### Documentation

Note, you will only need documentation if you hope to make modifications or additions to this application.  It will run as is, if setup properly.

**ARM References**
- [ARMv6-M Architecture Reference Manual](https://engineering.purdue.edu/ece362/refs/ARMv6-M_Architecture_Manual.pdf)
- [ARM Cortex-M0 Generic User Guide](https://engineering.purdue.edu/ece362/refs/Cortex-M0_Generic_User_Guide.pdf)
- [ARM Cortex-M0 Technical Reference](https://engineering.purdue.edu/ece362/refs/Cortex-M0_Technical_Reference.pdf)
- [STM32F0xx Cortex-M0 programming manual](https://engineering.purdue.edu/ece362/refs/PM0215_Programming_Manual.pdf)

**STM32 References**
- [STM32F0x1 Family Reference](https://engineering.purdue.edu/ece362/refs/STM32F0x1_Family_Reference.pdf)
- [STM32F051R8T6 Data Sheet](https://engineering.purdue.edu/ece362/refs/STM32F051R8T6.pdf)
- [STM32F0DISCOVERY User Manual](https://engineering.purdue.edu/ece362/refs/STM32F0Discovery_User_Manual.pdf)
- [ST Microelectronics site for STM32F051R8 documentation (including errata)](https://www.st.com/en/microcontrollers-microprocessors/stm32f051r8.html)

**Device Datasheets**
- [LCD Display Datasheet](https://www.sparkfun.com/datasheets/LCD/GDM12864H.pdf)
- [Joystick Quasi-Datasheet](https://github.com/sparkfun/Qwiic_Joystick/)


## Individual Contributions

As previously mentioned, this project was a collaborative effort.  However, because this repository was created to showcase the Pong application, and not to be used for its development, I'll only discuss my individual contributions below.

- Interfacing with the display
- Retrieving input from the joysticks
- Generating the (ironically) tetris theme song
- Developing the game logic

## Deployment Instructions


