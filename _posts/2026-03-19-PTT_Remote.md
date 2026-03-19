---
title: "Universal Remote PTT - Peripheral Serial Emulator"
date: 2026-03-19
categories: [electronics, agriculture]  # Options: motorsport, aviation, uas, agriculture, electronics, 3d-printing
tags: [PTT, UHF, CB Radio, Serial Communication, Equipment Operator, Safety, Agriculture, Heavy Equipment, Hands Free]
status: "In Progress"  # Options: Planning, In Progress, Complete, Testing
image: "assets/project_photos/PTT/PCB.png"
excerpt: "A hardware-based peripheral designed to universally learn and emulate RS-232/TTL/UART serial commands enabling remote PTT capabilities for consumer UHF/CB radios."
---

## Overview

**IN PROGRESS**

**Keep your hands on the controls, not the radio.**

Remote Push To Talk (PTT) switches have been used in aviation for decades, allowing pilots to maintain control of critical flight systems while staying connected with air traffic control. Yet machine operators in agriculture, construction, and heavy industry—who often manipulate even more controls—have had to stop operating just to transmit on their radio.

The PTT Peripheral Serial Emulator (PSE) is a universal hardware solution that bridges this gap. It learns and emulates RS-232/TTL/UART serial commands from any UHF/CB radio handpiece, enabling remote PTT functionality without compromising safety or productivity.

---

## Technical Approach

The device addresses two distinct handpiece architectures found in modern radios:

**Traditional Handpieces:** Simple devices containing only a speaker, microphone, and PTT button. When pressed, the PTT button grounds a specific pin within the radio to activate transmission. For these, the operation is simple, the PSE learns the grounding pin and initiates transmission by connecting it to GND.

**Remote Handpieces:** More complex units with additional control buttons (channel change, volume, scan on the handpiece). These send serial commands to the radio when any button is pressed (including PTT). The PSE's serial emulation capability captures these PTT commands and replays them to activate transmission remotely.

Key technical features include:
- Serial command learning and emulation up to 115200 baud
- ±15V tolerant inputs with reverse polarity, over-voltage, and over-current protection
- Dual-core architecture with dedicated debug channel (8-channel bipolar voltage analyser and UART detector)
- WiFi hotspot hosting an intuitive GUI accessible without internet connectivity
- RJ45 connectivity for seamless integration between radio and handpiece

---

## Execution

The project is being developed as an open-source hardware platform with three main components:

**Hardware:** Custom PCB design with robust input protection and dual-core processing. The physical interface uses standard RJ45 connectors for universal compatibility with existing radio handpiece cables.

**Firmware:** Embedded software handling serial communication, command learning algorithms, and real-time PTT emulation. In this research stage, the debug core operates independently to provide continuous signal analysis without impacting primary functionality.

**Software:** Browser-based GUI hosted on the device itself. Users connect to the "PTT" WiFi hotspot via smartphone, scan a QR code or navigate to the local IP, and follow guided prompts to learn their radio's specific PTT sequence. Radio profiles can be saved and recalled for plug-and-play operation across multiple devices.

The learning process is straightforward: connect via WiFi, set the GUI mode switch to "Learn", press the PTT button on the handpiece, and the device captures the command. Switch to "Run" mode in the GUI and the remote PTT is ready for use.

**Progress** 

| Parameter | Value |
|-----------|-------|
| PCB | Design ready for validation and manufacture |
| Firmware/Software | Preliminary vibe code complete |
| Testing | Pending integration with hardware |

We are really looking forward to getting the PCB completed so that we can start testing and validating!

---

## Images & Media


<div style="display: grid; grid-template-columns: repeat(3, 1fr); gap: 1rem;">
  <figure>
    <img src="{{ '/assets/project_photos/PTT/PCB.png' | relative_url }}" alt="PCB Design">
    <figcaption>PCB Design</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/project_photos/PTT/Hardware Interface.png' | relative_url }}" alt="Hardware Interface">
    <figcaption>Hardware Interface Block Diagram</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/project_photos/PTT/PSE3.1.png' | relative_url }}" alt="PSE v3.1">
    <figcaption>Main Block Diagram</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/project_photos/PTT/PulseView.png' | relative_url }}" alt="PulseView Analysis">
    <figcaption>Example of PTT protocol: GME AT Command PulseView Analysis 57600 Baud 8n1</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/project_photos/PTT/PSE_PTT_1.1-SCH.svg' | relative_url }}" alt="Schematic">
    <figcaption>Main Schematic</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/project_photos/PTT/PSE_PTT_1.1-SCH-Power.svg' | relative_url }}" alt="Power Schematic">
    <figcaption>Power Schematic</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/project_photos/PTT/PSE_PTT_1.1-SCH-Peripherals.svg' | relative_url }}" alt="Peripherals Schematic">
    <figcaption>Peripherals Schematic</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/project_photos/PTT/PSE_PTT_1.1-B_Mask.svg' | relative_url }}" alt="Board Mask">
    <figcaption>Board Mask</figcaption>
  </figure>
  <figure>
    <img src="{{ '/assets/project_photos/PTT/PSE_PTT_1.1-SIG 1.svg' | relative_url }}" alt="Signal Layer">
    <figcaption>Signal Layer</figcaption>
  </figure>
</div>

---

## Specifications

| Parameter | Value |
|-----------|-------|
| Interface | RJ45 (Radio and Handpiece) |
| Serial Support | RS-232 / TTL / UART up to 115200 baud |
| Input Protection | ±15V tolerant, reverse polarity, over-voltage, over-current |
| Connectivity | WiFi Hotspot (Local hosting, no internet required) |
| Power | USB or 12V |
| Debug Features | 8-channel bipolar voltage analyser, UART detector |

---

## Who Is It For?

- Earthmovers and heavy equipment operators
- Road crews and construction teams
- Farm machinery operators
- Anyone using UHF/CB radio with occupied hands

---

## Project Links

- **GitHub Repository:** [github.com/mgreenhough/PTT](https://github.com/mgreenhough/PTT)
