# Mars AOCS Simulation

Attitude Control System simulation for a spacecraft in Low Mars Orbit using nonlinear rigid-body dynamics and Modified Rodrigues Parameters (MRP).

---

## Overview

This project simulates a spacecraft Attitude Determination and Control System (ADCS/AOCS) operating in a 400 km Low Mars Orbit.

The spacecraft autonomously switches between three mission modes:
- Sun Pointing
- Nadir Pointing
- Communication Pointing

The simulation focuses on nonlinear attitude dynamics, reference frame generation, and closed-loop tracking control.

---

## Key Features

- Modified Rodrigues Parameters (MRP) attitude representation
- Nonlinear rigid-body rotational dynamics
- PD tracking controller in body frame
- Autonomous mode switching logic
- Reference frame generation (Sun, Nadir, Communication)
- RK4 numerical integration
- 3D animation of spacecraft motion and attitude

---

## Dynamics Model

Rigid body rotational dynamics:

\[
\dot{\omega} = I^{-1} \left( u - \omega \times (I \omega) \right)
\]

MRP kinematics:

\[
\dot{\sigma} = \frac{1}{4} B(\sigma)\,\omega
\]

---

## Control Law

Tracking control is defined as:

\[
u = -K \sigma_{BR} - P \omega_{BR}
\]

Where:
- \( \sigma_{BR} \): attitude error (Body → Reference)
- \( \omega_{BR} \): angular velocity error in body frame
- K, P: control gains

---

## Reference Frame Generation

The simulation uses three reference frames:

- **Sun Frame**: fixed inertial direction approximation
- **Nadir Frame**: aligned with spacecraft position vector
- **Communication Frame**: line-of-sight vector between LMO and GMO spacecraft

---

## Mode Switching Logic

The spacecraft selects its pointing mode based on orbital geometry:

- **Sunlit condition** → Sun pointing mode
- **GMO visibility (≤ 35°)** → Communication pointing mode
- **Else** → Nadir pointing mode

---

## Numerical Method

- Integrator: RK4 (Runge-Kutta 4th order)
- Time step: 1 second
- Total simulation duration: multi-orbit scenario

---

## Results

The simulation produces:
- Attitude convergence under switching modes
- Stable tracking under nonlinear dynamics
- Smooth transitions between reference frames
- 3D spacecraft visualization (MATLAB animation export)

---

## Visualization

Includes animated visualization of:
- Spacecraft orbit in Mars-centered inertial frame
- Body frame orientation evolution
- Reference direction vector switching
- Mode-dependent pointing behavior

---

## Key Insight

The system demonstrates:
- Robust attitude stabilization under nonlinear dynamics
- Multi-mode autonomous control logic
- Practical MRP-based spacecraft control implementation

---

## Future Work

- Reaction wheel actuator model
- Sensor noise and estimation (EKF)
- External disturbance torques (aerodynamic / gravity gradient)
