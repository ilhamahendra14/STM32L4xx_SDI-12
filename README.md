# STM32L4xx_SDI-12

## Hardware
I used 3 board/module:
+ Custom board with STM32L432KCU6
+ Step Up 3v3 to 5v
  - VCC input from PA1 pin
+ Logic converter
  - 3v3 VCC from PB4 pin
  - 5v VCC from Step Up output

**Note:** SDI-12 use 12V (I have 12V output from my custom board)



## Firmware
Important: 
+ Relation between baudrate & freq
  - 1 baud rate = 1 Hz
  - 1200 baud rate = 1200 bits/seconds
  - f = 1200 Hz = 1.2MHz
  - Please, set UART clock <= 1.2MHz.
+ Basically SDI-12 uses a single UART pin (TX) and cycles between TX and RX to send and receive commands (respectively)
  - Please, enable 'TX and RX Pins Swapping'.

This firmware tested with [Solinst Sensor](https://www.solinst.com/products/data/3001.pdf)<br/>
