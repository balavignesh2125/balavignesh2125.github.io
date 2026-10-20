
# Cubli — Three-Axis Edge Balancing

## Overview

The Cubli is a three-axis reaction-wheel-based balancing platform designed to balance on an edge. This project combines embedded C++, inertial sensing, feedback control, and motor actuation to demonstrate active attitude stabilisation on a physical system.

The accompanying video shows the Cubli balancing on an edge.

## Demonstration

![Cubli balancing demonstration](cubli-balancing.gif)

The demonstration video is available on the [portfolio homepage](../../).

## System Architecture

The available source-code snapshot references the following components:

- **Microcontroller:** Teensy 4.1
- **Inertial measurement unit:** Bosch BMI270
- **Motor control:** moteus motor controller
- **Communication:** CAN
- **Software:** Embedded C++ using the Arduino framework and PlatformIO

The hardware configuration of the successful demonstration must be confirmed against the original working version.

## Control and State Estimation

The available source snapshot contains implementations related to:

- **Attitude estimation:** IMU measurement processing and complementary filtering
- **Feedback control:** Linear Quadratic Regulator (LQR) implementation
- **Motor actuation:** Torque commands sent to the motor controller
- **Embedded execution:** Sensor acquisition, state processing, and control-loop execution

The exact relationship between these components in the successful three-axis balancing implementation remains to be verified.

## Mathematical Model

The control model should document the relevant rigid-body and reaction-wheel dynamics, including:

- Body attitude and angular velocity
- Reaction-wheel angular velocities
- Coupling between body motion and wheel acceleration
- State-space representation used by the controller
- Modelling assumptions and coordinate conventions

The equations, parameters, and state definitions will be added after the working implementation is recovered or verified.

## Experimental Results

The available video demonstrates the physical system balancing on an edge.

Quantitative performance results have not yet been documented. Future analysis should establish:

- Balance duration and repeatability
- Attitude stability and settling behaviour
- Reaction-wheel speed and control effort
- Sensor noise and estimation performance
- Behaviour under disturbances

## Repository Structure

The available source snapshot includes:

- `src/` — embedded application and implementation files
- `include/` — project header files
- `lib/` — supporting libraries
- `test/` — test code
- `host/lqr/` — host-side LQR implementation
- `platformio.ini` — PlatformIO build configuration

## Current Status and Limitations

The available source snapshot may not be the exact version used for the successful balancing demonstration.

The final control architecture, model parameters, three-axis implementation, build procedure, and experimental performance require verification before they can be documented as established results.

## Future Work

- Recover and identify the working source-code version.
- Document the complete three-axis control architecture.
- Verify the mathematical model and controller implementation.
- Add reproducible build and setup instructions.
- Quantify experimental performance using recorded data.
