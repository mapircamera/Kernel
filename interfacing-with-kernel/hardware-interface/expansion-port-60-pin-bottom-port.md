Expansion Port

The bottom facing Expansion port is designed to allow accessory board development.

The connector on the Kernel camera stack bottom Connector Board is the [Hirose DF40C-60DP-0.4V(51)](http://tinyurl.com/h3w6h66). An expansion board would require the mating component [Hirose DF40HC(4.0)-60DS-0.4V(51)](https://www.hirose.com/product/en/products/DF40/DF40HC%284.0%29-60DS-0.4V%2851%29/).

Some examples may include:

-WIFI
-Bluetooth
-Cellular 4G
-GPS
-LCD
-Battery

![](/assets/kernel_expansion_port.jpg)

| **Pin** | **Label**    | **I/O Voltage** | **Default Function** | **Alt. Function 1** | **Alt. Function 2** |
|---------|--------------|-----------------|----------------------|---------------------|---------------------| 
| 1        |VCC_SYS_5V   |                 | 5V Power     |                     |                     | 
| 2        |VCC_SYS_5V   |                 | 5V Power     |                     |                     | 
| 3        |VCC_SYS_5V   |                 | 5V Power      |                     |                     | 
| 4        |VCC_SYS_5V   |                 | 5V Power     |                     |                     | 
| 5       |X            |                 | NC                   |                     |                     | 
| 6       |X            |                 | NC                   |                     |                     | 
| 7       | RGMII_RXC    | 1.8 V           | RCMII_RXC (Ethernet)  | GPIO6_IO30          |                     | 
| 8        | GND          |                 | GROUND           |                     |                     | 
| 9       | RCMII_RD0    | 1.8 V           | RCMII_RD0 (Ethernet)      | GPIO6_IO25          |                     | 
| 10      | RCMII_TXC    | 1.8 V           | RCMII_TXC (Ethernet)      | GPIO6_IO19          |                     | 
| 11      | RCMII_RD1    | 1.8 V           | RCMII_RD1 (Ethernet)      | GPIO6_IO27          |                     | 
| 12      | RCMII_TD0    | 1.8 V           | RCMII_TD0 (Ethernet)      | GPIO6_IO20          |                     | 
| 13      | RCMII_RD2    | 1.8 V           | RCMII_RD2 (Ethernet)      | GPIO6_IO28          |                     | 
| 14      | RCMII_TD1    | 1.8 V           | RCMII_TD1 (Ethernet)      | GPIO6_IO21          |                     | 
| 15      | RCMII_RD3    | 1.8 V           | RCMII_RD3 (Ethernet)      | GPIO6_IO29          |                     | 
| 16      | RCMII_TD2    | 1.8 V           | RCMII_TD2 (Ethernet)      | GPIO6_IO22          |                     | 
| 17      | RCMII_RX_CTL | 1.8 V           | RCMII_RX_CTL (Ethernet)   | GPIO6_IO24          |                     | 
| 18      | RCMII_TD3    | 1.8 V           | RCMII_TD3 (Ethernet)     | GPIO6_IO23          |                     | 
| 19      | ENET_CRS_DV  | 1.8 V           | RCMII_RSTN (Ethernet)     |                     |                     | 
| 20      | RCMII_TX_CTL | 1.8 V           | RCMII_TX_CTL (Ethernet)    | GPIO6_IO26          |                     | 
| 21      | ENET_MDIO    | 1.8 V           | ENET_MDIO (Ethernet)     | GPIO6_IO22          |                     | 
| 22      | ENET_RXD1    | 1.8 V           | ENET_1588_ EVENT3_OUT (Ethernet)  | GPIO6_IO26          |                     | 
| 23      | ENET_MDC     | 1.8 V           | RCMII_MDC  (Ethernet)     | GPIO6_IO22          |                     | 
| 24      | ENET_REF_CLK | 1.8 V           | ENET_TX_CLK (Ethernet)     | GPIO6_IO23          |                     | 
| 25       |GND          |                 | GROUND           |                     |                     | 
| 26       |GND          |                 | GROUND           |                     |                     | 
| 27      | EIM_D21      | 3.3 V           | 12SCL                | GPIO3_IO21          |                     | 
| 28      | SD2_CMD      | 3.3 V           | GPIO3_IO21           |                     |                     | 
| 29      | EIM_D28      | 3.3 V           | I2C1_SDA             | GPIO3_IO28          |                     | 
| 30      | SD2_CMD      | 3.3 V           | GPIO1_IO11           |                     |                     | 
| 31      | GPIO_7       | 3.3 V           | UART_TX_DATA       | GPIO1_IO07          |FLEXCAN1_TX  | 
| 32      | SD2_DAT0     | 3.3 V           | GPIO_IO15            |                     |                     | 
| 33      | GPIO_8       | 3.3 V           | UART2_RX_DATA      | GPIO1_IO08       | FLEXCAN1_RX| 
| 34       |GND          |                 | GROUND           |                     |                     | 
| 35       |GND          |                 | GROUND           |                     |                     | 
| 36      | DAC          |                 | Analog Video out     |                     |                     | 
| 37       |GND          |                 | GROUND            |                     |                     | 
| 38      |GND          |                 | GROUND           |                     |                     | 
| 39      | X            |                 | X                   |                     |                     | 
| 40      | NANDF_D1     | 3.3 V           | GPIO2_IO01    |                     |                     | 
| 41      | NANDF_D2     | 3.3 V           | GPIO2_IO02    |                     |                     | 
| 42      | NANDF_D3     | 3.3 V           | GPIO2_IO03    |                     |                     | 
| 43      | DISP0_DAT6   | 3.3 V           | ECSPI3_SS3   | GPIO4_IO27   |                     | 
| 44      | DISP0_DAT7   | 3.3 V           | ECSPI3_RDY   | GPIO4_IO28   |                     | 
| 45      | DISP0_DAT4   | 3.3 V           | ECSPI3_SS1   | GPIO4_IO25   |                     | 
| 46      | DISP0_DAT5   | 3.3 V           | ECSPI3_SS2 | GPIO4_IO26   |                     | 
| 47      | DISP0_DAT2   | 3.3 V           | ECSPI3_MISO  | GPIO4_IO23  |                     | 
| 48      | DISP0_DAT3   | 3.3 V           | ECSPI3_SS0   | GPIO4_IO24   |                     | 
| 49      | DISP0_DAT0   | 3.3 V           | ECSPI3_SCLK | GPIO4_IO21   |                     | 
| 50      | DISP0_DAT1   | 3.3 V           | ECSPI3_MOSI  | GPIO4_IO22   |                     | 
| 51      | DISP0_DAT16  | 3.3 V           | GPIO4_IO10   | ECSPI2_MOSI  |                     | 
| 52      | DISP0_DAT17  | 3.3 V           | GPIO4_IO11    | ECSPI2_MISO  |                     | 
| 53      | DISP0_DAT18  | 3.3 V           | AUD4_RXFS    | ECSPI2_SS0   | GPIO4_IO12   | 
| 54      | DISP0_DAT19  | 3.3 V           | AUD4_RXC     | ECSPI2_SCLK  | GPIO4_IO13   | 
| 55      | DISP0_DAT20  | 3.3 V           | AUD4_TXC     | ECSPI1_SCLK  | GPIO4_IO14   | 
| 56      | DISP0_DAT21  | 3.3 V           | AUD4_TXD     | ECSPI1_MOSI  | GPIO4_IO15   | 
| 57      | DISP0_DAT22  | 3.3 V           | AUD4_TXFS    | ECSPI1_MISO  | GPIO4_IO16  | 
| 58      | DISP0_DAT23  | 3.3 V           | AUD4_RXD     | ECSPI1_SS0  | GPIO4_IO17   | 
| 59      | GND          |                 | GROUND           |                      |                     | 
| 60      | GND          |                 | GROUND           |                      |                     | 