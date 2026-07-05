# TW-SCH-001 -- Power Management Schematic Specification

**Project:** TW-SAP1 Hardware Platform\
**Product:** XS3400 Residential Smart Lock\
**Revision:** A (Pre-Schematic)

## Objective

Define the complete power subsystem to be implemented in the first KiCad
schematic sheet.

## Inputs

-   4 × AA Alkaline Battery Pack (Primary)
-   USB Type-C (Emergency Power Only)

## Functional Blocks

1.  Battery input connector
2.  Reverse polarity protection (P-MOSFET)
3.  USB-C input with ESD protection
4.  TVS surge protection
5.  Automatic source selection (battery/USB)
6.  TI TPS62840 buck regulator (3.3 V)
7.  TI TPS22916 load switch
8.  Test points
9.  Decoupling network

## Outputs

  Rail     Purpose
  -------- --------------------------
  VBAT     Raw battery voltage
  +3V3     Logic supply
  VMOTOR   Motor supply
  VSW      Switched peripheral rail

## Protection

-   Reverse battery protection
-   USB ESD (USBLC6-2SC6)
-   Input TVS diode
-   Power filtering capacitors

## Design Targets

-   Ultra-low standby current
-   High efficiency on AA batteries
-   JLCPCB-compatible footprints
-   Short regulator feedback loop
-   Wide motor power traces

## Deliverables

The KiCad implementation shall include: - Schematic symbols - Net
labels - Component values - Test points - ERC-clean design
