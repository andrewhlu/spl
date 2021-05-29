# Smart Parking Lot
![parkingbase-logo](parkingbase-logo.png)

ECE 189 - [Computer Engineering Capstone](https://web.ece.ucsb.edu/~yoga/capstone/), Professor Isukapalli
---

## Team Members

* Andrew Lu - Team Lead
* Finn Linderman
* Luyao Han
* Seungjun Cho

## Project Statement

The rapid advancement of cloud computing has boosted the development of IoT devices in recent years. For example, IoT devices are deployed into farms to monitor and manage the status of crops. In another case, a massive amount of IoT devices are used to gather the wind direction & speed data for predicting the weather. In this project, we want to take the advantage of the current IoT development and try to save drivers time while they are searching for an unoccupied parking spot. Specifically, we are aiming to design a smart parking lot to ease the process of finding a parking spot.

## Project Objective

In this project, you will design a smart parking lot prototype. Whenever a driver enters a parking lot, the driver can use his/her phone to open this parking lot app, from where he/she can tell what are the available spots. So instead of wandering around to find an empty spot, the driver can locate the empty spot right away and drive to the empty spot directly. To achieve the above features, this smart parking lot should be able to track which spot is occupied and which spot is available. As the front-end of this project, a web-based or phone-based app should indicate the driver where are the empty parking spots.

## Project Tasks

### System Overview
- Design a smart parking lot system to achieve the above features and draw block diagrams.
- In addition to just being functional, this system should also be achievable with a low price, mass deployable, and power saving.
- Consider the interfaces between different modules, such as what protocols should be used between the server and the IoT devices, or what are the arguments and return values of the APIs.

### Hardware Design
- Design the schematics.
- Verify the design using prototype and development boards.
- Develop the PCB for IoT devices targeting for deployment.
- Design necessary 3D parts to construct a mini parking lot for demo purposes.
- Design a gateway capable of handling 20+ endnodes

### Software Design
- Server-side backend logic and APIs design.
- IoT devises firmware design, usually involves configuring interfaces like I2C, SPI, etc, communicating with sensors and managing threads if RTOS is used.
- Front-end application design.

## Block Diagram

![BlockDiagram](/demo_pics/BlockDiagram.png)

## Project Milestones

[Milestone 1](milestone1.pdf)
[Milestone 2](spl_winter2021.pdf)

## Sensor Unit Assembly
![sensor_rendering02_edit](sensor_rendering02_edit.png)
![Sensor-Unit](Sensor-Unit.png )


## Sensor Unit PCB Design
[PCB Schematics](sch.pdf)
#### Miscellaneous
![miscellaneous](pins.png){:height="50%" width="50%"}

#### Power Management
![power management](power.png)

#### LoRa Comm
![LoRa](wireless.png)

#### STM32 Microcontroller
![MCU](MCU.png)

[PCB Layout(Open With Kicad)](spl_prototype.zip)

![PCB Assembly00](PCBAssembly00.png)

![PCB Assembly01](PCBAssembly01.png)

![spl_prototype01.png](spl_prototype01.png)

#### Firmware Block Diagram

![FirmwareBlock](firmware_block.png )

#### Gateway Implementation

#### GUI Screenshots
