# Arduino Timer Interrupt Project Using Timer1

[![Arduino](https://img.shields.io/badge/Arduino--UNO-Blue?style=for-the-badge)](https://store.arduino.cc/products/arduino-uno-rev3) [![Language: Embedded C++](https://img.shields.io/badge/Language-EmbeddedC++-orange?style=for-the-badge)]() [![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg?style=for-the-badge)](https://opensource.org/licenses/MIT)

This project demonstrates how to use **Timer1 Overflow Interrupt** in **Arduino UNO** to toggle an LED using accurate timer-based logic. The preloader value can be changed using push buttons, and the current value is displayed on a **16x2 LCD** display. It replaces the traditional `delay()` method with precise hardware-timer control.

![Arduino Timer Circuit](https://circuitdigest.com/sites/default/files/circuitdiagram_mic/Circuit-Diagram-for-Arduino-Timer.png)

---

## 🚀 Features

- Timer1 overflow-based LED toggle using ISR
- Non-blocking timer logic (no `delay()`)
- Preloader adjustment via push buttons
- Real-time preloader value shown on LCD
- Demonstrates register-level control in Arduino

---

## 🛠️ Hardware Requirements

| Component         | Description                          |
|-------------------|--------------------------------------|
| Arduino UNO       | Main microcontroller board           |
| 16x2 LCD Display  | To show preloader value              |
| LED               | Indicator output on pin 7            |
| Push Buttons (2)  | Increment/decrement timer preload    |
| 10k Resistors (2) | Pull-down resistors for buttons      |
| 2.2k Resistor     | For LED current limiting             |
| Potentiometer     | Contrast control for LCD             |
| Jumper Wires      | Connections                          |
| Breadboard        | Prototyping                          |

---

## ⚙️ Arduino Timers Overview

### Timer0
- 8-bit timer
- Used by functions like `delay()`, `millis()`

### Timer1
- 16-bit timer
- Used in this project for interrupt-based control

### Timer2
- 8-bit timer
- Used in `tone()` function and PWM applications

---

## 🔌 Circuit Connection

| LCD Pin | Arduino UNO Pin                         |
|---------|------------------------------------------|
| VSS     | GND                                      |
| VDD     | +5V                                      |
| V0      | Potentiometer middle pin                 |
| RS      | Pin 8                                    |
| RW      | GND                                      |
| E       | Pin 9                                    |
| D4      | Pin 10                                   |
| D5      | Pin 11                                   |
| D6      | Pin 12                                   |
| D7      | Pin 13                                   |
| A (LED+) | +5V                                     |
| K (LED-) | GND                                     |

**Other Connections:**

- Push Button 1 → Pin 2 (with 10k pull-down)
- Push Button 2 → Pin 4 (with 10k pull-down)
- LED Anode → Pin 7 (via 2.2k resistor)

---

## 🧠 Troubleshooting

| Issue                          | Cause / Solution                                  |
|--------------------------------|---------------------------------------------------|
| LED not blinking               | Check Timer1 ISR and preloader logic              |
| LCD not displaying             | Check wiring, contrast pot, and `lcd.begin()`     |
| Push buttons unresponsive      | Confirm pull-down resistors and pinMode settings  |
| Interrupts not triggering      | Ensure `TIMSK1` and `interrupts()` are set        |

---

## 📱 Applications

- Timer-based LED blinking without delay()
- Time-controlled device switching
- Real-time system clocks
- Multitasking systems
- Accurate PWM-based systems

---

## 🔮 Future Enhancements

- Add buzzer or relay for timed alarms
- EEPROM save/restore of last preloader value
- Serial interface for real-time control
- Debounce filtering on buttons
- Add support for Timer0/Timer2 configurations

---

## 🧪 Technical Specifications

| Parameter          | Value                               |
|--------------------|--------------------------------------|
| Microcontroller    | Arduino UNO (ATmega328P)             |
| Timer Used         | Timer1 (16-bit)                      |
| Timer Mode         | Overflow Interrupt                   |
| Prescaler          | 1024                                 |
| Preloader Value    | Adjustable (default: 3035)           |
| Output             | LED on pin 7                         |
| Input              | Buttons on pin 2 and pin 4           |
| Display            | 16x2 LCD (Pins 8–13)                 |

---

## 🔗 Full Project

- 📖 [Complete Tutorial on Circuit Digest](https://circuitdigest.com/microcontroller-projects/arduino-timer-tutorial)

---

## ⭐ Support

If you found this helpful, please ⭐ star this repository and share it with others!

---

**Built with ⏱️ by [Circuit Digest](https://circuitdigest.com/)**  
_Making Electronics Simple_

---

### 🔖 Keywords

`arduino timer project` `timer1 overflow interrupt` `arduino uno led blink` `lcd timer counter`  
`register level programming` `arduino push button control` `embedded c++ arduino` `precise delay without delay()`  
`timer interrupt tutorial` `arduino real-time timer` `hardware timer programming` `arduino timer example`
