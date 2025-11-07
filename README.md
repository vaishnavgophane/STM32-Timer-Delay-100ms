
This project demonstrates how to configure and use a **hardware timer** in the **STM32 microcontroller** to generate a precise **100 ms delay** without using `HAL_Delay()`. The project was created using **STM32CubeIDE** and simulated in **Proteus**.

---

## 🚀 Project Overview

- **Microcontroller:** STM32F103C6TA
- **Toolchain:** STM32CubeIDE
- **Simulation:** Proteus 8 Professional
- **Delay:** 100 ms (using Timer interrupt or polling)
- **Timer Mode:** Up-counting, internal clock source

The timer is configured using **STM32CubeMX (IOC file)** to generate periodic delays, toggling an LED every 100 ms to verify timing accuracy.

---

## ⚙️ Configuration Details

| Parameter              | Value                |
|------------------------|----------------------|
| Timer used             | TIM1                 |
| Prescaler              | 12                   |
| Counter Period (ARR)   | 61538                |
| Clock Frequency        | 8 MHz (APB2 Timer)   |
| Calculated Delay       | 100 ms               |
| Mode                   | Up-counting          |
| Output                 | LED Toggle (PIN: PA0)|

---

## 🧠 Files Included

| File / Folder | Description |
|----------------|-------------|
| `main.c` | Main source file implementing 100 ms delay using timer |
| `stm32f4xx_it.c` | Interrupt service routine (if interrupt mode used) |
| `.ioc` | STM32CubeMX configuration file |
| `Proteus Simulation.pdsprj` | Proteus simulation schematic |
| `README.md` | This documentation file |

---

## 🧩 How It Works

1. **Timer initialized** in CubeMX with desired prescaler and ARR values.
2. **Timer started** in interrupt or polling mode.
3. **LED toggles** every 100 ms inside the loop(polling Method).
4. **Simulation** in Proteus verifies timing accuracy and working.

---

## 🖥️ Running the Project

1. Open `.ioc` file in **STM32CubeIDE** and generate the code.
2. Build and flash to STM32 board **or**
3. Run **Proteus simulation** using provided `.pdsprj` file.
4. Observe LED toggling every 100 ms.

---

## 🧰 Tools Used

- STM32CubeIDE   
- Proteus 8 Professional  
 

---

## 📚 Learning Outcome

- Understand STM32 timer configuration  
- Learn delay generation without blocking functions  
- Understand prescaler and auto-reload value calculation  
- Integrate hardware timer with Proteus simulation  

---

## 🧑‍💻 Author

**Vaishnav Gophane**  
Embedded Systems Enthusiast | C PROGRAMMING | EMBEDDED C ||STM32 | PIC | CAN | RTOS | LINUX |I2C | SPI | UART |   

---

⭐ *If you found this project useful, consider giving it a star on GitHub!*
