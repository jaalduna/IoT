# IoT

This proyect is about connecting things at house to the internet to control them and to collect information from them. This is achieved here using a wireless sensor/actuator node. This nodes are strongly focused on indoor applications under IoT requierements.

The [Thread](http://threadgroup.org) group sponsored by Google among other big companies, propose the use of IEEE 802.15.4  and 6LowPan  standard to stablish communication between IoT devices.

Two types of devices are divised here, noted as *nodes* and *edge routers*

1. *nodes* devices acts like a terminal node, with a direct interface with sensor and actuators. Between nodes within the 6lowPan network, the 802.15.4 physical transport layer is used.  By the other hand, 
1. *edge routers* translate the in-network communication protocol 802.15.4 to other physical interface such as Ethernet or Wifi. Over This physical layers an UDP/IP protocol is used. For nodes a compresed version of the UDP/IP protocol is used, according to the 6LowPan standard. Whereas for Edge networks, traditional UDP/IP protocol is used. Then the *edge routers* also compress and decompress the UDP/IP protocol.

