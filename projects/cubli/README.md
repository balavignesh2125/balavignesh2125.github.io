
# Cubli — Three-Axis Edge Balancing

## Overview

The Cubli is a 3-axis reaction wheel based balancing cube designed to balance on an edge and a corner. This project combines embedded C++, inertial sensing, feedback control, and motor actuation to demonstrate active attitude stabilisation on a physical system.

The accompanying video shows the Cubli balancing on an edge.

## Demonstration

![Cubli balancing demonstration](cubli-balancing.gif)

The demonstration video is available on the [portfolio homepage](../../).

## System Architecture

- **Microcontroller:** Teensy 4.1
- **Inertial measurement unit:** BMI270
- **Motor control:** Moteus motor drive
- **Communication:** CAN bus, SPI, I2C
- **Software:** Embedded C++ using the Arduino framework and PlatformIO

The hardware configuration of the successful demonstration must be confirmed against the original working version.

## Control and State Estimation

- **Attitude estimation:** IMU measurement processing and complementary filtering
- **Feedback control:** Linear Quadratic Regulator (LQR) implementation
- **Motor actuation:** Torque commands sent to the motor drive
- **Embedded execution:** Sensor acquisition, state processing, and control-loop execution

The exact relationship between these components in the successful three-axis balancing implementation remains to be verified.

## Mathematical Model

- Body attitude and angular velocity
- Reaction-wheel angular velocities
- Coupling between body motion and wheel acceleration
- State-space representation used by the controller
- Modelling assumptions and coordinate conventions

The equations, parameters, and state definitions will be added after the working implementation is recovered or verified.

## Experimental Results

- Edge Balance duration up to 5 mins, Corner balance of few seconds and repeatability
- Attitude stability and settling behaviour irrespective of surface friction and sharp edges, corners
- Reaction wheel speed and control effort
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
