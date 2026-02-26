# Software Setup & Workflow

### 1. FlatCAM on Linux WSL
To achieve high-precision PCB G-code generation, I used **FlatCAM** on **Linux (Windows Subsystem for Linux - WSL)**. 
* **Reason:** FlatCAM provides advanced tools for isolation routing and PCB geometry that are more stable in a Linux environment.
* **Task:** Converting Gerber files (from KiCad/EasyEDA) into G-code compatible with GRBL.

### 2. Universal Gcode Sender (UGS)
* **Function:** Used as the interface between the PC and the CNC machine.
* **Config:** Baud rate set to `115200`. 
* **Calibration:** I used the console to fine-tune `$100`, `$101`, and `$102` settings for exact mm movement.

### 3. Workflow Summary
Digital Design (Gerber) -> FlatCAM (Linux WSL) -> G-code -> UGS -> Mini CNC Plotter -> Chemical Etching.
