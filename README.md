# 🚀 High-Speed PCIe + DDR SoC Subsystem with UVM Verification

---

## 📌 Overview

This project presents the design and verification of a **high-performance SoC subsystem** integrating a **PCIe interface, DMA engine, and DDR memory controller** interconnected via an **AXI-based architecture**.

The system is designed to support **high-throughput data transfer** between external interfaces and memory, and is verified using a **complete industry-standard UVM verification environment**.

This project demonstrates **end-to-end SoC design + protocol-level verification**, aligned with real-world semiconductor workflows.

---

## 🎯 Objectives

* Design a scalable **SoC subsystem architecture**
* Implement **PCIe endpoint controller**
* Develop **high-performance DMA engine**
* Design **DDR memory controller with burst support**
* Integrate modules using **AXI interconnect**
* Build **UVM-based verification environment**
* Ensure **protocol compliance and data integrity**

---

## 🧠 System Architecture

### 🔹 High-Level Components

* **PCIe Endpoint Controller**
* **DMA Engine (Scatter-Gather capable)**
* **DDR Memory Controller**
* **AXI Interconnect**
* **Memory Model (DRAM simulation)**

---

### 🔹 Data Flow

PCIe Host ⇄ PCIe Controller ⇄ DMA Engine ⇄ AXI Interconnect ⇄ DDR Memory

---

### 🔹 Key Design Features

* High-speed packet-based communication
* Burst-based memory transactions
* Flow control and arbitration
* Scalable and modular architecture

---

## 🏗️ RTL Design

### 🔹 PCIe Controller

* Transaction Layer Packet (TLP) handling
* Completion logic
* Flow control management

### 🔹 DMA Engine

* Memory ↔ PCIe transfers
* Burst transactions
* Scatter-Gather support
* FSM-based control

### 🔹 DDR Controller

* Address mapping
* Timing constraints
* Refresh logic

### 🔹 AXI Interconnect

* Read/Write channels
* Handshake protocols
* Arbitration between masters

---

## 🧪 Verification Methodology (UVM)

### 🔹 Testbench Architecture

* UVM-based hierarchical environment
* Multi-agent verification (PCIe, AXI, DDR)

---

### 🔹 UVM Components

#### ✔ Environment

* Integrates all agents and scoreboard

#### ✔ Agents

* PCIe Agent
* AXI Agent
* DDR Agent

#### ✔ Driver

* Generates protocol-specific transactions

#### ✔ Monitor

* Observes DUT signals and transactions

#### ✔ Scoreboard (Critical)

* End-to-end data integrity checking
* Validates:

  * PCIe → DMA → DDR data path

---

### 🔹 Assertions (SVA)

* AXI handshake correctness
* PCIe packet format validation
* Data consistency checks

---

### 🔹 Functional Coverage

* Protocol states
* Burst sizes
* Error scenarios
* Corner cases

---

## 🧪 Test Scenarios

### 🔹 Basic Tests

* PCIe read/write transactions
* DDR memory access

### 🔹 Integration Tests

* DMA transfers (PCIe ↔ DDR)

### 🔹 Stress Tests

* High-throughput traffic
* Back-to-back transactions

### 🔹 Corner Cases

* Misaligned transfers
* Packet loss / retry
* Timeout conditions

---

## 📊 Performance Metrics

* **Throughput (GB/s)**
* **Latency (cycle-level)**
* **Bandwidth utilization**
* **Error rate under stress**

---

## ⚙️ Tools & Technologies

| Category     | Tools                    |
| ------------ | ------------------------ |
| RTL Design   | Verilog, SystemVerilog   |
| Verification | UVM                      |
| Simulation   | Synopsys VCS / QuestaSim |
| Debug        | GTKWave                  |
| Scripting    | Python, TCL              |
| Modeling     | Python / C++             |

---

## 📁 Project Structure

```id="9pjv9y"
rtl/
  pcie/
  dma/
  ddr/
  axi/

verification/
  uvm_env/
  agents/
  scoreboard/
  sequences/
  tests/

scripts/
models/
docs/
results/
```

---

## 🚀 Features

* High-speed PCIe + DDR integration
* Scalable AXI-based architecture
* Full UVM verification flow
* Assertion-based protocol validation
* Coverage-driven verification
* End-to-end data integrity checking

---

## 📊 Results

* Verified PCIe, AXI, and DDR protocol compliance
* Achieved reliable high-throughput data transfer
* Functional coverage across key scenarios
* Successful stress testing with no data loss

---

## 🔬 Future Enhancements

* PCIe Gen4 / Gen5 support
* Advanced traffic generators
* FPGA prototyping (hardware validation)
* Formal verification integration

---

## 📌 Key Learnings

* SoC integration of high-speed interfaces
* Protocol design (PCIe, AXI, DDR)
* UVM verification methodology
* Assertion-based verification (SVA)
* Debugging complex hardware systems

---

## 🏆 Applications

* Data center accelerators
* High-speed networking systems
* Storage controllers
* AI/ML hardware platforms

