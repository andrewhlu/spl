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

![BlockDiagram](/demo_pics/block_diagram_01.png)

## Application Scene
![BlockDiagram](/demo_pics/application_scene.png)

## Project Milestones

[Milestone 1](/demo_pics/milestone1.pdf)

[Milestone 2](/demo_pics/spl_winter2021.pdf)

## Sensor Unit Assembly
![sensor_rendering02_edit](/demo_pics/sensor_rendering02_edit.png)


<p align="center">
  <img width="640" height="480" src=/demo_pics/sensor_unit_assembly_electric_parts.png>
</p>


<p align="center">
  <img width="640" height="300" src=/demo_pics/Sensor-Unit.png>
</p>


## Sensor Unit PCB Design
[PCB Schematics](/demo_pics/sch.pdf)
#### Miscellaneous


#### Power Management


#### LoRa Comm

#### STM32 Microcontroller
[PCB Layout(Open With Kicad)](/demo_pics/spl_prototype.zip)


#### Firmware Block Diagram


#### Gateway Implementation

#### GUI Screenshots
