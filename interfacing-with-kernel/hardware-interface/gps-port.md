UART/DAC/PWM Port

Next to Kernel's side UAVCAN port is the 6-pin UART/DAC/PWM port which follows the same pin-out used by the Pixhawk 1 and Pixhawk 2 flight
controllers. The 6-pin port supports existing and future drone GPS units for geo-referencing captured media if you do not want to connect
to the vehicle's main controller. Examples of some supported GPS units can be found on the [Pixhawk GPS page](https://pixhawk.org/peripherals/sensors/gps).

![](/assets/uart_dac_pwm.jpg)

| Pin #    | Name                | Direction    | Description          |
|----------|---------------------|--------------|----------------------|
|    1     | VCC_SYS_5V          | OUT          | Power                |
|    2     | UART2_TXD           | OUT          | UART TX|
|    3     | UART2_RXD           | IN           | UART RX|
|    4     | DAC1                | OUT          | Analog Video            |
|    5     | PWM3_IN             | IN           | PWM|
|    6     | GND                 | -            | Ground |

