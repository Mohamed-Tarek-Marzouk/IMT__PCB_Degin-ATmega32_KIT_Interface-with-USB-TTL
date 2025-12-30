# 🔧 ATmega32 Development & Programming Board (PCB Design)

![Project Type](https://img.shields.io/badge/Project-PCB_Design-green)
![Layers](https://img.shields.io/badge/Layers-2--Layer_PCB-blue)
![MCU](https://img.shields.io/badge/MCU-ATmega32-red)

## 📌 Overview
This project features a **2-layer PCB design** tailored for the **ATmega32** microcontroller. It is specifically engineered to interface with a **USB to TTL module**, enabling seamless programming, debugging, and testing through a simple USB connection.

The board provides a stable environment for the ATmega32, making it ideal for both prototyping and standalone application deployment.

---

## 🎯 Main Features

* **Microcontroller:** Optimized for the ATmega32 (40-pin DIP).
* **USB Interface:** Dedicated 1x5 pin header for easy connection to any USB-to-TTL converter.
* **Programming:** Allows direct code burning and serial communication via UART.
* **Standalone Operation:** Designed to run independently using an external power source once the code is uploaded.

---

## ⚙️ Technical Specifications

### 🔌 Power Management
* **Voltage Regulation:** Includes a **7805 voltage regulator** to protect the MCU from input voltages higher than 5V.
* **Safety:** Ensures a stable 5V logic supply regardless of external fluctuations.
* **Indicator:** A dedicated **Power LED** provides immediate visual confirmation that the system is energized.

### ⏱ Clock & Timing
* **Crystal Oscillator:** Equipped with a **16 MHz crystal** for high-speed, accurate timing.
* **Stability:** Features dual decoupling capacitors to stabilize the clock signal and reduce jitter.

### 💡 Testing & Diagnostics
* **On-board LEDs:** 3 test LEDs are hardwired to **Port D (Pins 2, 3, and 4)**. 
* **Purpose:** These allow for instant "Blink" tests or status indications without needing external breadboarding.

---

## 🔄 Connectivity & I/O

| Interface | Connector Type | Description |
| :--- | :--- | :--- |
| **I/O Ports** | 4 x 8-pin Sockets | Full access to Port A, Port B, Port C, and Port D. |
| **Programming** | 1 x 5-pin Header | RX, TX, VCC, GND, and RESET interface. |
| **Oscillator** | Crystal + Caps | 16 MHz System Clock circuit. |

---

## 🛠 How to Use

1.  **Connection:** Connect your USB-to-TTL module to the 5-pin programming header (Cross-connect RX to TX and TX to RX).
2.  **Powering:** Apply power through the regulator input or via the USB module (ensure voltage jumper settings match).
3.  **Programming:** Use your preferred ISP or UART bootloader software to flash the `.hex` file.
4.  **Testing:** Utilize the integrated LEDs on Port D to verify that your code is executing correctly.

---

## 📝 Design Notes
> [!NOTE]  
> The 2-layer layout includes a dedicated ground plane to minimize noise and improve signal integrity for the 16 MHz clock. Ensure a proper heatsink is used on the 7805 regulator if the input voltage significantly exceeds 7V.
