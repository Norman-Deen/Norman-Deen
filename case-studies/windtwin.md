# WindTwin — Operational Wind Farm Prototype

[Live demo](https://windtwin.nourtin.com/) · [Full visual case study](https://nourtin.com/pages/Subpages/windtwin-case-study.html) · [Nourtin](https://nourtin.com/)

## Purpose

Explore how a browser-based 3D environment can connect spatial context, asset condition, and maintenance action. This independent portfolio project covers application architecture, TypeScript development, 3D integration, responsive interfaces, simulation, and performance optimization.

## Operational workflow

1. Inspect the farm and select one of the four primary turbines.
2. Review operating values, charts, health, and fault information.
3. A simulated fault creates an alert and linked work order.
4. Prioritize work and dispatch the maintenance vehicle.
5. Track travel, service progress, completion, and asset recovery.

The expanded environment supports 100 turbines using four primary assets plus medium- and low-detail assets loaded on demand.

## Engineering

- Three.js / WebGL rendering with TypeScript and Vite.
- Centralized state shared by the scene, dashboards, charts, alerts, and work orders.
- Chart.js monitoring and selectable turbine, vehicle, and Operations Center views.
- Live Open-Meteo weather context.
- Adaptive pixel ratio and shadow quality, deferred modules, and detail levels.
- Runtime FPS, draw-call, triangle-count, GPU, and loading diagnostics.

## Data boundaries

| Data | Source |
| --- | --- |
| Wind, direction, air temperature | Live Open-Meteo API, with fallback behavior |
| Turbine operating input | Normalized demo wind input |
| Power, rotor speed, temperature, vibration | Internal simulation |
| Faults, personnel, inventory, work orders, vehicle movement | Demonstration logic |
| Camera views | Simulated image feeds |

This is a **Digital Twin visualization prototype**, not a production SCADA system. It has no physical PLC/sensor connection and must not be used for operational decisions.

## Performance interpretation

The external case study includes device-specific diagnostics. Loading and frame-rate results depend on the tested device, scene mode, network, cache, and quality settings; they are not universal guarantees. Local diagnostic load times must be distinguished from network startup times.

## Repository scope

This document is a public engineering overview. It does not publish private application source, credentials, or licensed 3D assets. See the full visual case study for screenshots and architecture diagrams.

[Back to profile](../README.md)
