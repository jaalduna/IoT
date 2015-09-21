# IoT

This proyect is about connecting things at house to the internet to control them and to collect information from them. This is achieved here using a wireless sensor/actuator node. This nodes are strongly focused on indoor applications under IoT requierements.

The [Thread](http://threadgroup.org) group sponsored by Google among other big companies, propose the use of IEEE 802.15.4  and 6LowPan  standard to stablish communication between IoT devices.

Two types of devices are divised here, noted as *nodes* and *edge routers*

1. *nodes* devices acts like a terminal node, with a direct interface with sensor and actuators. Between nodes within the 6lowPan network, the 802.15.4 physical transport layer is used.  By the other hand, 
1. *edge routers* translate the in-network communication protocol 802.15.4 to other physical interface such as Ethernet or Wifi. Over This physical layers an UDP/IP protocol is used. For nodes a compresed version of the UDP/IP protocol is used, according to the 6LowPan standard. Whereas for Edge networks, traditional UDP/IP protocol is used. Then the *edge routers* also compress and decompress the UDP/IP protocol.

## The nodes
From a sensing point of view a node should have the capability to sense all the relevant variables for a domotic applications. This includes:

1. Detecting prescense 
2. Detecting/processing human voice
3. Measuring analog variables

From an actuating point of view a node should have the capacilibyt to:

1. Switching on/off electronic devices
2. Dimming lights

Over this sensor/actuator functions, coordination functions are requiered such as:

1. Setting timmers,
2. Power managment,
3. Signals processing, and
4. Communication  

While the above is true, each node can only implement a subgroup of this functions. In this project the focus are going to be on sensing AC power consumption and Switching lights on/off.

![Alt foto](./foto.png)
 

## Testbed
How to test a pcb?

First, what is need to be tested has to be defined. Tipically for a pcb there are somo common functions that has to be verified. Also there are inputs and outputs. The Inputs and outputs can be roughtly classified into by its nature as analog or digital signals. Or by their speed as low speed or high speed. Four group of signals can then be analized:

1. *Analog and slow signals*: This signals can be analized with traditional analog to digital converters. The resolution requiered depends on the accuracy requiered for the measurment, also the voltage range is important to take into account.
2. *Analog and fast signals*: RF fenomena occurs when transmitting fast-analog signals. Then, special care should be taken when meausing them to do not distord them. Tipically an osciloscope is requiered to observe the transcients properties of the signal. Altough, fast ADC will also do the job in some cases (Nyquist Cryteria).
3. *Slow Digital signals*: This signals can be analized with general porpouse I/O pins.
4. *Fast Digital signals: This signals has to be analized with a logic analizer. 

The experimental setup consist tipically of 
 



1. Power levels: If the circuit has voltage regulators, the power level for each regulated voltage has to be measured. 
