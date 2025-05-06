# 🔬 Custom 8×8 6T SRAM Memory | VLSI Final Project 🧠⚙️

This repository showcases a full-custom **8×8 Static Random-Access Memory (SRAM)** project designed using **Cadence Virtuoso**. It was developed as part of the **Introduction to VLSI Design** course at **Braude Academic College of Engineering**.

> We designed and simulated the entire SRAM system from scratch — using CMOS logic gates, creating custom layouts, building control logic, and verifying full functionality through transient simulations.

---

## 📦 Project Components

- ✅ Custom CMOS logic gates: INV, NAND2, NOR2, AND4
- ✅ 3-to-8 row decoder for wordline activation
- ✅ 6-transistor (6T) SRAM cell
- ✅ Integrated 8×8 array layout with read/write logic
- ✅ Functional and timing simulations (Spectre)

---

## 🧠 System Architecture

The design consists of **64 SRAM cells** (6T architecture) arranged in an 8×8 matrix, activated by a **3-to-8 decoder**, and interfaced with **write-enable** and **data-in** signals.

### Key Signals:
- `WR`: Toggles read/write mode
- `DataIn`: Input data for write
- `Bitlines`: Carry data in/out
- `Wordlines`: Activated via decoder

---

## 🧰 Design Stages

### 1️⃣ CMOS Logic Gates  
- Built using custom transistor-level design  
- Simulated individually for correctness and timing

### 2️⃣ Row Decoder  
- 3-to-8 decoder activates a single row  
- Verified for proper one-hot output and minimal delay

### 3️⃣ 6T SRAM Cell  
- Designed for static noise margin stability  
- Simulated under both read and write conditions

### 4️⃣ Memory Array  
- 64 cells tiled into an 8×8 grid  
- Bitlines vertically shared, wordlines horizontally routed

### 5️⃣ Read/Write Control  
- Verified full functionality using transient simulations  
- Timing diagrams confirm proper access behavior

---

## 📈 Performance Summary

| Feature              | Value                  |
|---------------------|------------------------|
| Cell Type           | 6T CMOS                |
| Total Bits          | 64 (8×8 array)         |
| Max Frequency       | 1.58 GHz (simulated)   |
| Layout Area         | 240 µm × 315 µm        |
| Validation          | DRC, LVS, Spectre Sim  |

---

## 🖼️ Project Snapshots

### 🧩 Block Diagram
<img src="docs/System Block Diagram Scematic.png" width="600"/>

### 🧱 Layout Samples
<img src="layout/8×8 SRAM Array Layout1.png" width="600"/>
<img src="layout/Complete 8×8 SRAM System Layout.png" width="600"/>

### 🌊 Simulation Results
<img src="docs/Transient Simulations.png" width="600"/>
<img src="simulations/SRAM Read_Write Simulation Graph.png" width="600"/>

---

## 📂 Folder Structure

```plaintext
.
├── README.md                  → Project overview and design notes
├── LICENSE                    → MIT License
├── docs/                      → Block diagrams, PDF reports, waveforms
├── schematics/                → Custom logic schematics
├── layout/                    → Layout previews of gates, cells, arrays
├── simulations/               → Spectre results and waveform graphs
