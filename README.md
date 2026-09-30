# Mini Smart Factory
### Automated Conveyor & Sorting System

A student-built tabletop automation system that brings together mechanical design, electronics, embedded firmware, and a monitoring dashboard.

The project aims to transport objects along a conveyor, detect and classify them, and sort them into designated collection areas. A central controller will coordinate the process, while a dashboard will display system status and processing data.

Developed by a team of 10 Electrical Engineering, Computer Engineering, and Mechatronics students at the University of Waterloo.

**Status:** Planning and initial prototyping  
**Target MVP completion:** October 31, 2026

## Planned Features

- Motor-driven conveyor for automatic object transport
- Sensor-based object detection and classification into at least two categories
- Automated sorting into designated collection areas
- Central control for coordinating subsystem operation
- Monitoring dashboard for system status, object counts, and fault messages
- Manual stop and basic fault handling

The classification method and corresponding sensors will be selected through initial testing.

## System Architecture

The system consists of three connected subsystems:

| Subsystem | Purpose |
| --- | --- |
| Conveyor / Transport | Moves objects through the system using a custom conveyor, DC motor, and motor driver. |
| Detection / Sorting | Detects and classifies objects, then directs them into collection areas using a sorting mechanism. |
| Central Control / Monitoring | Coordinates subsystem operation, handles system states and faults, and provides dashboard updates. |

Controller selection, electrical interfaces, and communication methods are currently being evaluated.

## System Workflow

Object Input → Transport → Detection → Classification → Sorting → Collection

The central controller will coordinate this sequence and send status updates to the dashboard.

## Technology

The planned implementation includes:

- **Embedded firmware:** C/C++
- **Electronics:** Microcontrollers, sensors, motor drivers, and servo control
- **Mechanical design:** CAD, conveyor assembly, and custom mounts
- **Monitoring:** A dashboard for operational data and system status

Specific components and software tools will be documented as the design is finalized.

## Project Progress

The project is currently in the planning and initial prototyping stage. Current work focuses on component evaluation, subsystem design, and interface definition.

Photos, demonstration videos, and test results will be added as development progresses.

## Setup and Documentation

Build instructions, wiring diagrams, firmware setup, and dashboard setup will be added as working prototypes become available.

Detailed design decisions, subsystem interfaces, and testing procedures will be maintained in separate project documents.
