# Attitude Control Simulation

Simulation of a spacecraft attitude control system using nonlinear rigid body dynamics and closed loop attitude tracking control.

## Overview

The simulation demonstrates spacecraft attitude control through three pointing modes:

- Sun Pointing
- Nadir Pointing
- Communication Pointing (with a higher orbit satellite)

## Key Features

- Modified Rodrigues Parameters (MRP) and quaternion attitude representations
- Nonlinear rigid body rotational dynamics
- PD attitude tracking controller
- Autonomous switching between pointing modes
- Numerical integration of the attitude dynamics

## Control

A proportional-derivative (PD) controller tracks the commanded attitude. The controller uses attitude error and angular velocity error to calculate the control torque.

## Visualization

The simulation displays spacecraft orientation, reference directions, and changes in pointing mode over time.

## Future Work

- Reaction wheel actuator model
- Sensor noise and attitude estimation
- External disturbance torques
