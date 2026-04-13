## High-Speed PCIe + DDR SoC Subsystem with UVM Verification

## 📌 Description

This project involves the design and verification of a **high-performance SoC subsystem** integrating **PCIe interface, DMA engine, and DDR memory controller**. The system is built using an **AXI interconnect**, enabling high-speed data transfer between subsystems.

A configurable **DMA engine** supports efficient data movement between PCIe and memory, including burst and scatter-gather transactions. The design is verified using a **full UVM-based verification environment**, ensuring protocol compliance and data integrity.

The project emphasizes **industry-level verification methodologies**, including assertions, functional coverage, and stress testing.

---

## 🎯 Objectives

* Design high-speed SoC subsystem
* Implement PCIe, DDR, and DMA modules
* Develop full UVM verification environment
* Validate system under stress and corner cases

---

## 🏗️ Architecture

* PCIe Endpoint Controller
* DMA Engine
* DDR Memory Controller
* AXI Interconnect
* Memory Model

---

## ⚙️ Tools & Technologies

* Verilog / SystemVerilog
* UVM (Universal Verification Methodology)
* VCS / QuestaSim
* GTKWave
* Python / TCL

---

## 📁 Project Structure

```
rtl/
  pcie/
  dma/
  ddr/
  axi/
verification/
  uvm_env/
  agents/
  scoreboard/
scripts/
docs/
```

---

## 🚀 Features

* High-speed data transfer architecture
* Protocol-based design (PCIe, AXI, DDR)
* Full UVM verification flow
* Assertion-based validation

---

## 📊 Results

* Verified end-to-end data integrity
* Achieved high throughput under load
* Comprehensive protocol coverage

