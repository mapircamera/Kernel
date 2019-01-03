#PWM/UART/DAC Side Port

The 6-pin PWM/UART/DAC port on an individual Kernel allows you to interface with UART components, provides SD video out, and the necessary power and ground pins to power a 5VDC device.  The port is a [JST SM06B-GHS-TB](http://tinyurl.com/hrlfyu8) and mates with a plug [JST GHR-06V-S](http://www.digikey.com/product-detail/en/jst-sales-america-inc/GHR-06V-S/455-1596-ND/807818).

![](/assets/uart_dac_pwm.jpg)

| Pin #    | Name                | Direction    | Description          |
|----------|---------------------|--------------|----------------------|
|    1     | VCC_SYS_5V          | OUT          | Power 5VDC               |
|    2     | UART2_TXD           | IN          | UART TX|
|    3     | UART2_RXD           | OUT           | UART RX|
|    4     | DAC1                | OUT          | Analog Video            |
|    5     | PWM3_IN             | IN           | PWM|
|    6     | GND                 | -            | Ground |


##*Note About UART Connection

The connections are labeled above to match your other device (computer). For instance, connect pin2 to your computer's UART-TX pin and pin3 to your computer's UART-RX pin. Sometimes devices are labeled opposite this, so it's recommended to connect, test and if it's not working swap wires going to pin 2 and 3.

![](/assets/kernel_side_plugs_bottom_lbl2.png)

