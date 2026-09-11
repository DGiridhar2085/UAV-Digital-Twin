# Telemetry Architecture

## Current Data Path

```text
Physical UAV / PX4
        ↓
     MAVLink
        ↓
Python Telemetry Gateway
        ↓
  Parsed UAV State
```

## Purpose

This layer is the foundation for the future Digital Twin. It is responsible for receiving UAV telemetry, decoding the required messages, validating the values, and preparing a consistent software-side representation.

## Initial Telemetry Fields

- Attitude: roll, pitch, yaw
- Altitude
- Velocity / speed
- GPS position
- IMU data
- Battery voltage/current
- Motor/ESC information when supported by the flight-controller configuration

## Design Principle

Keep the live telemetry path lightweight. Historical storage, Digital Twin visualization, machine-learning inference, and other processing should be connected after the basic telemetry stream is stable rather than placed in the critical transfer path.

## Next Validation Steps

1. Confirm continuous MAVLink reception.
2. Verify individual message fields and units.
3. Record timestamps at reception.
4. Measure packet/update frequency.
5. Measure end-to-end transfer latency when the next application layer is added.
6. Handle dropped, delayed, or invalid messages safely.
