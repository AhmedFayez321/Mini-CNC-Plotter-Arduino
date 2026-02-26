# 📠 Custom Mini CNC PCB Plotter (GRBL + Arduino Nano)

A fully custom-built Mini CNC Plotter designed as a **PCB Fabrication Tool**. This machine bridges the gap between digital design and physical manufacturing by plotting circuit tracks directly onto copper-clad boards for chemical etching.

## 🌟 Manufacturing Workflow (The Process)
Even without visual documentation, the following technical workflow was successfully implemented and tested:
1. **CAM Processing:** Utilized **FlatCAM** running on **Linux WSL** to process Gerber files and generate precise G-code for isolation plotting.
2. **G-Code Streaming:** Used **Universal Gcode Sender (UGS)** to stream the G-code to the Arduino Nano controller.
3. **Hardware Execution:** The machine uses a marker to draw the circuit layout on copper. This act as an etch-resist layer.
4. **Chemical Etching:** The plotted board is then processed in a chemical acid bath to remove unwanted copper, leaving the final circuit tracks intact.

## 🚀 Technical Highlights
* **Custom Control Board:** Designed a dedicated PCB around the **Arduino Nano** and **ULN2003** drivers for 3-axis control.
* **Firmware Adaptation:** Modified **GRBL** to work with 5V unipolar stepper motors (28BYJ-48).
* **Precise Calibration:** Achieved high accuracy by manually calibrating `steps/mm` using physical measurements.
* **Neat Cable Management:** Integrated all wiring into a custom PCB with 5-pin headers for a tangle-free operation.

## 🛠️ Bill of Materials (BOM)
| Component | Quantity | Description |
| :--- | :---: | :--- |
| **Arduino Nano** | 1 | Main Controller (GRBL) |
| **ULN2003 IC** | 3 | Stepper Drivers |
| **5V Stepper** | 3 | Axis Motors |
| **XL4015 Module** | 1 | 5V Power Regulator |
| **Custom PCB** | 1 | Main Control Board |

## 📂 Repository Structure
* `/Firmware`: Modified GRBL source code.
* `/Hardware`: Schematics and PCB design files.
* `/Software`: Documentation on **FlatCAM (WSL)** setup and **UGS** configurations.
* `/G-Code-Samples`: Sample files generated for PCB tracks.

---
### 👨‍💻 Developed by:
**Ahmed Fayez** *AI & Robotics Student*
