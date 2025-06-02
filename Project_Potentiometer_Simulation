# STM32 Potentiometer-Controlled Relay with LED Output

## Overview

This project uses an **STM32F103C8** microcontroller to read an analog voltage from a **potentiometer** and control a **relay module** connected to an **LED**. When the potentiometer voltage exceeds a defined threshold, the relay is activated, turning ON the LED.

Developed using **STM32CubeIDE** and simulated in **Proteus**.

---

## Hardware Configuration

**Microcontroller**: STM32F103C8 (Blue Pill)

### Connections

- **Potentiometer**:
  - VCC: 3.3V  
  - GND: GND  
  - Wiper (Middle pin): PA0 (ADC input)

- **Relay Module**:
  - IN: PA1 (Digital Output)
  - VCC/GND: 5V/GND

- **LED**:
  - Connected to Relay's NO (Normally Open) contact and GND  
  - Turns ON when Relay is activated

---

## Functionality

- Continuously reads analog input from the potentiometer using **ADC**.
- If the voltage is above a preset threshold (e.g., > 2V), the STM32 sets PA1 **HIGH** to activate the relay.
- If below the threshold, PA1 is set **LOW** to deactivate the relay.
- The relay switches power to the LED accordingly.

---

## Development Tools

- **IDE**: STM32CubeIDE  
- **Simulation**: Proteus 8 Professional  
- **Programming Language**: C  
- **HAL Drivers** used for ADC and GPIO

---

## How to Run

1. Connect the potentiometer to PA0 and relay control pin to PA1.
2. Configure ADC1 in STM32CubeIDE for single-channel continuous conversion on PA0.
3. In code, compare ADC value to a threshold (e.g., corresponding to 2V = ~2480 for 12-bit ADC).
4. Export the `.hex` file and load it into Proteus STM32.
5. Simulate: turning the potentiometer will control the LED through the relay.

---

## Threshold Configuration (Example)

For a 12-bit ADC (0–4095 range) and 3.3V reference:
- 2V threshold → `(2 / 3.3) * 4095 ≈ 2480`

In code:
```c
if (adc_value > 2480)
    HAL_GPIO_WritePin(GPIOA, GPIO_PIN_1, GPIO_PIN_SET);  // Relay ON
else
    HAL_GPIO_WritePin(GPIOA, GPIO_PIN_1, GPIO_PIN_RESET);  // Relay OFF
