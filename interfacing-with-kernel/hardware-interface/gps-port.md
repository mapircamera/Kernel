#PWM/UART/DAC Side Port

The 6-pin PWM/UART/DAC port allows you to interface with UART components, provides SD video out, and the necessary power and ground pins to power a 5VDC device.  The port is a [JST SM06B-GHS-TB](http://tinyurl.com/hrlfyu8) and mates with a plug [JST GHR-06V-S](http://www.digikey.com/product-detail/en/jst-sales-america-inc/GHR-06V-S/455-1596-ND/807818).

![](/assets/uart_dac_pwm.jpg)

| Pin #    | Name                | Direction    | Description          |
|----------|---------------------|--------------|----------------------|
|    1     | VCC_SYS_5V          | OUT          | Power 5VDC               |
|    2     | UART2_TXD           | OUT          | UART TX|
|    3     | UART2_RXD           | IN           | UART RX|
|    4     | DAC1                | OUT          | Analog Video            |
|    5     | PWM3_IN             | IN           | PWM|
|    6     | GND                 | -            | Ground |

