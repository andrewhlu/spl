# Smart Parking Lot

ECE 189 - [Computer Engineering Capstone](https://web.ece.ucsb.edu/~yoga/capstone/), Professor Isukapalli

[View Repository on GitHub](https://github.com/andrewhlu/spl)

[Open Slack Workspace](http://ucsb-capstone-21.slack.com/)

---

## Team Members

* Andrew Lu - Team Lead
* Finn Linderman
* Kelly Yeh - Scribe
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

### Software Design
- Server-side backend logic and APIs design.
- IoT devises firmware design, usually involves configuring interfaces like I2C, SPI, etc, communicating with sensors and managing threads if RTOS is used.
- Front-end application design.

---

# Meeting Notes

## 10/5 Meeting

We started this meeting by deciding on our team lead - Andrew Lu. 

We also decided on a scribe for our meetings - Kelly Yeh.

Resources compiled from individual research:

* [Bosch Parking Lot Sensor](https://www.bosch-connectivity.com/products/connected-mobility/parking-lot-sensor/)
  * A solution very similar (at least in appearance) to the one seen on JAPA. 
  * [Bosch Datasheet, Manuals](https://www.bosch-connectivity.com/products/connected-mobility/parking-lot-sensor/downloads/)
  * [Alliot (Vendor) Datasheet, Specs](https://www.alliot.co.uk/products/sensors/parking-management-sensors/bosch-lorawan-parking-sensor/)
    * This vendor sells for [£175.75 + VAT](https://www.alliot.co.uk/products/sensors/parking-management-sensors/bosch-lorawan-parking-sensor#:~:text=RRP:%20%C2%A3175.75+VAT) (which is roughly $227.2 excluding tax).
    * This is about 7.6% of our budget, so we don't think it's worth the investment to purchase for R&D.
* [2008 IEEE Paper from USC - "Intelligent Parling Lot Applications Using Wireless Sensor Networks"](http://anrg.usc.edu/~amitabhag/papers/CTS-2008.pdf)
* [Vehicle Detection Solutions - YouTube](https://www.youtube.com/watch?v=7a1fiUJtp_k)

Brief notes from our discussion of the various sensors:

Ultrasonic Sensor
- Generally very accurate when used to detect vehicles 
- Tradeoff between accuracy and power

Magnetometer
- Relatively low power consumption
- Complicated object detection algorithm
- May require heavy signal processing
- More resistant to noise

IR light
- Requires emitter + sensor combo (something on both sides)
- Measure light being emitted
- Can be used at night, but costly, and can only be used indoors

Action Items: 
- Clarify with Yoga regarding power consumption and usage/maintenance requirements in Parking lot 10 and which parking lots the project will be used for.
- Decide on overhead wired vs in-ground vehicle detection sensor
- Research and decide if solar power is an option

## 10/7 Meeting

Office hours with Yoga, Luyao, Andrew

Confirmed with Yoga: 
- wired devices are not accepted in parking lot
- cannot get a Parkjapa sensor from TPS

Suggested research topics:
- wireless transceiving device suited for average parking lot dimension
- low power consumption processor
  - Luyao will look into STM32L0
- solar panels as a method of extending battery life

Suggested device aspects:
- should last for at least 5 years

## 10/9 Meeting

We started by discussing our new project requirements from Office Hours

Problems with Battery-powered Solutions
- Wireless communication
  - This might require a lot of power, esp. to get past metal from cars and concrete slabs

Problems with Solar Panels
- Only works for outdoor parking structures without a roof (i.e. not Parking Lot 10)
- Where would we put the solar panel?
  - Putting it directly on the space would work, but we can't guarantee that there will be periods of time where there is no car parked and the unit can charge
- We are going to hold off on researching this for now - if we have time later, we can look into making a version with a solar panel (i.e. an "outdoor" model)

### Areas of Research for Next Week

Microprocessor / Magnetometer
- Luyao will look into purchasing a Nucleo dev board with an STM32L0 or L1 microprocessor and magnetometer
- Select a model over the weekend, get it reviewed briefly on Monday, then we can ask Yoga to get it expensed / procured
- We will start with a magnetometer-only solution for now, we will look into ultrasonic later (if needed)

Communication between Devices
- We want to look into pre-built communication modules instead of R&Ding our own solution
  - Will make PCB prototyping much easier
  - Matching impedance for antenna will be a challenge, not worth the time spent
  - May make power consumption issue worse though
- Potential protocols
  - Bluetooth LE
  - ZigBee
  - RFID
  - LoRaWAN / LPWAN
  - IEEE 802.11ah
- For each of these, what will we be researching?
  - Power consumption
  - Distance
  - Interference (by metal / concrete)
  - Cost
  - Scalability (number of devices)
- Potential idea: look into using hubs as a middleman between main gateway / server and parking spaces as a way to reduce power consumption

Luyao and Andrew will individually meet on Monday to discuss purchasing of dev board, otherwise we will likely not meet again as a team until Friday.

<!-- Don't edit anything below this line! -->

<style>
.markdown-body h1:first-of-type {
    display: none;
}
</style>
