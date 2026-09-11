# Project Roadmap

## Phase 1 — Telemetry / Data Transfer
**Current**
- PX4 telemetry
- MAVLink communication
- Python telemetry handling
- Transfer validation

## Phase 2 — Telemetry Foundation
- Normalize telemetry data
- Timestamp messages
- Measure update rate and latency
- Improve error/dropout handling
- Add structured logging

## Phase 3 — Software UAV State
- Create a clean software representation of UAV state
- Connect the live telemetry stream to the application layer

## Phase 4 — Digital Twin
- Real-time state synchronization
- UAV state visualization
- Historical state and telemetry

## Phase 5 — Fault Diagnosis
- Controlled fault-data collection
- Multi-sensor feature engineering
- Baseline anomaly detection/classification
- Component-level fault identification

## Phase 6 — Health & Predictive Maintenance
- Fault severity estimation
- UAV/component health score
- Degradation tracking
- Predictive maintenance / RUL investigation

## Phase 7 — Validation
- Real-UAV experiments
- Sim-to-real work only if later required
- Accuracy and F1 evaluation
- Detection latency
- Telemetry-to-application latency
- False-positive analysis
- Resource/bandwidth measurements

> Roadmap items describe future work and should not be presented as completed until they are actually implemented and tested.
