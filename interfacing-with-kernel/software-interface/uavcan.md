# UAVCAN

UAVCAN is a lightweight protocol designed for reliable communication in aerospace and robotic applications via CAN bus. Please browse the [UAVCAN.org](http://uavcan.org/) website for more information.

* Democratic network - no single point of failure.  
* Publish/subscribe or request/response exchange semantics.  
* Allows efficient exchange of large data structures.  
* Lightweight, easy to implement protocol.  
* Supports network-wide time synchronization with microsecond precision.  
* Doubly- or triply- redundant CAN bus.  
* Can be used in deeply embedded, resource constrained, hard real-time systems.  
* The specification and high quality reference implementations are open and free to use \(MIT License\).  

The Kernel cameras use the UAVCAN bus to collect sensor data, such as position from the GPS and saves this information to each captured image's metadata. This reduces the need to save separate log files and also allows for much more accurate values compared to post processing procedures \(PPK\).

Each Kernel camera acts as a static node, with a default id of 16. You can configure this in[ MCC](https://mapir-camera.gitbook.io/kernel-development-guide/interfacing-with-kernel/software-interface/mcc).  
You must use a termination resistor to terminate the bus.  
![](../../.gitbook/assets/can_chaining_non_redundant.png)

## Default Kernel UAVCAN Settings

### Bitrate: 1000 kbit/s

### Sample Point: 800 \(80%\)

### CAN Fix Message: Both \(Fix1 and Fix2\)

### Node ID: 16

## Flight Controller Settings \(Pixhawk APM\)

Using Mission Planner \(or similar program\) configure the following parameters as follows:

### BRD\_CAN\_BITRATE = 1000000

### BRD\_CAN\_DEBUG = 0

### BRD\_CAN\_ENABLE = 2

### BRD\_CAN\_UC\_EN = 1

### BRD\_CAN\_UC\_NODE = 10

