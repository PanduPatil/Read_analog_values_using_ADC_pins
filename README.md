Read Analog Values Using ADC Pins
This repository demonstrates how to read analog values from ADC pins using the MSPM0G3507 microcontroller. The example code initializes the ADC, configures interrupts, and reads the analog input from pin PA15.

Features:
  Analog-to-Digital Conversion (ADC): Converts analog signals into digital values (12-bit resolution). Monitors a specific ADC pin (PA15) for voltage levels.
  LED Control Based on Voltage: If the voltage at PA15 is below 1.25V, the LED on pin PB13 is turned ON. If the voltage at PA15 is above 1.25V, the LED on pin PB13 is turned OFF.
  Interrupt Handling: Uses ADC interrupt for efficient data handling.
Key Components:
  SYSCFG_DL_init(): Initializes system configurations.
  DL_ADC12_startConversion(): Triggers the ADC conversion process.
  DL_GPIO_setPins() and DL_GPIO_clearPins(): Controls the GPIO pins for the LED.
  ADC12_0_INST_IRQHandler(): Handles the ADC interrupt for data processing.
