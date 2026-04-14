---
title: "Development of multirobot painting control system with realtime monitoring"
excerpt: "An automated multirobot control system line that coordinates industrial manipulators, conveyor motion, and process monitoring in real time to improve efficiency, coating quality, and operator safety. <br/> ![painting_control_system](https://raw.githubusercontent.com/rassulz/rassulz.github.io/customize/images/diploma_picture_laboratory.jpg)
"
collection: portfolio
---
Accepted for publishing in The 20th IEEE International Conference on Control & Automation (IEEE ICCA 2026)

This **ongoing** project focuses on the development of a **multirobot painting control system with real-time monitoring** for automated industrial production. **The goal of the system** is to **increase process efficiency**, **reliable system**, and **remove human operators from hazardous working environments** by using coordinated robotic manipulators and intelligent control logic.


The system integrates a ** collaborative RoArm M2s manipulators** and and **industrial KUKA KR10 R1100-2 manipulator**, all low level commands made by PLC SIMATIC s7-1500,  and high-level coordination and operation is made by MATLAB/SYMULINK. The whole process consistes of 3 main stages such as **painting process**, **drying process** and **pick and place process**.   



**Highlights:** <br/>
- **MATLAB/SYMULINK:** Path plannig, coordination and real time monitoring of robot, such as torque, current, velocity and voltage <br/>
- **PLC SIMATIC S7-1500S:** low level coordination, via OPC UA, SCADA system integraion, and hmi visualization <br/>
- **Mathematical model** conveyor belt mathematical model, stability and different regulators integration such as LQR and PID<br/>

<a href="https://github.com/rassulz/multirobot_painting_control_system" target="_blank" rel="noopener noreferrer">
Project repository (GitHub)
</a>

### Program realization:

<iframe width="560" height="315" src="https://www.youtube.com/embed/7L7fTCguy7g" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>



<br/><br/>

This project universle system, which can be implemetant to any INDUSTRY 5.O, and right now, working on integration of reinforcement learning, in order to make system more accurate and data-driven system.