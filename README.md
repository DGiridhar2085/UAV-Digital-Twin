# UAV Digital Twin

## Real-Time Digital Twin-Based Multi-Sensor Fault Diagnosis and Predictive Maintenance for UAVs

### Current Project Status
**Phase 1 — Telemetry / Data Transfer**

The project is currently focused on establishing reliable live data transfer from the UAV flight controller to the software system. The Digital Twin, ML fault diagnosis, predictive maintenance, and dashboard stages are future development phases and are **not yet implemented**.

### Work Completed So Far
- Investigated the UAV-to-software telemetry pipeline.
- Worked on live flight-data transfer using PX4/MAVLink.
- Tested the telemetry/data-transfer stage before moving to Digital Twin development.
- Established the telemetry gateway as the next integration point.

### Current Architecture
```text
UAV / PX4 Flight Controller
          |
       MAVLink
          |
   Python Telemetry
       Gateway
          |
   Live Data Stream
```

The immediate goal is to make the telemetry pipeline stable and measurable before adding visualization or Digital Twin functionality.

### Planned Development
1. Complete and validate live telemetry transfer.
2. Parse and normalize required UAV telemetry fields.
3. Add timestamping and latency measurements.
4. Build the live software-side UAV state representation.
5. Develop the Digital Twin visualization.
6. Add historical telemetry storage.
7. Generate and collect controlled fault data.
8. Develop multi-sensor fault detection and classification.
9. Add fault severity estimation and health scoring.
10. Investigate predictive maintenance / RUL estimation.
11. Validate the system using real UAV experiments.

### Target Telemetry
- Roll, pitch and yaw
- Altitude
- Velocity / speed
- GPS position
- IMU measurements
- Battery voltage and current
- Motor / ESC telemetry where available
- Temperature and vibration data where available

### Core Technologies
- PX4
- MAVLink
- Python
- pymavlink
- WebSocket for future live application streaming
- FastAPI for the future backend
- Machine Learning for later fault-diagnosis stages

### Repository Structure
```text
UAV-Digital-Twin/
├── README.md
├── docs/
│   ├── CURRENT_STATUS.md
│   ├── TELEMETRY_ARCHITECTURE.md
│   └── ROADMAP.md
├── telemetry/
├── digital_twin/
├── ml/
├── experiments/
├── hardware/
└── research/
```

### Scope Note
**Isaac Sim and other simulation platforms are intentionally excluded from the current implementation.** The present work is limited to the telemetry/data-transfer foundation. Digital Twin and simulation components will be added only after the live data-transfer layer is working reliably.

---

## Project Direction
The long-term objective is a real-time UAV health-monitoring Digital Twin that mirrors the physical UAV state, uses multi-sensor telemetry for fault diagnosis, estimates fault severity, and supports predictive maintenance. The repository will be updated incrementally as each stage is actually implemented and validated.
