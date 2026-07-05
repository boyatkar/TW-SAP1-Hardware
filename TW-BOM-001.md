# TW-BOM-001 -- Prototype Bill of Materials

**Project:** TW-SAP1 Hardware Platform\
**Product:** XS3400 Residential Smart Lock\
**Revision:** A (Draft)

## Purpose

This document defines the preliminary prototype Bill of Materials (BOM)
for the TW-SAP1 main controller board. Prices are target estimates and
will be validated during prototype procurement.

  Category             Component               Selected Part             Prototype Status
  -------------------- ----------------------- ------------------------- ------------------
  MCU                  Wi-Fi/BLE MCU           ESP32-C6-MINI-1           Frozen
  Fingerprint          Sensor Module           Hi-Link HLK-ZW101         Frozen
  Touch                Capacitive Controller   Microchip MTCH2120        Frozen
  Motor Driver         H-Bridge                TI DRV8833                Frozen
  Buck Regulator       DC/DC                   TI TPS62840               Frozen
  Load Switch          Power Switch            TI TPS22916               Frozen
  USB Protection       ESD                     ST USBLC6-2SC6            Frozen
  TVS                  Input Protection        SMF5.0A (or equivalent)   Preferred
  Reverse Protection   P-MOSFET                TBD                       Pending
  Buzzer               Piezo                   TBD                       Pending
  Connectors           JST/FPC                 TBD                       Pending
  USB                  USB Type-C              TBD                       Pending
  Passives             R/C/L                   0402/0603                 Pending

## Mechanical Items

-   MinebeaMitsumi actuator (preferred)
-   Dormount Euro profile cylinder (Phase 1)

## Notes

-   Prototype sourcing should prioritize JLCPCB/LCSC compatible parts
    where practical.
-   Alternate approved vendors will be added after prototype validation.
-   Production AVL will be maintained separately.

## Next Deliverable

Create TW-SCH-001 (Power Management Schematic).
