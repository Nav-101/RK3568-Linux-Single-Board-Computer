# ROCKY — RK3568 Linux Single-Board Computer

ROCKY is a custom application-class single-board computer built around the Rockchip RK3568. The project is intended to develop and demonstrate practical SoC hardware-design skills: multi-rail power architecture, PMIC integration, high-speed memory, storage, multimedia interfaces, PCB layout and eventual embedded-Linux bring-up.

> **Current status:** schematic design in progress. The board has not yet been fabricated or validated.

## Design direction

The board is being developed as a compact, media-oriented Linux platform rather than a copy of an existing reference design. The intended architecture includes:

- Rockchip RK3568 quad-core Arm Cortex-A55 SoC
- RK809 PMIC and the required power sequencing/control connections
- External DDR memory
- On-board non-volatile storage
- MicroSD support
- Audio codec and external audio interfaces
- Camera and display connectivity
- USB and Ethernet
- On-board generation of the main 5 V and 3.3 V rails from a 12 V input
- Debug and hardware bring-up access

## Current progress

### Completed

- Defined the initial system architecture and divided the schematic into functional hierarchical blocks.
- Created the KiCad project and imported the RK3568 symbol and BGA footprint.
- Checked the imported package dimensions and 0.65 mm ball pitch against the device documentation.
- Connected the RK3568 power and ground pins.
- Added the required local decoupling capacitors for the SoC supply domains.
- Established the preliminary 12 V input and on-board 5 V/3.3 V power-conversion strategy.
- Added the RK809 PMIC and worked through its supply, reference, RTC and management connections.
- Connected the PMIC control and management signals, including the required open-drain interfaces.

### In progress

- Completing the RK809 audio-codec section and its analogue/digital support circuitry.
- Continuing schematic capture one subsystem at a time, with each interface checked against the RK3568 and peripheral documentation.
- Reviewing power sequencing, rail dependencies and signal-voltage domains as the remaining blocks are added.

### Next stages

1. Complete the audio subsystem.
2. Add DDR memory and validate topology, pin mapping and power requirements.
3. Add boot/storage interfaces, including on-board flash and microSD.
4. Add Ethernet, USB, camera and display interfaces.
5. Complete clocks, reset, boot configuration and debug connections.
6. Run a full schematic and power-sequencing review.
7. Define the PCB stack-up, placement strategy and breakout approach for the 0.65 mm-pitch BGA.
8. Route, verify, manufacture and bring up the hardware.
9. Develop the Linux boot and board-support configuration.

## Engineering objectives

This project is being used to build demonstrable competence beyond MCU-level designs, particularly in:

- Application-processor power architecture and sequencing
- PMIC integration
- DDR design constraints
- High-speed interface implementation
- Dense BGA breakout and multilayer PCB design
- Hardware bring-up and fault isolation
- Boot chain, device tree and embedded-Linux board support

## Project status summary

| Area | Status |
| --- | --- |
| System architecture | Initial definition complete |
| KiCad project structure | Complete |
| RK3568 symbol/footprint integration | Complete; continuing pin-level verification |
| SoC power, ground and decoupling | Complete |
| Main input-power concept | Defined |
| RK809 PMIC management connections | Complete |
| Audio codec | In progress |
| DDR, storage and high-speed interfaces | Planned |
| PCB layout | Not started |
| Fabrication and bring-up | Not started |

The repository will be expanded with schematic extracts, design decisions, PCB progress, manufacturing outputs and bring-up results as the project develops.
