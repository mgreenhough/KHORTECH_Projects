---
title: "Dual Spectrum FPV Gimbal"
date: 2026-03-19
categories: [uas, electronics, 3d-printing]
tags: [FPV, Gimbal, Thermal, Camera, Quadcopter, Drone]
status: "In Progress"
image: "assets/project_photos/FPV_gimbal/Wraith One v18.png"
excerpt: "A universal, dual-spectrum camera gimbal for FPV quadcopters featuring -40° to +90° range of motion for a seamless combination of high-speed, full angle of attack flying and top-down surveillance in situ."
---

## Overview

**Full spectrum vision for any flight mission.**

This project addresses a critical limitation in FPV drone operations: The inability to change camera orientation when transitioning between extreme flight attitudes and loiter or position holds. FPV drones are typically unable to perform surveillance effectively becaus of there aggressive camera angle but they can transit to and from/between targets at high speed. "DJI" or "camera" type drones have excellent surveillance capabilities but lack the agility and speed of FPV drones.

The solution is a lightweight, single-axis gimbal carrying both thermal and visual spectrum cameras with an exceptional range of motion from -40° (pitched aft for aggressive forward attitude) to +90° (top-down(nadir) for stable and prolonged observation), enabling meaningful video feed regardless of aircraft pitch and speed.

---

## Technical Approach

The design prioritizes range of motion, damping and weight reduction through topology-optimized 3D printed components in a linkage free, direct drive single-axis design that also minimises cost and complexity. The components were nested specifically to facilitate maximum ROM and lower the gimbal’s moment of inertia about its rotation axis so as to reduce the servos torque requirements and maximise stability and tilt authority. 

A universal mounting system ensures compatibility with a wide range of FPV frames and DFM methodologies allow for streamlined and efficient manufacture and assembly.

An OEM cam-switcher enables seamless toggling between thermal and visual spectrum cameras but future iterations may see these feeds merged for a hybrid solution.

Camera angle is operator adjustable via a potentiometer on the radio but automatic and stabilized flight modes are absolutely possible. A relatively simple process utilising sensors already onboard that can enhance operational efficiency and user experience. This will be introduced in future iterations of the system.

FPV platforms can produce high vibrational noise in video feeds. The system uses customized TPU soft mounts for dampening and virtually eliminates this issue.

**Key specifications:**
- **Tilt range:** -40° to +90°
- **Payload:** Dual camera system (visual + thermal)
- **Control:** PWM input from flight controller or RC receiver to digital or analogue servo
- **Mounting:** Universal FPV frame compatibility (takes place of front standoffs)

---

## Images & Media

### CAD Renders

<figure>
  <img src="assets/project_photos/FPV_gimbal/Wraith One v18.png" alt="Gimbal CAD render showing dual camera mounting">
  <figcaption>Primary CAD render showing the dual-spectrum camera arrangement on 7 inch frame</figcaption>
</figure>

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 1rem;">
  <figure>
    <img src="assets/project_photos/FPV_gimbal/Wraith One.OneTwo v11.png" alt="Design iteration v11">
    <figcaption>Section analysis 1</figcaption>
  </figure>
  <figure>
    <img src="assets/project_photos/FPV_gimbal/Wraith One.OneTwo v12.png" alt="Design iteration v12">
    <figcaption>Section analysis 2</figcaption>
  </figure>
</div>

<div style="display: grid; grid-template-columns: repeat(2, 1fr); gap: 1rem;">
  <figure>
    <img src="assets/project_photos/FPV_gimbal/Wraith One.OneTwo v122.png" alt="Design iteration v122">
    <figcaption>Cruize ~-25 deg</figcaption>
  </figure>
  <figure>
    <img src="assets/project_photos/FPV_gimbal/Wraith One.OneTwo v123.png" alt="Design iteration v123">
    <figcaption>Top-down (nadir) mode</figcaption>
  </figure>
</div>

### Physical Prototype

<figure>
  <img src="assets/project_photos/FPV_gimbal/20241226_175048.jpg" alt="Assembled gimbal prototype">
  <figcaption>The start of the process</figcaption>
</figure>

---

## Current Status

The project is currently in the prototype testing phase. Dual video feed is functional.The mechanical design is finalized and initial prints have been validated for fit and function. Next steps include:

- Vibration isolation testing
- Control loop tuning for the servo drive
- Flight testing and validation