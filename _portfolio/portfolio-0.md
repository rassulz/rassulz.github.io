---
title: "Multirobot Control System for Automated Part Painting"
excerpt: "A completed and laboratory-validated automated painting line coordinating two RoArm-M2-S spray arms, a KUKA KR10 robot, a conveyor, and Siemens S7-1500 control through MATLAB/Simulink. <br/> ![Laboratory implementation of the multirobot painting system](https://raw.githubusercontent.com/rassulz/multirobot_painting_control_system/main/docs/images/Physical_System_Implementation.png)
"
collection: portfolio
---

This completed **2026 KBTU graduation project**, developed by a four-person student team, is a distributed multirobot control system with real-time monitoring for an automated industrial painting line. It coordinates **two collaborative painting manipulators**, an **industrial pick-and-place robot**, and a **conveyor** within one production cycle. The laboratory implementation was modeled on an automotive painting line at **Hyundai Trans Kazakhstan** and designed for future industrial scale-up.

Research based on this project was accepted for **The 20th IEEE International Conference on Control & Automation (IEEE ICCA 2026)**.

![Laboratory implementation of the multirobot painting system](https://raw.githubusercontent.com/rassulz/multirobot_painting_control_system/main/docs/images/Physical_System_Implementation.png)

### Automated process

The system automates the full part-finishing cycle:

1. The conveyor transports and positions the workpiece using inductive proximity sensors.
2. Two **Waveshare RoArm-M2-S** manipulators paint the workpiece simultaneously.
3. The conveyor transfers the painted part through the drying station.
4. A **KUKA KR10 R1100-2** robot unloads the finished part with an electromagnetic gripper.

Every stage transition is controlled by PLC interlocks, keeping the conveyor, painting arms, drying system, and KUKA robot synchronized.

### Control architecture

- **Supervisory level — MATLAB and Simulink:** Performs high-level coordination, trajectory generation, robot dispatch, kinematics, and real-time telemetry. The Simulink supervisor reads workpiece-position sensors through OPC UA and launches the required painting or pick-and-place process.
- **Industrial control level — Siemens SIMATIC S7-1500:** Executes deterministic sequencing, safety interlocks, field-device I/O, drying control, and closed-loop PID speed control for the BLDC conveyor. A **WinCC SCADA/HMI** provides operating modes, alarms, trends, and live process visualization.
- **Physical level:** Includes the KUKA robot, two RoArm manipulators, a BLDC conveyor, four inductive sensors, the drying fan, and the electromagnetic end-effector.

![Three-level architecture of the multirobot painting control system](https://raw.githubusercontent.com/rassulz/multirobot_painting_control_system/main/docs/images/architecture_three_level.png)

### Key engineering work

- **Three-robot coordination:** Integrated two 4-DOF RoArm painting manipulators with a 6-DOF KUKA industrial robot in one sensor-driven production cycle.
- **Multi-protocol communication:** Used **PROFINET** for field devices, **OPC UA** for PLC–MATLAB supervision, **TCP/IP with KukaVarProxy** for KUKA control, and **HTTP/JSON over Wi-Fi** for the RoArm manipulators.
- **KUKA pick-and-place control:** Developed a MATLAB interface with pose editing, 3D trajectory preview, live joint telemetry, execution controls, and smooth quintic trajectories with joint-limit and singularity safeguards.
- **Dual-arm painting control:** Implemented MATLAB motion-control classes and a dual-arm application with jogging, workspace preview, path planning, synchronized execution, and telemetry.
- **Conveyor regulation:** Implemented PLC-based PID speed control for the BLDC conveyor to maintain a constant production takt under changing loads.
- **Safety and monitoring:** Added PLC-governed operating modes, emergency-stop handling, safety handshakes, device interlocks, HMI alarms, and real-time monitoring of robot and process states.

### Technology stack

**MATLAB R2025b · Simulink · Siemens TIA Portal V19 · WinCC · SIMATIC S7-1500 · OPC UA · PROFINET · TCP/IP · HTTP/JSON · KUKA KRL · ESP32 · AutoCAD · Fusion 360**

### Project resources

- <a href="https://github.com/rassulz/multirobot_painting_control_system" target="_blank" rel="noopener noreferrer">Source code and technical documentation (GitHub)</a>
- <a href="https://github.com/rassulz/multirobot_painting_control_system/blob/main/docs/Diploma_Final.pdf" target="_blank" rel="noopener noreferrer">Full graduation thesis (PDF)</a>
- <a href="https://github.com/rassulz/multirobot_painting_control_system/blob/main/docs/Diploma_presentation.pdf" target="_blank" rel="noopener noreferrer">Project presentation (PDF)</a>

### System demonstration

<iframe width="560" height="315" src="https://www.youtube.com/embed/CDdXuiCqLzY" title="Multirobot painting control system demonstration" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
