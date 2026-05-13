# Power Grid Frequency Control Using PI/PID Controller

## Problem Statement

Sudden load changes in a power grid can cause frequency deviations and instability in the system. The objective of this project is to design a PI/PID controller that stabilizes the system frequency quickly with minimal oscillations and stable response.

---

## System Model

The power grid system is modeled as:

G(s) = 1 / (4s + 1)

Where:
- Input = Control signal
- Output = Frequency deviation
- Disturbance = Sudden load change at t = 8 seconds

---

## Objectives

- Restore frequency deviation back to zero quickly
- Minimize oscillations
- Ensure stable system response
- Analyze disturbance rejection capability

---

## Approach

1. Modeled the power grid using a transfer function.
2. Applied a sudden load disturbance at 8 seconds using a Step block.
3. Designed a PI/PID controller for automatic correction.
4. Simulated the system response in MATLAB Simulink.
5. Evaluated system stability and frequency restoration.

---

## Simulink Blocks Used

| Block Name | Parameters |
|------------|------------|
| Step | Step Time = 8, Initial Value = 0, Final Value = 1 |
| Sum | Signs = +- |
| PID Controller | Kp = 1, Ki = 0.5, Kd = 0 |
| Transfer Function | Numerator = [1], Denominator = [4 1] |
| Scope | Used for response visualization |

---

## Block Diagram
![Block Diagram](images/block diagram.png)
---

## Simulation Response

The disturbance introduced at t = 8 seconds causes a temporary frequency deviation. The PI/PID controller detects the error and automatically stabilizes the system by reducing oscillations and restoring the frequency back to steady state.

---

## Add-On Application

This system can also be implemented in portable microgrids used in disaster relief camps, military defense stations, and emergency rescue operations. Sudden activation of heavy loads such as medical equipment or communication systems may disturb the grid frequency, and the controller helps stabilize the power supply quickly and efficiently.

---

## Files Included

- MATLAB Simulink Model
- MATLAB Source Code
- Simulation Graphs
- Demo Video
- Project Report

---

## How to Run the Project

1. Open MATLAB.
2. Open the Simulink model file from the src folder.
3. Run the simulation.
4. Observe the frequency response on the Scope block.

---

## Tools and Technologies

- MATLAB
- Simulink
- PI/PID Controller
- Control System Toolbox

---

## Conclusion

The proposed PI/PID-based frequency control system successfully stabilizes frequency deviations caused by sudden load disturbances. The controller improves system stability, reduces oscillations, and ensures faster recovery of the power grid frequency.
