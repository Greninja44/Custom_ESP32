# 📘 Custom ESP32-WROOM-32E Development Board

This is a custom-designed development board built around the powerful **ESP32-WROOM-32E** module, offering robust wireless capabilities (Wi-Fi + Bluetooth), full GPIO access, and convenient USB-C programming. The board is engineered to be compact, reliable, and suitable for both prototyping and production use in IoT, embedded systems, and automation applications.

---

## 🔍 Overview

The board is based on the **ESP32-WROOM-32E** (8MB flash), an industry-leading microcontroller module from Espressif, and integrates essential components for smooth development and deployment:

- **USB-to-Serial programming** via CP2102N
- **Power regulation** using AMS1117-3.3 for stable 3.3V output
- **Dual GPIO header rows** for complete access to all ESP32 I/O pins
- **Dedicated EN (reset)** and **IO0 (boot/user)** push buttons
- **Status LEDs** for power indication and user interaction
- **USB Type-C connector** for modern and reversible connectivity
- **Support for external 5V power input** via jumper selection

---

## 🧠 Key Features

| Feature               | Description                                                    |
|------------------------|----------------------------------------------------------------|
| **ESP32 Module**       | ESP32-WROOM-32E with 8MB flash, Wi-Fi & Bluetooth               |
| **USB Interface**      | CP2102N USB to UART with auto-reset and bootloader support     |
| **Voltage Regulator**  | AMS1117-3.3 for stable onboard 3.3V power                      |
| **Programming Port**   | USB Type-C for power and flashing                              |
| **Power Inputs**       | USB-C VBUS and External 5V (selectable via jumper)             |
| **Buttons**            | EN (reset) and IO0 (boot/user) push buttons                    |
| **LED Indicators**     | Power LED and user LED (connected to IO2)                      |
| **ESD Protection**     | USB data lines protected for reliable long-term use            |
| **Connectivity**       | 2x 17-pin headers exposing all GPIOs, ADCs, and input-only pins|

---

## 🔌 Power Supply Options

The board supports two power input methods:

- **USB Type-C (VBUS)**: Powers the board directly from the host.
- **External 5V Header (J4)**: Provides an alternative supply for standalone use.

Power selection is handled via the **J5 jumper**:
- Connect to `VBUS` for USB power.
- Connect to `+5V_EXT` for external input.

All power inputs are regulated down to **3.3V** using the AMS1117 linear regulator.

---

## 📐 GPIO Access & Pinout

This board provides full access to the ESP32's GPIOs:

| Pin Range    | Notes                        |
|--------------|------------------------------|
| IO0 – IO39   | All I/O pins exposed         |
| IO34–IO39    | Input-only (no output)       |
| IO32–IO33    | ADC capable                  |
| IO12–IO15    | Use with caution during boot |
| TXD0/RXD0    | Default UART0 (USB serial)   |
| IO2          | Connected to User LED        |

Pins are arranged in two 17-pin headers (`J1`, `J2`) to facilitate breadboard or jumper-wire connections.

---

## 🔧 USB to Serial Interface

The onboard **CP2102N-A02** USB to UART bridge enables seamless programming and debugging:

- Auto-reset and auto-bootloader mode via RTS and DTR lines
- Standard USB data lines (`USB_DP`, `USB_DN`)
- USB ESD protection components for durability
- Exposed serial pins: `TXD`, `RXD`, `DTR`, `RTS`

---

## 🧩 Board Layout & Connectors

| Connector | Function                            |
|-----------|-------------------------------------|
| J1, J2    | Dual 17-pin headers for all GPIOs   |
| J4        | 3-pin external power header (+5V)   |
| J5        | Power source selection jumper       |
| USB-C     | Power + USB-to-Serial communication |

---

## 📄 Repository Contents

- `Schematic.pdf` — Full circuit schematic
- `PCB_PCB_esp32_custom_2025-05-22.json` — PCB layout file (EasyEDA)
- `README.md` — Board documentation
- `BOM.csv` & `PickAndPlace.csv` 

---
## PCB 
![Screenshot 2025-05-22 005807](https://github.com/user-attachments/assets/b27c88e1-da5e-4473-9053-b903e551bcbe)

## 3D MODEL



![2025-05-2201-01-48-ezgif com-video-to-gif-converter](https://github.com/user-attachments/assets/1f09d577-f04e-4eee-82bb-5773d4afa8bc)



## 📝 License

This project is released under the [MIT License](LICENSE).

---

> For feedback, improvements, or contributions, feel free to open an issue or pull request.
