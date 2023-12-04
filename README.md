# SmartFridge


## CubeMX Configuration:

- Under the Analog tab, choose ADC
  - Enable channels 8 to 11 as Single-ended
  - Under Parameter Settings, Go to ADC_Regular_ConversionMode and set the number of conversions to 4
  - Go to the below-created ranks, and ensure that each corresponds to a different channel
  - Go to DMA Settings and click "Add" and make sure that "Memory" is only checked
- Under the Connectivity tab, choose I2C1
  - In the dropdown menu, choose I2C
  - 
- STM32 is receiving from UART1 and transimitting through UART2 through the bluetooth module -> Baud rates for both = 9600
- Interrupts should be enabled globally for UART1
- Before generating the code, go to the Project Manager tab, ensure that the Toolchain/IDE is MDK-ARM, then go to Code Generator and choose "Copy only the necessary library files"

## Project Settings
- Ensure that "Reset and Run" is checked. To check it, go to the "Options for Target...", click the "Debug" tab, click on "Settings" beside the ST-Link Debugger, choose the "Flash Download" tab, and click "Reset and Run".
- To set up the LCD:
- Download liquidcrystal_i2c.h and put it in the Core/Inc folder.
- From the project, create a liquidcrystal_i2c.c file, and copy the file contents from the repo.
- Click on "Rebuild"

## Wire Connections:
- GND on STM32 with the Ground on the breadboard.
- The right pin of each Force Sensitive Resistor (FSR) connected to the ground on the breadboard
- 5V on STM32 connected to the positive line on the breadboard.
- 4 resistors (100k), one side connected with the positive line and the other connected to the left pin of FSR.
- Pins A2 to A5 connected to the left pin of FSR.
- Ground on Bluetooth module connected with the ground line on the breadboard.
- VCC on Blutooth module connected to 3.3V on STM32.
- TXD on Bluetooth module connected to D0 (Rx of UART1) on STM32.
- RXD on Bluetooth module connected to A7 (TX of UART2) on STM32.
- Ground on LCD adapter module connected with ground line on breadboard.
- The VCC on the LCD adapter module connected the positive line on breadboard.
- The SDA on the LCD adapter module connected the D4 on STM32.
- The SCL on the LCD adapter module connected the D5 on STM32.
  
    ![alt text](circuit-task1.png)
