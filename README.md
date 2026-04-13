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

pcie-ddr-soc-uvm/
│
├── README.md
├── LICENSE
├── .gitignore
│
├── docs/
│   ├── architecture/
│   │   ├── soc_block_diagram.png
│   │   ├── pcie_flow.png
│   │   └── ddr_controller.png
│   ├── specifications/
│   │   ├── pcie_protocol.md
│   │   ├── axi_protocol.md
│   │   └── ddr_timing.md
│   └── reports/
│       ├── verification_report.pdf
│       └── performance_analysis.pdf
│
├── rtl/
│   ├── top/
│   │   └── soc_top.v
│   │
│   ├── pcie/
│   │   ├── pcie_top.v
│   │   ├── tlp_handler.v
│   │   ├── dll_layer.v
│   │   └── flow_control.v
│   │
│   ├── dma/
│   │   ├── dma_engine.v
│   │   ├── dma_scheduler.v
│   │   └── dma_fsm.v
│   │
│   ├── ddr/
│   │   ├── ddr_controller.v
│   │   ├── refresh_logic.v
│   │   └── timing_ctrl.v
│   │
│   ├── axi/
│   │   ├── axi_interconnect.v
│   │   ├── axi_master.v
│   │   └── axi_slave.v
│   │
│   └── common/
│       ├── fifo.v
│       ├── arbiter.v
│       └── registers.v
│
├── verification/
│   ├── tb/
│   │   └── tb_top.sv
│   │
│   ├── uvm_env/
│   │   ├── env.sv
│   │   ├── config.sv
│   │   └── virtual_sequencer.sv
│   │
│   ├── agents/
│   │   ├── pcie_agent/
│   │   │   ├── pcie_driver.sv
│   │   │   ├── pcie_monitor.sv
│   │   │   └── pcie_seq_item.sv
│   │   │
│   │   ├── axi_agent/
│   │   └── ddr_agent/
│   │
│   ├── scoreboard/
│   │   └── soc_scoreboard.sv
│   │
│   ├── sequences/
│   │   ├── base_sequence.sv
│   │   ├── pcie_rw_sequence.sv
│   │   └── stress_sequence.sv
│   │
│   ├── tests/
│   │   ├── base_test.sv
│   │   ├── sanity_test.sv
│   │   └── stress_test.sv
│   │
│   └── coverage/
│       ├── functional_coverage.sv
│       └── protocol_coverage.sv
│
├── sim/
│   ├── run.do
│   ├── compile.sh
│   └── run_sim.sh
│
├── scripts/
│   ├── compile.tcl
│   ├── run_regression.py
│   └── waveform_setup.tcl
│
├── models/
│   ├── memory_model.sv
│   └── pcie_reference_model.py
│
├── results/
│   ├── waveforms/
│   ├── logs/
│   └── coverage/
│
└── ci/
    └── regression.yml
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

