# TW-SCH-002 -- ESP32-C6 Core Schematic Specification

**Project:** TW-SAP1 Hardware Platform\
**Product:** XS3400 Residential Smart Lock\
**Revision:** A (Pre-Schematic)

## Objective

Define the ESP32-C6-MINI-1 integration for the TW-SAP1 main board.

## Core Device

-   MCU/Radio: ESP32-C6-MINI-1
-   Wi-Fi 6 (2.4 GHz)
-   Bluetooth LE 5
-   IEEE 802.15.4 (Matter/Thread ready)

## Power

-   Supply: +3.3 V
-   Local 100 nF decoupling at each supply pin
-   Bulk capacitor near module (10 µF recommended)

## Required Circuits

1.  EN (Reset) pull-up network
2.  Boot configuration circuitry
3.  UART programming/debug header
4.  Status test pads
5.  RF antenna keep-out region
6.  Ground stitching around module (excluding antenna)

## Planned Interfaces

  Interface   Connected Device
  ----------- -----------------------
  UART        HLK-ZW101 Fingerprint
  I²C         MTCH2120
  PWM/GPIO    DRV8833
  ADC         Battery Monitor
  GPIO        USB Detect
  GPIO        Buzzer

## PCB Requirements

-   Module placed at PCB edge
-   No copper beneath antenna
-   No high-current traces near antenna
-   Keep switching regulator away from RF section

## Deliverables

The KiCad sheet shall include: - ESP32-C6 symbol - Power pins -
Decoupling network - Programming interface - Net labels - ERC-clean
implementation
