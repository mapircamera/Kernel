Expansion Port


|                  |          |          |                  | 
|-----------------:|:--------:|:--------:|:-----------------|
| ** USB JTAG**    | **PORT** | **PORT** | **HDMI**         | 
| VCC_SYS_5V       | 1        | 2        | VCC_SYS_5V       | 
| VCC_SYS_5V       | 3        | 4        | VCC_SYS_5V       | 
| X                | 5        | 6        | X                | 
| iMX6_RGMII_RXCLK | 7        | 8        | GND              | 
| iMX6_RGMII_RXD0  | 9        | 10       | iMX6_RGMII_TXCLK | 
| iMX6_RGMII_RXD1  | 11       | 12       | iMX6_RGMII_TXD0  | 
| iMX6_RGMII_RXD2  | 13       | 14       | iMX6_RGMII_TXD1  | 
| iMX6_RGMII_RXD3  | 15       | 16       | iMX6_RGMII_TXD2  | 
| iMX6_RGMII_RXDV  | 17       | 18       | iMX6_TXD3        | 
| RGMII_RSTn       | 19       | 20       | iMX6_RGMII_TXEN  | 
| RGMII_MDIO       | 21       | 22       | RGMII_INT        | 
| RGMII_MDC        | 23       | 24       | RGMII_REF_CLK    | 
| GND              | 25       | 26       | GND              | 
| 12C1_SCL         | 27       | 28       | CSP15_MOSI       | 
| 12C1_SDA         | 29       | 30       | CSP15_SCLK       | 
| UART1_TXD        | 31       | 32       | CSP15_MISO       | 
| UART1_RXD        | 33       | 34       | GND              | 
| GND              | 35       | 36       | DAC1             | 
| GND              | 37       | 38       | GND              | 
| X                | 39       | 40       | GPIO_1           | 
| GPIO_2           | 41       | 42       | GPIO_3           | 
| DISP_DAT6        | 43       | 44       | DISP_DAT7        | 
| DISP_DAT4        | 45       | 46       | DISP_DAT5        | 
| DISP_DAT2        | 47       | 48       | DISP_DAT3        | 
| DISP_DAT0        | 49       | 50       | DISP_DAT1        | 
| DISP_DAT16       | 51       | 52       | DISP_DAT17       | 
| DISP_DAT18       | 53       | 54       | DISP_DAT19       | 
| DISP_DAT20       | 55       | 56       | DISP_DAT21       | 
| DISP_DAT22       | 57       | 58       | DISP_DAT23       | 
| GND              | 59       | 60       | GND              | 



| **Pin** | **Label**    | **I/O Voltage** | **Default**          | **Alt. Function 1** | **Alt. Function 2** | 
|---------|--------------|-----------------|----------------------|---------------------|---------------------| 
| 1       | VCC_SYS_5V   |                 | 5V Power ~danger     |                     |                     | 
| 2       | VCC_SYS_5V   |                 | 5V Power ~danger     |                     |                     | 
| 3       | VCC_SYS_5V   |                 | 5V Power ~danger     |                     |                     | 
| 4       | VCC_SYS_5V   |                 | 5V Power ~danger     |                     |                     | 
| 5       | X            |                 | NC                   |                     |                     | 
| 6       | X            |                 | NC                   |                     |                     | 
| 7       | RGMII_RXC    | 1.8 V           | RCMII_RXC ~info      | GPIO6_IO30          |                     | 
| 8       | GND          |                 | **Ground**           |                     |                     | 
| 9       | RCMII_RD0    | 1.8 V           | RCMII_RD0 ~info      | GPIO6_IO25          |                     | 
| 10      | RCMII_TXC    | 1.8 V           | RCMII_TXC ~info      | GPIO6_IO19          |                     | 
| 11      | RCMII_RD1    | 1.8 V           | RCMII_RD1 ~info      | GPIO6_IO27          |                     | 
| 12      | RCMII_TD0    | 1.8 V           | RCMII_TD0 ~info      | GPIO6_IO20          |                     | 
| 13      | RCMII_RD2    | 1.8 V           | RCMII_RD2 ~info      | GPIO6_IO28          |                     | 
| 14      | RCMII_TD1    | 1.8 V           | RCMII_TD1 ~info      | GPIO6_IO21          |                     | 
| 15      | RCMII_RD3    | 1.8 V           | RCMII_RD3 ~info      | GPIO6_IO29          |                     | 
| 16      | RCMII_TD2    | 1.8 V           | RCMII_TD2 ~info      | GPIO6_IO22          |                     | 
| 17      | RCMII_RX_CTL | 1.8 V           | RCMII_RX_CTL ~info   | GPIO6_IO24          |                     | 
| 18      | RCMII_TD3    | 1.8 V           | RCMII_TD3  ~info    | GPIO6_IO23          |                     | 
| 19      | ENET_CRS_DV  | 1.8 V           | RCMII_RSTN  ~info    |                     |                     | 
| 20      | RCMII_TX_CTL | 1.8 V           | RCMII_TX_CTL  ~info   | GPIO6_IO26          |                     | 
| 21      | ENET_MDIO    | 1.8 V           | ENET_MDIO   ~info   | GPIO6_IO22          |                     | 
| 22      | ENET_RXD1    | 1.8 V           | ENET_1588_     EVENT3_OUT  ~info| GPIO6_IO26          |                     | 
| 23      | ENET_MDC     | 1.8 V           | RCMII_MDC   ~info    | GPIO6_IO22          |                     | 
| 24      | ENET_REF_CLK | 1.8 V           | ENET_TX_CLK   ~info   | GPIO6_IO23          |                     | 
| 25      | GND          |                 | **Ground**           |                     |                     | 
| 26      | GND          |                 | **Ground**           |                     |                     | 
| 27      | EIM_D21      | 3.3 V           | 12SCL                | GPIO3_IO21          |                     | 
| 28      | SD2_CMD      | 3.3 V           | GPIO3_IO21           |                     |                     | 
| 29      | EIM_D28      | 3.3 V           | I2C1_SDA             | GPIO3_IO28          |                     | 
| 30      | SD2_CMD      | 3.3 V           | GPIO1_IO11           |                     |                     | 
| 31      | GPIO_7       | 3.3 V           | *UART_TX_DATA*       | GPIO1_IO07          |*FLEXCAN1_TX*  | 
| 32      | SD2_DAT0     | 3.3 V           | GPIO_IO15            |                     |                     | 
| 33      | GPIO_8       | 3.3 V           | *UART2_RX_DATA*      | GPIO1_IO08       | *FLEXCAN1_RX*| 
| 34      | GND          |                 | **Ground**           |                     |                     | 
| 35      | GND          |                 | **Ground**           |                     |                     | 
| 36      | DAC          |                 | Analog Video out     |                     |                     | 
| 37      | GND          |                 | **Ground**            |                     |                     | 
| 38      | GND          |                 | **Ground**           |                     |                     | 
| 39      | X            |                 | NC                   |                     |                     | 
| 40      | NANDF_D1     | 3.3 V           | GPIO2_IO01 ~active   |                     |                     | 
| 41      | NANDF_D2     | 3.3 V           | GPIO2_IO02 ~active   |                     |                     | 
| 42      | NANDF_D3     | 3.3 V           | GPIO2_IO03 ~active   |                     |                     | 
| 43      | DISP0_DAT6   | 3.3 V           | ECSPI3_SS3 ~warning  | GPIO4_IO27 ~active  |                     | 
| 44      | DISP0_DAT7   | 3.3 V           | ECSPI3_RDY ~warning  | GPIO4_IO28  ~active |                     | 
| 45      | DISP0_DAT4   | 3.3 V           | ECSPI3_SS1 ~warning  | GPIO4_IO25 ~active  |                     | 
| 46      | DISP0_DAT5   | 3.3 V           | ECSPI3_SS2 ~warning  | GPIO4_IO26 ~active  |                     | 
| 47      | DISP0_DAT2   | 3.3 V           | ECSPI3_MISO ~warning | GPIO4_IO23 ~active  |                     | 
| 48      | DISP0_DAT3   | 3.3 V           | ECSPI3_SS0 ~warning  | GPIO4_IO24 ~active  |                     | 
| 49      | DISP0_DAT0   | 3.3 V           | ECSPI3_SCLK ~warning | GPIO4_IO21 ~active  |                     | 
| 50      | DISP0_DAT1   | 3.3 V           | ECSPI3_MOSI ~warning | GPIO4_IO22 ~active  |                     | 
| 51      | DISP0_DAT16  | 3.3 V           | GPIO4_IO10 ~active   | ECSPI2_MOSI ~warning |                     | 
| 52      | DISP0_DAT17  | 3.3 V           | GPIO4_IO11 ~active   | ECSPI2_MISO ~warning |                     | 
| 53      | DISP0_DAT18  | 3.3 V           | AUD4_RXFS ~success   | ECSPI2_SS0 ~warning  | GPIO4_IO12  ~active | 
| 54      | DISP0_DAT19  | 3.3 V           | AUD4_RXC ~success    | ECSPI2_SCLK ~warning | GPIO4_IO13 ~active  | 
| 55      | DISP0_DAT20  | 3.3 V           | AUD4_TXC ~success    | ECSPI1_SCLK ~warning | GPIO4_IO14  ~active | 
| 56      | DISP0_DAT21  | 3.3 V           | AUD4_TXD  ~success   | ECSPI1_MOSI ~warning | GPIO4_IO15 ~active  | 
| 57      | DISP0_DAT22  | 3.3 V           | AUD4_TXFS ~success   | ECSPI1_MISO ~warning | GPIO4_IO16 ~active  | 
| 58      | DISP0_DAT23  | 3.3 V           | AUD4_RXD ~success    | ECSPI1_SS0 ~warning  | GPIO4_IO17 ~active  | 
| 59      | GND          |                 | **GROUND**           |                     |                     | 
| 60      | GND          |                 | **GROUND**           |                     |                     | 
