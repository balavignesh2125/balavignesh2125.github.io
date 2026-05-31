# balavignesh.github.io
Portfolio focused on GNC, AOCS, spacecraft dynamics, control systems, simulation, and SIL/HIL validation.

## LMO AOCS Animation

## Overview

This project simulates the Attitude Determination and Control System (ADCS/AOCS) of a spacecraft operating in Low Mars Orbit.

The spacecraft autonomously switches between:

- Sun Pointing Mode
- Nadir Pointing Mode
- Communication Pointing Mode

The simulation models:

- Nonlinear rigid-body rotational dynamics
- Modified Rodrigues Parameters (MRP)
- Reference frame generation
- Autonomous mission-mode logic
- Closed-loop attitude tracking control

- ## Configuration
- ## Key Results

| Feature | Description |
|----------|-------------|
| Dynamics Model | Nonlinear Euler rotational equations |
| Attitude Representation | Modified Rodrigues Parameters |
| Controller | PD Tracking Controller |
| Numerical Integrator | RK4 |
| Mission Duration | 7000 s |
| Operational Modes | 3 |
| Orbit | 400 km Low Mars Orbit |

- ## Dynamics
- omega_dot = I_inv *(u - cross(omega,I*omega));

- ## Control law
- om_BR = om_BN - BR * om_RN;
- u = -K_gain*sig_BR-P_gain*om_BR;

- ## Attitude Error Computation
- BN = mrp2dcm(sig_BN);
- BR = BN * RN_ref';
- sig_BR = dcm2mrp(BR);
