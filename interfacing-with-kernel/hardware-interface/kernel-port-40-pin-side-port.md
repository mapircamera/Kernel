# Kernel Port - 40 pin Side Port

The Kernel port is the main interface between the camera module and the link boards used in the camera arrays. The Kernel port is a [TE CHAMP 2129260-2](http://www.te.com/usa-en/product-2129260-2.html) and mates to the link board or breakout board's [TE CHAMP 2129261-1](http://www.te.com/usa-en/product-2129261-1.html). For straight connecting cables you would us the [TE CHAMP 2129276-1](http://www.te.com/usa-en/product-2129276-1.html). You can find a list of all the compatible mating CHAMP connectors [here](http://www.te.com/usa-en/plp/Y30jw.html?q=&n=540054&d=545426&type=products&samples=N).

###The Kernel port is mounted to the underside of the connector board with the following pin assignment:

![](/assets/kernel_champ.PNG)

| GROUP | SIGNAL | ROW 1 PIN | ROW 2 PIN | SIGNAL | GROUP |
| :---: | :---: | :---: | :---: | :---: | :---: |
| Boot mode | BOOT\_MODE0 | 1 | 2 | GND | Power |
| Power | VCC\_SYS\_5V | 3 | 4 | VCC\_5V | Power |
| Boot mode | BOOT\_MODE1 | 5 | 6 | GND | Power |
| Power | VCC\_SYS\_5V | 7 | 8 | HDMI\_DDC\_SCL | HDMI |
| USB OTG | USB \_OTG \_ID | 9 | 10 | HDMI\_TX\_DDC\_SDA | HDMI |
| UART | UART\_OTG\_ID | 11 | 12 | GND | Power |
| Power | VCC\_USB\_OTG\_VBUS | 13 | 14 | HDMI\_MX\_HP | HDMI |
| UART | UART1\_RXD | 15 | 16 | GND | Power |
| Power | GND | 17 | 18 | OUT\_TMDS\_CLK\_N | HDMI |
| CAN | CAN1\_L | 19 | 20 | OUT\_TMDS\_CLK\_P | HDMI |
| USB OTG | USB\_OTG\_N | 21 | 22 | GND | Power |
| CAN | CAN1\_H | 23 | 24 | OUT\_TMDS\_D0\_N | HDMI |
| USB OTG | USB\_OTG\_P | 25 | 26 | OUT\_TMDS\_D0\_P | HDMI |
| Power | GND | 27 | 28 | GND | Power |
| Power | GND | 29 | 30 | OUT\_TMDS\_D1\_N | HDMI |
| Power | VCC3V3 | 31 | 32 | OUT\_TMDS\_D1\_P | HDMI |
| Analog Video Out | DAC1 | 33 | 34 | GND | Power |
| Power | GND | 35 | 36 | OUT\_TMDS\_D2\_N | HDMI |
| PWM | PWM3\_OUT | 37 | 38 | OUT\_TMDS\_D2\_P | HDMI |
| PWM | PWM4\_IN | 39 | 40 | GND | Power |


![](/assets/kernel_port_plug_lbl_c_9ce75ee3-b64c-4984-9548-5b1666dc0508.png)