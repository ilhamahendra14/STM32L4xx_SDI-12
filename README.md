# STM32L4xx_SDI-12

## Hardware<br/>
+ Custom board with STM32L432KCU6<br/>
+ Step Up 3v3 to 5v
  - VCC input from PA1 pin<br/>
+ Logic converter
  - 3v3 VCC from PB4 pin<br/>
  - 5v VCC from Step Up output<br/>
<br/>
**Note:** SDI-12 use 12V (I have 12V output from my custom board)<br/>
<br/><br/>
## Firmware<br/>
Important: <br/>
+ 1200 baud rate = 1200 bits/seconds --> f = 1200 Hz = 1.2MHz. So, set UART clock <= 1.2MHz.<br/>
+ Basically SDI-12 uses a single UART pin (TX) and cycles between TX and RX to send and receive commands (respectively). So, enable 'TX and RX Pins Swapping'.<br/>
<br/><br/>
This firmware tested with [Solinst Sensor](https://www.solinst.com/products/data/3001.pdf)<br/>
