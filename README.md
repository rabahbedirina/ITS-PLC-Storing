# ITS PLC Storing & Sorting System (`ITSPLCMHJSTORING`)

An industrial automation and simulation project designed for the **ITS PLC MHJ Edition** 3D plant simulation environment, controlled using Siemens SIMATIC STEP 7 (S7 Classic) / WinSPS-S7.

## 🎥 Demonstration Video
This repository is based on and corresponds to the setup demonstrated in the following YouTube video:
* [ITS PLC Sorting System | Tri de Caisses](https://www.youtube.com/watch?v=Do_Fvs9n41s)

---

## 🏗️ Project Overview
The **ITS-PLC-Storing** repository contains a complete STEP 7 project layout structured to control a virtual 3D sorting and storing conveyor system. It handles inputs from optical sensors, proximity switches, and controls actuators like pneumatic pushers and diverters.

### Key Components:
- **PLC Program Blocks:** Contains Organization Block statement list source code (`OB1.AWL`) and compiled machine code blocks (`OB1.MC7`, `FB1.MC7`) targeted for Siemens S7-300 controllers.
- **Hardware Configuration:** Network and hardware description files (`S7Netze.hdw`, `Hardwareconfig_ws7_Offline.wld`) matching the virtual machine setup.
- **Symbol & Variable Tables:** Includes mapping files (`SymbolTable.SEQ`, `TableOfVariables.var`, `Symbolic_File.ASC`) to correlate tags with the 3D model.
- **Diagnostic Protocols:** A collection of historical system and execution logs (`.prot`) contained within the `Protocol` directory.

---

## 🛠️ Software Requirements & Tools
To open, run, or modify this project, you will need:
1. **Siemens SIMATIC STEP 7 (v5.x)** or **WinSPS-S7** (with built-in S7-300 simulation).
2. **ITS PLC MHJ Edition** (3D Industrial Plant Simulation Software).

---

## 📂 Repository Directory Structure
```text
ITSPLCMHJSTORING/
├── OFFLINE/        # Offline program block source files (e.g., OB1.AWL)
├── ONLINE/         # Online/compiled block data (e.g., FB1.MC7, OB1.MC7)
├── HDW1_4/         # Hardware configuration and network files
├── Protocol/       # Diagnostic logs and runtime protocol files
├── S7P/            # STEP 7 internal project databases and metadata
└── README.md       # Project documentation
```

---

## 🚀 Getting Started
1. Clone or download this repository onto your local machine.
2. Open **WinSPS-S7** or **Siemens STEP 7** and load the `ITSPLCMHJSTORING` project.
3. Start the **ITS PLC MHJ** 3D sorting scene simulator.
4. Establish the communication link between the simulator and the PLC environment, then monitor `OB1` to test the automated sorting and storing routines.