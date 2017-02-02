GPS Port

Next to Kernel's side UAVCAN port is the 6-pin GPS port which follows the same pin-out used by the Pixhawk 1 and Pixhawk 2 flight
controllers. The 6-pin port supports existing and future drone GPS units for geo-referencing captured media if you do not want to connect
to the vehicle's main controller. Examples of some supported GPS units can be found on the [Pixhawk GPS page](https://pixhawk.org/peripherals/sensors/gps).

| Pin #    | Name                | Direction    | Description          |
|----------|---------------------|--------------|----------------------|
|    1     | VCC_5V              | out          | Supply to GPS from AP|
|    2     | MCU_TX              | out          | 3.3-5.0 V TTL level, TX of AP|
|    3     | MCU_RX              | in           | 3.3-5.0 V TTL level, RX of AP|
|    4     | SCL                 | out          | 3.3-5.0 V I2C2|
|    5     | SDA                 | in           | 3.3-5.0 V I2C2|
|    6     | GND                 | -            | GND connection|

