# Awesome CPU Design & Architecture 🚀

*Read this in other languages: [English](README.md) | [Türkçe](README-tr.md)*

A curated list of royalty-free, completely free, and open-source (CC/BSD/Apache/MIT) resources for learning CPU design, microarchitecture, and digital logic circuits. This repository focuses specifically on open standards like **RISC-V** and **OpenRISC**, offering a learning journey from logic gates to operating system-capable cores.

[![Awesome](https://awesome.re/badge.svg)](https://awesome.re)

## Contents
- [Recommended Learning Path](#recommended-learning-path)
- [1. ISA Specifications (Open Standard, Free)](#1-isa-specifications-open-standard-free)
- [2. University Course Materials (Video + Slides)](#2-university-course-materials-video--slides)
- [3. Free Courses and Certified Programs](#3-free-courses-and-certified-programs)
- [4. Open Source Processor Cores (RTL)](#4-open-source-processor-cores-rtl)
- [5. Simulators and Toolchains](#5-simulators-and-toolchains)
- [6. Free / Open Access Books](#6-free--open-access-books)
- [Contributing](#contributing)

---

## Recommended Learning Path

By following the order below, you can follow a completely royalty-free/open-source path from scratch:

1. **Lay the Foundations:** Read RISC‑V and OpenRISC ISA documents to learn basic instruction set formats, addressing modes, and architectural principles.
2. **Examine the Architecture:** Understand the microarchitecture (datapath + control) by examining HDL (Hardware Description Language) codes of OpenRISC OR1200 and simple RISC‑V cores.
3. **Design Your Own:** Design and simulate your own small core using step-by-step guides like single-cycle RISC‑V processor design.
4. **Consolidate Concepts:** Reinforce logic circuit and bus concepts with educational processor projects and Von Neumann / Logisim documents.

---

## 1. ISA Specifications (Open Standard, Free)

Instruction Set Architecture (ISA) is the bridge between hardware and software.

- [RISC-V ISA Manual](https://riscv.org/technical/specifications/) / [GitHub Repository](https://github.com/riscv/riscv-isa-manual) - CC BY 4.0 licensed, full specification PDFs. Divided into "Unprivileged ISA" and "Privileged Spec".
- [OpenRISC](https://openrisc.io/) - A free and open RISC ISA with DSP features; offers open-source implementations and a software development toolchain.
- [OpenPOWER ISA](https://openpowerfoundation.org/) - Powerful architectural standards governed by the Apache 2.0 license.
- [SPARC / OpenSPARC](https://www.oracle.com/servers/technologies/opensparc.html) - A historical open-source reference (GPL licensed).

## 2. University Course Materials (Video + Slides)

Completely free academic course contents shared by top universities:

- [Onur Mutlu – ETH Zürich / CMU](https://people.inf.ethz.ch/omutlu/) - A massive video archive (2013-2025) of *Digital Design & Computer Architecture* (Undergrad) and *Computer Architecture* (Graduate) courses. Full playlists are available on YouTube.
- [UC Berkeley CS61C ("Great Ideas in Computer Architecture")](https://cs61c.org/) - The iconic course focusing on RISC-V architecture, covering hardware, architecture, assembly, and software tools.
- [MIT 6.004 / 6.191 / 6.175 (Constructive Computer Architecture)](https://ocw.mit.edu/) - Legendary MIT materials featuring basic RISC-V processor design, multi-cycle, and 2-stage pipeline labs (CC BY-NC-SA).
- [CMU 18-447 Computer Architecture](https://www.youtube.com/channel/UCR1iaH4WEEHkEMB22kEbbqQ) - Carnegie Mellon's computer architecture YouTube channel.
- [nand2tetris](https://www.nand2tetris.org/) - An amazing project where you build a computer from scratch, starting from logic gates (NAND), to processor, compiler, OS, and finally the game Tetris.

## 3. Free Courses and Certified Programs

- [Linux Foundation LFD111x: Building a RISC-V CPU Core](https://training.linuxfoundation.org/training/building-a-risc-v-cpu-core-lfd111x/) - A great free course on edX that teaches design from digital logic gates to a RISC-V CPU core using the Makerchip IDE.
- [RISC-V International Training](https://riscv.org/community/training/) - Browser-based RISC-V CPU building courses using modern tools.
- [riscv/learn (GitHub)](https://github.com/riscv/learn) - A massive official community "awesome list" covering RISC-V microarchitecture design, OS development, and IM architecture basics.

## 4. Open Source Processor Cores (RTL)

Suitable core codes (MIT/Apache/BSD) for reviewing, simulating, and deriving in your own projects:

- [PicoRV32](https://github.com/YosysHQ/picorv32) - A highly size-optimized, popular RISC-V (RV32IMC) core.
- [SERV](https://github.com/olofk/serv) - The world's smallest RISC-V core. Features an interesting "bit-serial" design.
- [Rocket Chip / Chipyard (Berkeley)](https://github.com/ucb-bar/rocket-chip) - An advanced environment for producing SoCs and custom accelerators using Chisel HDL.
- [OpenRISC OR1200](https://github.com/openrisc/or1200) - A GNU LGPL licensed project written in Verilog HDL where you can examine pipeline, ALU, and exception logic.
- [CORE-V CVA6](https://github.com/openhwgroup/cva6) - An industry-standard, Linux-boot capable open-source RV64GC processor core.
- [mikeroyal/RISC-V-Guide](https://github.com/mikeroyal/RISC-V-Guide) - Another massive guide listing hundreds of tools like Ripes, Renode, Unicorn.

## 5. Simulators and Toolchains

- [Ripes](https://github.com/mortbopet/Ripes) - A fantastic graphical (GUI) RISC-V pipeline simulator. You can visually see how instructions advance through the processor.
- [Spike (riscv-isa-sim)](https://github.com/riscv-software-src/riscv-isa-sim) - The original and official ISA simulator.
- [QEMU](https://www.qemu.org/) - The legendary system emulator supporting architectures like RISC-V, ARM, etc.
- **Open Source EDA Tools:** [Verilator](https://www.veripool.org/verilator/), [Icarus Verilog](https://steveicarus.github.io/iverilog/), [Yosys](https://yosyshq.net/yosys/), and [nextpnr](https://github.com/YosysHQ/nextpnr) for synthesis, placement, and simulation.
- [Logisim-Evolution](https://github.com/logisim-evolution/logisim-evolution) - A great tool where you can visually draw and simulate your circuit from the gate level.

## 6. Free / Open Access Books

- **Guide to Computer Processor Architecture: A RISC-V Approach (Goossens):** An academic work published via Springer, with some open-access chapters available.
- **Academic Archives (arXiv, etc.):** PDFs providing extensive information on the toolchain and ecosystem, searchable with keywords like "RISC-V Education", "RISC-V Software Ecosystem".
- *Reference Note:* The book "Computer Organization and Design: RISC-V Edition (Patterson & Hennessy)" is a fundamental building block but is copyrighted. PDFs are not shared; access via academic libraries is recommended.

---

## Contributing
You can help us grow this list! To add a new resource:
1. Add just the link and a short 1-2 sentence description.
2. Avoid directly copying copyrighted content.
3. Make sure the repository/resource you add has an open license (CC/BSD/Apache/MIT, etc.).
