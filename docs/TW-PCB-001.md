# TW-PCB-001 -- PCB Floor Plan & Layout Guidelines

**Project:** TW-SAP1 Hardware Platform\
**Product:** XS3400 Residential Smart Lock\
**Revision:** A (Draft)

## 1. PCB Overview

  Item         Specification
  ------------ ------------------------
  Board Size   65 mm × 45 mm
  Layers       4
  Thickness    1.6 mm
  Finish       ENIG
  Assembly     SMT, top side dominant

Bottom side is reserved primarily for capacitive touch electrodes.

## 2. Functional Zones

### Zone A -- RF

-   ESP32-C6-MINI-1
-   Antenna at PCB edge
-   No copper beneath antenna
-   RF keep-out maintained

### Zone B -- Power

-   Battery input
-   USB-C emergency input
-   TPS62840 buck regulator
-   TPS22916 load switch
-   TVS/ESD protection

### Zone C -- Processing

-   ESP32-C6
-   Decoupling capacitors close to power pins
-   Debug/programming pads

### Zone D -- User Interface

-   MTCH2120 touch controller
-   Fingerprint connector (HLK-ZW101)

### Zone E -- Motor

-   TI DRV8833
-   Motor connector
-   Wide power traces
-   Separate high-current routing

## 3. PCB Rules

-   Ground plane on internal layer
-   Separate motor and logic return paths
-   Ground stitching vias around board edge
-   Short regulator feedback loop
-   JLCPCB standard DRC compatibility

## 4. Testability

-   SWD/UART pads
-   Battery test point
-   3.3 V test point
-   Ground test point
-   Motor output test pads

## 5. Revision Control

PCB placement changes affecting RF, power, or mechanics shall be
reviewed before routing.
