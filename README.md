# Mini Smart Factory — Automated Conveyor & Sorting System

A student-built tabletop automation project combining mechanical design, electronics, embedded firmware, and a monitoring dashboard.

The system will transport objects on a conveyor, detect and classify them, sort them into collection areas, and display live system status.

**Project status:** Planning and initial prototyping  
**Team:** 10 students across Electrical Engineering, Computer Engineering, and Mechatronics  
**Target MVP completion:** October 31, 2026

## Project Goals

- Build a working automated transport and sorting system.
- Gain practical experience with motor control, sensors, embedded programming, and subsystem communication.
- Develop three subsystems that can be tested independently and integrated progressively.
- Document the design, implementation, and testing process.

## Minimum Viable Product (MVP)

The initial system should:

- [ ] Automatically transport an object using a conveyor.
- [ ] Detect an incoming object using at least one sensor.
- [ ] Classify objects into at least two categories.
- [ ] Route objects into the correct collection area using a sorting mechanism.
- [ ] Coordinate transport, detection, and sorting through a central controller.
- [ ] Display basic system status on a monitoring dashboard.
- [ ] Provide a manual stop function.
- [ ] Stop relevant actuators and report basic faults.

The classification property, such as color, size, or material, and its corresponding sensor will be selected after initial testing.

## System Architecture

The project is divided into three main subsystems.

### Subteam A : Conveyor / Transport

**3 members: proposed 2 EE + 1 TRON**

Responsible for moving objects reliably through the system.

- Conveyor mechanical design and CAD
- Fabrication, assembly, and motor mounting
- DC motor and motor driver selection
- Motor wiring and local power requirements
- Motor control and conveyor speed testing

### Subteam B : Detection / Sorting

**3 members: proposed 2 EE + 1 CE**

Responsible for detecting, classifying, and physically sorting objects.

- Sensor selection, circuits, and testing
- Object detection and classification firmware
- Servo and sorting gate design
- Sorting actuator wiring and control
- Detection and sorting status reporting

### Subteam C : Central Control / Monitoring

**4 members: proposed 1 EE + 3 CE**

Responsible for coordinating the overall system and displaying its status.

| Role | Responsibilities |
| --- | --- |
| Embedded Control | Main controller firmware, system state machine, command sequencing, and fault handling |
| Communication / Integration | Subsystem interfaces, message definitions, communication implementation, and integration testing |
| Dashboard / Software | Monitoring dashboard, status display, object counts, and fault display |
| Central Electronics | Central controller wiring, power distribution, electrical interfaces, and hardware integration |

### Cross-Team Leads

These responsibilities are held by members of the existing subteams.

- **System Lead : TRON:** Overall architecture, mechanical compatibility, and system integration.
- **Hardware Lead : EE:** Shared voltage, power, connector, wiring, and electrical interface standards.
- **Software / Firmware Lead : CE:** Shared firmware structure, communication protocol, code interfaces, and GitHub integration.

Individual assignments will be added once confirmed.

## Planned System Workflow

1. **INITIALIZING:** Initialize controllers, sensors, actuators, and communication.
2. **IDLE:** Wait for the system to begin.
3. **TRANSPORTING:** Move an object toward the detection and sorting station.
4. **DETECTING:** Detect the incoming object.
5. **CLASSIFYING:** Determine its category and destination.
6. **SORTING:** Activate the sorting mechanism.
7. **COLLECTING:** Allow the object to enter its collection area.
8. **RESETTING:** Reset the sorting mechanism and update the dashboard.
9. Return to **TRANSPORTING** for the next object.

Additional states:

- **STOPPED:** A manual stop has been activated.
- **ERROR:** A fault, such as a sensor timeout, communication failure, or possible object jam, has been detected.

Entering STOPPED or ERROR should stop relevant actuators and update the dashboard. Fault detection and restart behavior will be defined during implementation.

## Subsystem Communication

The team will define commands, data, and status messages before selecting the final communication method.

Initial interface examples:

| Message | Purpose |
| --- | --- |
| START_CONVEYOR | Request conveyor movement |
| STOP_CONVEYOR | Request conveyor stop |
| OBJECT_DETECTED | Report object presence |
| OBJECT_TYPE | Report the detected category |
| SORT_A / SORT_B | Request a sorting destination |
| READY | Report subsystem readiness |
| ERROR | Report a subsystem fault |

The MCU layout and communication method are still to be determined. Options include UART, I²C, SPI, or wireless communication, depending on hardware selection and system requirements.

## Monitoring Dashboard

Planned information includes:

- System state
- Number of objects processed
- Current object category and destination
- Conveyor status
- Sensor status
- Sorter readiness
- Fault messages

## Initial Hardware Plan

Components under consideration:

- Microcontroller board(s)
- DC motor and compatible motor driver
- Conveyor belt, rollers, and frame
- Object presence sensor
- Classification sensor
- Servo and sorting gate
- Collection bins
- Suitable power supplies and distribution hardware
- Wiring, connectors, and prototyping boards
- Manual stop control

Exact components, quantities, and electrical specifications are not yet finalized.

## Integration and Testing

Integration will take place progressively:

1. **Interface testing:** Verify command and status exchange.
2. **Conveyor + Central Control:** Test conveyor start, stop, and control.
3. **Detection / Sorting + Central Control:** Test detection, classification, and sorting coordination.
4. **Full system integration:** Test the complete object-to-collection workflow.
5. **Error testing:** Test manual stop, sensor timeout, communication failure, and possible jams.

## Next Steps

- [ ] Confirm team members and leads.
- [ ] Create the system block diagram.
- [ ] Select and test the classification method.
- [ ] Finalize initial hardware and procurement.
- [ ] Define subsystem interfaces and electrical standards.
- [ ] Develop subsystem prototypes.
- [ ] Begin interface and integration testing.

## Setup and Documentation

Build instructions, wiring diagrams, firmware setup, dashboard setup, and test results will be added as the hardware and software are developed.
