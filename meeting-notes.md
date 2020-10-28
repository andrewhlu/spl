# Smart Parking Lot - Team Meeting Notes

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
- cannot get a Park JAPA sensor from TPS

Suggested research topics:
- wireless transceiver device suited for average parking lot dimension
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
  - Zigbee
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

## 10/14 Meeting

This meeting was mostly a status update for Professor Yoga and the TAs. We presented our plans for researching communication modules, and finalized purchases for the dev board and magnetometer.

Action item for next meeting includes creating a chart comparing the various protocols and modules so we can start purchasing them. 

## 10/22 and 10/23 Meetings

This meeting started with some sad news - Kelly Yeh has left the group to pursue CS Capstone. We wish her well in her endeavors!

Earlier this week, we had agreed to limit our research to only LoRaWAN and Zigbee because these protocols were openly available and widely used, and were most suitable for our project due to range and power consumption. With the scope narrowed down, we spent our time researching various modules and compiled our findings into the following tables:

[SPL Parts Comparison](https://docs.google.com/presentation/d/1yRpL1xZ8KImvildn2UcqCzZ-FXLFVyuSgNTehhlwKwY/edit?usp=sharing)

Both technologies had their advantages and disadvantages, so we ultimately decided in Friday's meeting with Professor Yoga and the TAs that it would be beneficial to experiment with both. We discussed some of the modules we found, and made the decision to purchase a set of each andd test with it in the coming weeks.

Aside from compiling our research on communication modules, we spent the meeting compiling [Milestone 1](milestone1.pdf).

Action items for next week include procuring the LoRaWAN and Zigbee modules and dev boards, and testing our new magnetometer in one of the UCSB parking structures.
