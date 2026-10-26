# Hi there! 👋 I'm Eureka (@huanglian34)

<p align="left">
  <img src="https://komarev.com/ghpvc/?username=huanglian34&label=Profile%20Views&color=0e75b6&style=flat" alt="Profile views" />
</p>

### ⚡ Embedded Power Firmware Engineer | High-Power Topologies & DSP | Systems & Market Dynamics

Embedded digital power software and firmware engineer focused on **high-power conversion topologies**, **discrete control algorithms**, and **cycle-accurate DSP implementation**. Experienced across full-cycle power electronics—from Altium multi-layer PCB design and magnetic modeling down to cycle-exact dsPIC assembly optimization.

Beyond hardware, I systematically research **market microstructure, liquidity, and price action (ICT / Al Brooks)**, alongside low-level system tooling, flash storage architectures, and classical philosophy (**Daoist spontaneous order, I Ching state transitions, and Stoic risk control**).

---

## 🔭 Core Technical Focus

### 🔌 Digital Power Electronics & Control Loops
- **Topologies & Conversion:**
  - **Interleaved PFC (IPFC):** Dual-phase 180° PWM interleaving, dynamic phase shedding, and high-precision current balancing.
  - **Phase-Shifted Full Bridge (PSFB):** Zero Voltage Switching (ZVS) timing optimization, Peak Current Mode (PCM) control, dynamic slope compensation, and Gate Drive Transformer (GDT) networks.
  - **LLC Resonant Converters:** First Harmonic Approximation (FHA) modeling, wide-output regulation, secondary synchronous rectification ($V_{DS}$ sensing & clamping), and primary auxiliary winding (BW) feedback.
- **Control Theory & Loop Architecture:**
  - Fast inner current loop paired with anti-chatter variable PI outer voltage loops (featuring hysteresis and state-holding timers to suppress transient chattering).
  - Practical compensator design: transitioning from complex 2P2Z compensators to computationally lean, easily tunable **first-order IIR filters**.
  - Direct raw ADC sampling counts as control references to ensure deterministic, zero-conversion-overhead execution.

### ⚙️ DSC & Embedded Firmware Engineering
- **Silicon Platforms:**
  - **Microchip dsPIC33CK / dsPIC33CH:** Deep peripheral utilization (High-Speed PWM generators, synchronized ADC cores, DMA controllers, analog comparators).
  - **Espressif ESP32-C3:** DMA pipelines, 4-wire SPI/I2C/parallel display drivers, and GPIO Matrix configuration.
- **Firmware Optimization:**
  - Bare-metal C paired with inline dsPIC assembly for performance-critical inner loops, slope compensation, and cycle-by-cycle PWM duty adjustments.
  - Deterministic telemetry pipelines using **VOFA+** for real-time bus voltage and control signal waveform debugging.

### 📐 Hardware Design & Magnetics
- **EDA & Layout (Altium Designer):** Multi-layer PCB design, high-voltage clearance/creepage rules, polygon pour cutouts, high-frequency gate drive routing, and structured BOM management.
- **Magnetics:** High-frequency transformer and resonant inductor sizing (PQ40 cores, Litz wire winding, leakage inductance integration, thermal mitigation).

### 📊 Market Microstructure, Order Flow & Economic Models
- **Price Action Methodologies:** Michael J. Huddleston's **Inner Circle Trader (ICT)** framework and **Al Brooks** price action methodology.
- **Structural Concepts:** Liquidity pools & sweeps, Market Structure Shifts (MSS), Fair Value Gaps (FVG), Order Blocks (OB), Breaker Blocks, and Premium/Discount arrays.
- **Markets & Derivatives:** Equities day trading / scalping, semiconductor leveraged ETFs (SOXL/SOXS), perpetual DEX mechanics (Hyperliquid, edgeX funding rates), and options order flow monitoring.
- **Daoist & Austrian Economic Dynamics:** Viewing market balance through spontaneous order (自发秩序), dynamic negative feedback loops ("损有余而补不足"), and liquidity distribution.

### 🖥️ Systems, Infrastructure & Hardware Tooling
- **Infrastructure:** Ubuntu server environments, Docker containerization, Tailscale mesh networking, and Zram/Swap tuning.
- **Storage & Flash Architecture:** Solid-State Drive (SSD) hardware architectures, NAND flash technologies (YMTC TLC / Solidigm QLC), USB bridge controllers (Realtek RTL9210/B), and testing utilities (Realtek MPTool, YTCoreTool).

---

## 🛠️ Tech Stack & Toolchain

### Firmware & Embedded Development
![C](https://img.shields.io/badge/-C-00599C?style=flat&logo=c&logoColor=white)
![Assembly](https://img.shields.io/badge/-dsPIC%20Assembly-6E4C13?style=flat)
![Microchip dsPIC](https://img.shields.io/badge/-dsPIC33CK%20%2F%20CH-DC2229?style=flat)
![ESP32-C3](https://img.shields.io/badge/-ESP32--C3-E7352C?style=flat&logo=espressif&logoColor=white)
![MPLAB X](https://img.shields.io/badge/-MPLAB%20X%20IDE%20%26%20XC16-143C54?style=flat)

### Hardware EDA & Simulation
![Altium Designer](https://img.shields.io/badge/-Altium%20Designer-A5915F?style=flat&logo=altiumdesigner&logoColor=white)
![VOFA+](https://img.shields.io/badge/-VOFA%2B%20Telemetry-29B6F6?style=flat)
![Python](https://img.shields.io/badge/-Python-3776AB?style=flat&logo=python&logoColor=white)

### Systems, Utilities & Trading
![Ubuntu Linux](https://img.shields.io/badge/-Ubuntu%20Linux-E95420?style=flat&logo=ubuntu&logoColor=white)
![Docker](https://img.shields.io/badge/-Docker-2496ED?style=flat&logo=docker&logoColor=white)
![Tailscale](https://img.shields.io/badge/-Tailscale-24292E?style=flat)
![VS Code](https://img.shields.io/badge/-VS%20Code-007ACC?style=flat&logo=visualstudiocode&logoColor=white)
![TradingView](https://img.shields.io/badge/-TradingView-131722?style=flat&logo=tradingview&logoColor=white)

---

## 📌 Highlighted Projects & Architectures

- **3kW Interleaved PFC Converter (`3KW_AC-DC_IPFC`):**
  - High-efficiency single-phase dual-interleaved PFC driven by **dsPIC33CK**.
  - Dual-loop control architecture: 1kHz outer voltage loop with anti-boundary-chatter variable PI parameters + 40kHz inner current loop utilizing discrete first-order IIR filters.
  - Deterministic ADC sampling references aligned directly to raw sensor counts.
- **30kW High-Power AC-DC Architecture:**
  - Multi-kilowatt power module featuring interleaved PFC front-end and full-bridge stage.
  - Cycle-by-cycle protection routines and PWM phase modulation implemented with hand-optimized DSC assembly routines.
- **ZVS Phase-Shifted Full Bridge (`3KW_AC-DC_PSFB` / `ZVS_FullBridge`):**
  - Peak Current Mode (PCM) controlled PSFB converter with digital slope compensation.
  - Zero-voltage soft switching across varying load regimes, optimized GDT gate drive networks, and cycle-by-cycle primary current limiting.
- **1kW Wide-Range LLC Resonant Converter:**
  - Wide output voltage resonant cavity design using PQ40 core geometry and Litz wire.
  - FHA impedance modeling, secondary synchronous rectification timing, and auxiliary feedback loop stability.
- **Systematic Order Flow & ICT Rule Engine:**
  - Quantitative scripts and indicator toolsets modeling institutional liquidity sweeps, order blocks, and multi-timeframe imbalance fills.

---

## 🌿 Philosophy & Guiding Principles

> *"道常无为而无不为。天之道，损有余而补不足。"* — 《老子》  
> *"Il faut cultiver notre jardin."* — Voltaire  
>
> 无论是微秒级闭环中的负反馈自稳、高频开关电路里的谐振裕度，还是面对非线性波动的风险敞口控制，本质皆是探寻底层确定性与自组织规律——敬畏边界，专注耕耘自己的花园。

---

## 📫 Connect With Me
- **GitHub:** [@huanglian34](https://github.com/huanglian34)
