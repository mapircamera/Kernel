#UART/DAC/PWM Side Port

The 6-pin UART/DAC/PWM port follows the same pin-out used by the Pixhawk 1 and Pixhawk 2 flight controllers. The port is a [JST SM06B-GHS-TB](http://tinyurl.com/hrlfyu8) and mates with a plug [JST GHR-06V-S](http://www.digikey.com/product-detail/en/jst-sales-america-inc/GHR-06V-S/455-1596-ND/807818).

The 6-pin port can support existing and future drone GPS units for geo-referencing captured media if you do not want to connect
to the vehicle's main controller. Examples of some supported GPS units can be found on the [Pixhawk GPS page](https://pixhawk.org/peripherals/sensors/gps).

The port is a [JST SM04B-GHS-TB](http://tinyurl.com/jjkkat2) and mates with a plug [JST GHR-04V-S](http://www.digikey.com/product-detail/en/jst-sales-america-inc/GHR-04V-S/455-1594-ND/807816).



![](/assets/uart_dac_pwm.jpg)

| Pin #    | Name                | Direction    | Description          |
|----------|---------------------|--------------|----------------------|
|    1     | VCC_SYS_5V          | OUT          | Power                |
|    2     | UART2_TXD           | OUT          | UART TX|
|    3     | UART2_RXD           | IN           | UART RX|
|    4     | DAC1                | OUT          | Analog Video            |
|    5     | PWM3_IN             | IN           | PWM|
|    6     | GND                 | -            | Ground |

