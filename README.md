# SmartFridge


## CubeMX Configuration:

- Under analog tab, choose ADC
- Enable channels 8 to 11 as Single ended
- Under Parameter Settings, Go to ADC_Regular_ConversionMode and set number of conversions to 4
- Go to the below created ranks, and enusre that each corresponds to different channel
- Go to DMA Settings and click "Add" and make sure that "Memory" is only checked
