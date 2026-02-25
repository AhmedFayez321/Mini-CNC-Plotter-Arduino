# ✍️ Custom Mini CNC Plotter (GRBL + Arduino Nano)

A fully custom-built Mini CNC Plotter utilizing **GRBL firmware** and **Universal Gcode Sender (UGS)**. Unlike standard builds that use off-the-shelf CNC shields, this project features a **custom-designed PCB** using ULN2003 drivers to control three 5V stepper motors.

## 🌟 Key Achievements & Technical Highlights

* **Custom Hardware Design:** Designed a dedicated PCB around the **Arduino Nano** and three **ULN2003** driver ICs, complete with an **XL4015 Step-Down converter** for stable 5V power delivery.
* **Firmware Adaptation:** Successfully integrated standard GRBL firmware to operate with unipolar 5V stepper motors (28BYJ-48), bypassing the need for standard Step/Dir drivers (like A4988).
* **Precise Calibration:** Manually calibrated the `steps/mm` parameters in GRBL using physical ruler measurements to ensure high plotting accuracy.
* **Cable Management:** The custom PCB design allowed for clean cable routing. Each stepper motor's wiring is isolated and neatly organized via 5-pin headers, preventing wire tangling during plotting.

## 🛠️ Hardware Architecture (BOM)

| Component | Quantity | Description |
| :--- | :---: | :--- |
| **Arduino Nano** | 1 | Core controller running GRBL. |
| **ULN2003 IC** | 3 | Motor drivers for X, Y, and Z axes. |
| **28BYJ-48 Stepper**| 3 | 5V Unipolar Stepper Motors. |
| **XL4015 Module** | 1 | Buck converter for robust 5V power supply. |
| **Capacitors** | 4 | 3x 100nF (Decoupling) & 1x 100uF (Smoothing). |
| **Custom PCB** | 1 | Designed for efficient wire routing and compactness. |

## 📂 Repository Structure
* `/Firmware`: Contains the modified GRBL source code flashed to the Arduino.
* `/Hardware`: Includes the KiCad/Eagle schematic (`.png`) and custom PCB design files.
* `/G-Code-Samples`: Sample `.gcode` files tested on this machine.
* `/Media`: Photos of the assembled machine and drawing videos.

## 🚀 How It Works
1. Create or download a vector graphic (SVG).
2. Generate G-code using software like Inkscape.
3. Connect the Arduino Nano to the PC via USB.
4. Open **Universal Gcode Sender (UGS)**, connect to the correct COM port (Baud rate: 115200).
5. Load the G-code file, set the zero position, and start plotting!

---
### 👨‍💻 Developed by:
**Ahmed Fayez** *AI & Robotics Student*
