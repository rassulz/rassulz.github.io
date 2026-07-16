---
title: "Kawasaki ROS 2 Safety Zone Monitoring in Isaac Sim"
excerpt: "A simulation-based robotic safety project integrating ROS 2 Humble, NVIDIA Isaac Sim, and YOLO-based human detection to stop and resume Kawasaki manipulator motion based on danger-zone occupancy. <br/> ![kawasaki_ros2_demo](https://img.youtube.com/vi/3Nn6YReXRXk/0.jpg)
"
collection: portfolio
---

This project demonstrates a **simulation-based safety monitoring system** for a **Kawasaki robotic manipulator** using **ROS 2 Humble** and **NVIDIA Isaac Sim 5.0.0**. The main objective is to improve safe human-robot interaction by stopping manipulator motion when a person enters a predefined danger zone and resuming motion automatically after the zone becomes clear.

The implementation combines **computer vision** and **robot motion control** in a ROS 2 workflow. A YOLO-based detector processes camera frames, identifies people in the workspace, and publishes a Boolean safety signal. Motion nodes use this signal to pause or continue the manipulator trajectory. The project includes both separated and combined node designs for flexibility during testing.

The simulation setup includes a Kawasaki manipulator, virtual human movement via `omni.anim.people`, and camera monitoring using an Intel RealSense D455 model. Motion control is based on **forward kinematics** and **inverse kinematics** for smooth trajectory generation.

**Highlights:** <br/>
- **ROS 2 Safety Architecture:** Real-time communication between perception and motion nodes using ROS 2 topics. <br/>
- **YOLO Human Detection:** Person detection and danger-zone checking from camera streams. <br/>
- **Safety Stop/Resume Logic:** Manipulator pauses when human is in zone and resumes when clear. <br/>
- **Kinematics-Based Motion:** Circular end-effector trajectory with inverse kinematics control. <br/>
- **Isaac Sim Integration:** Full workflow tested in NVIDIA Isaac Sim 5.0.0 on Linux 22.04.

**Project repository:**  
<a href="https://github.com/rassulz/kawasaki_ros2" target="_blank" rel="noopener noreferrer">
Project repository (GitHub)
</a>

### Program realization:

<iframe width="560" height="315" src="https://www.youtube.com/embed/3Nn6YReXRXk" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" referrerpolicy="strict-origin-when-cross-origin" allowfullscreen></iframe>
