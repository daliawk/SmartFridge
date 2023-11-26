# SmartFridge


## CubeMX Configuration:

- Under analog tab, choose ADC
- Enable channels 8 to 11 as Single ended
- Under Parameter Settings, Go to ADC_Regular_ConversionMode and set number of conversions to 4
- Go to the below created ranks, and enusre that each corresponds to different channel
- Go to DMA Settings and click "Add" and make sure that "Memory" is only checked
- STM32 is receiving from UART1 and transimitting through UART2 through the bluetooth module -> Baud rates for both = 9600
- Interrupts should be enabled globally for UART1

  ## Wire Connections:
  - GND on STM32 with the Ground on the breadboard.
  - The right pin of each Force Sensitive Resistor (FSR) connected to ground on breadboard
  - 5V on STM32 connected to positive line on breadboard.
  - 4 resistors (100k) one side connected with positive line and other connected to the left pin of FSR.
  - Pins A2 to A5 connected to the left pin of FSR.
  - Ground on Blutooth module connected with ground lin on breadboard.
  - VCC on Blutooth module connected to 3.3V on STM32.
  - TXD on Bluetooth module connected to D0 (Rx of UART1) on STM32.
  - RXD on Bluetooth module connected to A7 (TX of UART2) on STM32.

    ![alt text](circuit-task1.png)
