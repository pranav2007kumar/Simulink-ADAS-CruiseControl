# 🚗 Simulink ADAS: Adaptive Cruise Control (PID & MPC)

A comprehensive MATLAB/Simulink project demonstrating the application of classical and advanced control theory to real-world automotive systems. This repository models both standard Cruise Control and Adaptive Cruise Control (ACC) acting as an Advanced Driver Assistance System (ADAS).

## 📖 Project Overview
This project is split into two phases of vehicle dynamics control:

1. **Standard Cruise Control (PID Controller)**
   * Utilizes a classical Proportional-Integral-Derivative (PID) controller.
   * Maintains the vehicle's speed at a desired setpoint with minimal overshoot, fast settling time, and negligible steady-state error.
   * Demonstrates closed-loop feedback design for stability and robust tracking performance.

2. **Adaptive Cruise Control (Model Predictive Control - MPC)**
   * Extends the foundational PID model to handle complex, real-world driving scenarios.
   * Utilizes a Model Predictive Controller (MPC) to handle system constraints (e.g., maintaining a safe minimum distance from a lead car).
   * Actively manages acceleration and deceleration based on lead-car maneuvers and spacing errors.

## ✨ Core Features
* **Simulink Modeling**: Full `.slx` block diagrams for both PID and MPC architectures.
* **Safety Distance Tracking**: The MPC actively computes spacing errors, adjusting throttle to ensure collision avoidance while optimizing for the driver-set velocity.
* **Disturbance Rejection**: Both controllers are tested against simulated disturbances (e.g., upward slopes and changing aerodynamic drag) to ensure robustness.

## 📂 Repository Contents
* `Cruise_control.slx`: The foundational Simulink model using the PID controller.
* `Cruise_control.slx.r2022a`: A backward-compatible version of the PID model for MATLAB R2022a.
* `mpcACCsystem.slx`: The advanced Simulink model featuring the Model Predictive Controller (MPC) for Adaptive Cruise Control.
* `Result_Images/`: A collection of 23 simulation output plots and diagrams demonstrating velocity tracking, spacing error, and control effort.
* `slprj/`: Internal Simulink cache and project dependency files.

## 🚀 Getting Started
1. Clone the repository:
   ```bash
   git clone https://github.com/pranav2007kumar/Simulink-ADAS-CruiseControl.git
   ```
2. Open MATLAB (R2022a or newer recommended).
3. Navigate to the cloned directory.
4. Open `Cruise_control.slx` to explore the PID implementation.
5. Open `mpcACCsystem.slx` to explore the MPC ADAS implementation.
6. Run the simulations to view the scopes and dynamic vehicle responses.

## 🛠️ Built With
* **MATLAB / Simulink** 
* Control System Toolbox
* Model Predictive Control Toolbox

---
*Developed as part of the Modelling, Simulation & Analysis (MSA) Coursework.*
