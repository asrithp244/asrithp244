# Hi, I'm Asrith 👋

**Robotics & Embedded Systems Engineer** - I build systems that close the gap between simulation and real hardware.

MS Robotics @ Arizona State University. I work across the full stack: ROS 2 middleware, embedded firmware, real-time control loops, and perception pipelines.

📬 asrithmoose148@gmail.com · [LinkedIn](https://www.linkedin.com/in/asrith-pandreka/) · Open to new-grad Robotics SWE & Embedded Systems roles

---

## 📌 Featured Projects

### 🧠 [Humanoid Locomotion in Isaac Sim](https://github.com/asrithp244/IsaacSim-humanoid-gait)
Real-time locomotion control for a humanoid model, with PD controller gains tuned against USD Physics DriveAPI at runtime in NVIDIA Isaac Sim.
- **Stack:** NVIDIA Isaac Sim · USD PhysX DriveAPI · Python · ROS 2
- **What it proves:** Sim-to-real pipeline, humanoid dynamics, runtime control loop debugging
- **Key challenge solved:** High PD stiffness values caused joint oscillation in the PhysX contact solver; diagnosed by logging DriveAPI torque outputs per joint, identified the stiffness/damping ratio was mismatched to the inertia parameters, and retuned gains live without resetting the simulation.

### 🤖 [TurtleBot4 Autonomous Navigation](https://github.com/asrithp244/RAS598-2025-S-Team05.github.io)
Goal-oriented autonomy on TurtleBot4: an ESP32 IMU module streams positional goals over serial to a ROS 2 node, which feeds the Nav2 stack for real-time obstacle avoidance and SLAM-based navigation.
- **Stack:** ROS 2 Humble · Nav2 · SLAM Toolbox · ESP32 · Python · pyserial
- **What it proves:** Hardware bring-up, cross-device ROS 2 communication, full nav stack deployment on a physical robot
- **Key challenge solved:** ESP32 serial output occasionally dropped or malformed packets under USB load, causing the goal publisher node to crash; added input validation and reconnect logic to the serial parser so the nav stack recovered gracefully without requiring a restart.

### 🦾 [6-DoF Manipulation with Vision Guidance](https://github.com/asrithp244)
Perception-to-motion pipeline for a 6-DOF arm: camera input → YOLOv8 detection → MoveIt trajectory execution.
- **Stack:** ROS 2 · MoveIt · OpenCV · YOLOv8 · PyTorch · OMPL · Inverse Kinematics
- **What it proves:** End-to-end perception + manipulation, real-time CV integration
- **Key challenge solved:** YOLOv8 inference latency on CPU caused the arm to plan trajectories against stale detections, leading to grasp misses; moved inference to a dedicated thread decoupled from the planning loop, cutting end-to-end delay and eliminating the lag-induced misses.

### 🏭 [Virtual PLC Industrial Safety System](https://github.com/asrithp244/plc-kalman-ekf)
Safety interlock system for an industrial robot cell: EKF state estimator feeds a watchdog relay via Modbus TCP, running IEC 61131-3 Structured Text safety logic on OpenPLC.
- **Stack:** Python · Modbus TCP · IEC 61131-3 · Plotly Dash · EKF · Docker
- **What it proves:** Industrial protocol knowledge (Modbus/PLC), control system safety design, sensor fusion
- **Key challenge solved:** Raw encoder readings fed directly into safety interlocks caused constant false alarms from sensor quantization noise; built an EKF from scratch (numpy only, analytic Jacobians, Joseph-form covariance update) and added NEES chi-squared consistency monitoring, giving statistically grounded filter health checks rather than visual inspection.

---

## 🛠 Skills

**Robotics & Planning**
`ROS 2 (Humble)` `Nav2` `MoveIt` `SLAM Toolbox` `AMCL` `OMPL` `Trajectory Optimization` `Ceres Solver`

**Control & Estimation**
`PID / PD Control` `EKF / Sensor Fusion` `Quadrature Encoder Feedback` `Real-Time Control Loops`

**Embedded & Hardware**
`ESP32 (FreeRTOS)` `STM32` `Raspberry Pi 4` `Arduino` `UART / SPI / I2C / CAN` `PCB Design (KiCad)` `Firmware Bring-Up`

**Simulation**
`NVIDIA Isaac Sim` `Gazebo` `MATLAB Simulink / Simscape`

**Perception & ML**
`OpenCV` `YOLOv8` `PyTorch` `Inverse Kinematics`

**Languages**
`C++` `Python` `MATLAB`

**Industrial Protocols**
`Modbus TCP` `TCP/IP` `IEC 61131-3`

**Tooling**
`Git` `Docker` `Linux (Ubuntu)` `Bash` `RViz` `Oscilloscope` `Logic Analyzer`

---

## 📚 Education

**M.S. Robotics & Autonomous Systems** - Arizona State University  
**B.Tech Electrical Engineering**

---

## 📬 Let's Connect

I'm actively looking for entry-level / new-grad roles in **Robotics Software Engineering** and **Embedded Systems**.

- 📧 asrithmoose148@gmail.com
- 🔗 [LinkedIn](https://www.linkedin.com/in/asrith-pandreka/)
