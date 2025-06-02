# 🌞 LDR-Controlled LED with Relay Activation using STM32

This project demonstrates an **LDR (Light Dependent Resistor) based LED and Relay Control System** using an STM32 microcontroller programmed in **STM32CubeIDE**. Based on the ambient light level, the microcontroller turns an LED and a relay ON or OFF.

## 📌 Overview

- **Microcontroller:** STM32 (e.g., STM32F103C8T6 Blue Pill)  
- **Software:** STM32CubeIDE  
- **Sensor:** LDR for ambient light detection  
- **Output:** LED and Relay module  
- **Simulation:** Not used (hardware-based only)

## ⚙️ Features

- Reads analog voltage from an LDR via ADC  
- Controls an LED and a relay based on a threshold  
- Fully configured in STM32CubeIDE using HAL drivers  
- Energy efficient: activates outputs only in low light  

## 🧰 Components Required

| Component                      | Quantity |
|-------------------------------|----------|
| STM32 Board (e.g., Blue Pill) | 1        |
| LDR + 10kΩ Resistor           | 1        |
| LED + 220Ω Resistor           | 1        |
| Relay Module (5V)             | 1        |
| Breadboard & Jumper Wires     | As needed |
| USB or 5V Power Supply        | 1        |

## 🔌 Circuit Description

- **LDR voltage divider output** → `PA1` (ADC input)  
- **LED** → `PA5` (GPIO output)  
- **Relay IN pin** → `PA6` (GPIO output)  

```
[3.3V] --- [LDR] ---+--- [10kΩ] --- GND
                   |
                ADC (PA1)

PA5 → LED → 220Ω → GND  
PA6 → Relay IN
```

## 🛠️ STM32CubeIDE Configuration

1. Enable **ADC1** on pin `PA1`  
   - Channel: IN1  
   - Resolution: 12-bit  

2. Enable **GPIO Output** for `PA5` (LED) and `PA6` (Relay)  
3. Generate code using **STM32CubeMX**  
4. Write logic in `main.c` inside the while loop  

## 💻 Code Logic (main loop)

```c
#define THRESHOLD 2000 // Adjust based on lighting conditions

while (1)
{
    HAL_ADC_Start(&hadc1);
    HAL_ADC_PollForConversion(&hadc1, HAL_MAX_DELAY);
    uint32_t adc_value = HAL_ADC_GetValue(&hadc1);

    if (adc_value < THRESHOLD)
    {
        HAL_GPIO_WritePin(GPIOA, GPIO_PIN_5, GPIO_PIN_SET);   // LED ON
        HAL_GPIO_WritePin(GPIOA, GPIO_PIN_6, GPIO_PIN_SET);   // Relay ON
    }
    else
    {
        HAL_GPIO_WritePin(GPIOA, GPIO_PIN_5, GPIO_PIN_RESET); // LED OFF
        HAL_GPIO_WritePin(GPIOA, GPIO_PIN_6, GPIO_PIN_RESET); // Relay OFF
    }

    HAL_Delay(100); // Debounce delay
}
```

> 🔧 Use `UART` or `printf` to monitor ADC values and choose an optimal threshold.

## 🧪 Testing Instructions

1. Flash the code to your STM32 board via STM32CubeIDE  
2. Power the board via USB  
3. Adjust light over the LDR  
4. Observe the LED and relay toggle according to brightness  

## 📁 Folder Structure

```
LDR_LED_Relay_STM32/
├── Core/
│   ├── Inc/
│   └── Src/
│       └── main.c
├── Drivers/
├── .project
├── .cproject
├── README.md
```

## ✅ Possible Improvements

- Use PWM dimming instead of digital ON/OFF  
- Integrate UART or LCD display for live readings  
- Add FreeRTOS for multitasking control  

## 📄 License

MIT License — Feel free to use, modify, and distribute!


