#UART/DAC/PWM Side Port

The 6-pin UART/DAC/PWM port allows you to interface with a UAS GPS (and other UART) components, provides SD video out, and the neccessary power and ground pins to power a Kernel camera module.  The port is a [JST SM06B-GHS-TB](http://tinyurl.com/hrlfyu8) and mates with a plug [JST GHR-06V-S](http://www.digikey.com/product-detail/en/jst-sales-america-inc/GHR-06V-S/455-1596-ND/807818).

The 6-pin port can support existing and future drone GPS units for geo-referencing captured media if you do not want to connect
to the vehicle's main controller. Examples of some supported GPS units can be found on the [Pixhawk GPS page](https://pixhawk.org/peripherals/sensors/gps). In theory, any GPS that could can plug into a Pixhawk 2/1 (or similar flight controller) should be supported, but please match the pins up to confirm.

![](/assets/uart_dac_pwm.jpg)

| Pin #    | Name                | Direction    | Description          |
|----------|---------------------|--------------|----------------------|
|    1     | VCC_SYS_5V          | OUT          | Power 5VDC               |
|    2     | UART2_TXD           | OUT          | UART TX|
|    3     | UART2_RXD           | IN           | UART RX|
|    4     | DAC1                | OUT          | Analog Video            |
|    5     | PWM3_IN             | IN           | PWM|
|    6     | GND                 | -            | Ground |

