# 🚀 High-Speed PCIe + DDR SoC Subsystem with UVM Verification

---
![Status](https://img.shields.io/badge/Status-In%20Progress-yellow)
![Language](https://img.shields.io/badge/HDL-Verilog%20%7C%20SystemVerilog-blue)
![Verification](https://img.shields.io/badge/Verification-UVM-green)
![Flow](https://img.shields.io/badge/Flow-RTL--to--GDSII-orange)

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
| Simulation   |QuestaSim                 |
| Debug        | GTKWave                  |
| Scripting    | Python, TCL              |
| Modeling     | Python & C++             |

---

## 📁 Project Structure

```

pcie-ddr-soc-uvm/
├── README.md
├── LICENSE
├── .gitignore
├── Makefile

├── docs/
│   ├── architecture/
│   │   ├── soc_block_diagram.png
│   │   ├── data_flow.png
│   │   ├── pcie_layers.png
│   │   └── axi_ddr_integration.png
│   ├── specifications/
│   │   ├── pcie_protocol.md
│   │   └── axi_protocol.md
│   └── reports/
│       ├── design_constraints.md
│       ├── verification_plan.md
│       ├── coverage_report.md
│       ├── bug_tracker.md
│       └── performance_report.md

├── rtl/
│   ├── top/
│   │   ├── soc_top.v
│   │   ├── pcie_top.v
│   │   └── soc_config.vh
│   ├── pcie/
│   │   ├── pcie_tlp_engine.v
│   │   ├── pcie_rx.v
│   │   ├── pcie_tx.v
│   │   ├── pcie_flow_ctrl.v
│   │   └── pcie_config_space.v
│   ├── dma/
│   │   ├── dma_engine.v
│   │   ├── dma_scheduler.v
│   │   ├── dma_fsm.v
│   │   └── dma_descriptor.v
│   ├── ddr/
│   │   ├── ddr_controller.v
│   │   ├── ddr_cmd_scheduler.v
│   │   ├── ddr_buffer.v
│   │   ├── ddr_refresh.v
│   │   └── ddr_timing_ctrl.v
│   ├── axi/
│   │   ├── axi_interconnect.v
│   │   ├── axi_arbiter.v
│   │   ├── axi_master_if.v
│   │   └── axi_slave_if.v
│   └── common/
│       ├── fifo.v
│       ├── sync_fifo.v
│       ├── register_file.v
│       └── reset_sync.v

├── verification/
│   ├── tb/
│   │   ├── tb_top.sv
│   │   ├── tb_pkg.sv
│   │   └── tb_config.sv
│   ├── uvm_env/
│   │   ├── env.sv
│   │   ├── env_pkg.sv
│   │   ├── config.sv
│   │   └── virtual_sequencer.sv
│   ├── agents/
│   │   ├── pcie_agent/
│   │   ├── axi_agent/
│   │   └── ddr_agent/
│   ├── scoreboard/
│   │   ├── soc_scoreboard.sv
│   │   └── data_checker.sv
│   ├── sequences/
│   │   ├── base_sequence.sv
│   │   ├── pcie_read_seq.sv
│   │   ├── pcie_write_seq.sv
│   │   ├── dma_transfer_seq.sv
│   │   └── stress_seq.sv
│   ├── tests/
│   │   ├── base_test.sv
│   │   ├── sanity_test.sv
│   │   ├── dma_test.sv
│   │   ├── stress_test.sv
│   │   └── error_injection_test.sv
│   ├── coverage/
│   │   ├── functional_cov.sv
│   │   ├── protocol_cov.sv
│   │   └── cross_cov.sv
│   └── assertions/
│       ├── axi_assertions.sv
│       ├── pcie_assertions.sv
│       └── data_integrity_assertions.sv

├── sim/
│   ├── compile.do
│   ├── run.do
│   ├── sim.sh
│   └── run_regression.sh

├── scripts/
│   ├── compile.tcl
│   ├── sim_setup.tcl
│   ├── regression.py
│   ├── coverage_merge.py
│   └── waveform_setup.tcl

├── models/
│   ├── memory_model.sv
│   ├── pcie_ref_model.py
│   ├── traffic_generator.py
│   └── golden_model.cpp

├── results/
│   ├── logs/
│   ├── waveforms/
│   └── coverage/

├── reports/
│   └── regression.yml

├── ci/
│   └── lint.yml

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

