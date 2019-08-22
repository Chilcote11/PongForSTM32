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
- [System Workbench for STM32 (a version of the Eclipse IDE)](https://www.st.com/en/development-tools/sw4stm32.html)

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

As previously mentioned, this project was a collaborative effort.  However, my hope is that this repository serves not only to showcase the Pong application, but also my experience.  For that reason, and because this is an independent repository, I'll only discuss my individual contributions below.

This project can be pretty easily be broken down into four tasks, though highly interdependent upon one another.  These tasks are described as follows along with my contributions to each.  All of the the code can be found in `/src/main.c`
- Interfacing with the display
	- This required a thorough understanding of the datasheet, particularly the timing requirements.
	- Another team member handled wiring this display to the microcontroller; I wrote the sections of code that interfaced with it.
- Retrieving input from the joysticks
	- Originally, the joysticks were intended to be communicated with over an I2C bus, but documentation was found wanting.  Instead, input was read through the microcontrollers analog-to-digital converter
	- I made no contributions here
- Generating the (ironic) tetris theme song
	- To do this, the song's sheet music and individual note frequencies (in Hz) needed to be looked up and run through the microcontroller's digital-to-analog converter, which of course had to be configured.  
	- I wrote the entirety of this section.
- Developing the game logic
	- This was the last thing to be done.  Paddles and the game ball needed to be drawn on to the screen.  All three needed to move around and respond in real time to joystick signals and collisions with the sides and each other.
	- I wrote most of this section, delegating one minor portion to other teammates
		- Two other teammates added the functionality to display text on the screen (i.e. the countdown before the game starts)

This was a lighter semester for me, so it was easier for me to handle more of the load of this project than it was for others on my team (who admittedly seemed much less interested in our final grade).

## Deployment Instructions

**Hardware Setup**

Unfortunately another team member held on to the remnants of this project, so I don't have instructions for you on how to wire it up.  However, if you really want to see it in action, and you know your way around a microcontroller, it could be a fun challenge to check out the source code and see if you can't figure out how to wire it up yourself!

I did reach out to that team member; on the off chance he still has it (and left it connected), I may have a picture for you soon of our setup!

**Software Setup**

- Download [System Workbench](https://www.st.com/en/development-tools/sw4stm32.html)
- Import this project
- Ensure you have standard peripheral firmware (Eclipse should prompt you to download this)
- Plug in your microcontroller (wired up, of course)
- Run the application and enjoy!
	- There is no score limit, so you can play forever! (or add one)

