# TW-HDS-001 -- Hardware Design Specification

**Project:** TW-SAP1 Hardware Platform\
**Product:** XS3400 Residential Smart Lock\
**Revision:** A (Draft)

## 1. Scope

Defines the hardware implementation requirements for the TW-SAP1 main
controller board.

## 2. Main PCB

  Parameter   Specification
  ----------- ---------------------------------------
  PCB Size    65 mm × 45 mm
  Layers      4
  Finish      ENIG
  Thickness   1.6 mm
  Copper      1 oz
  Assembly    SMT, components primarily on top side

Bottom side is reserved for capacitive touch electrodes.

## 3. Core Components

  Function           Selected Component
  ------------------ --------------------
  MCU                ESP32-C6-MINI-1
  Fingerprint        Hi-Link HLK-ZW101
  Touch Controller   Microchip MTCH2120
  Motor Driver       TI DRV8833
  Buck Regulator     TI TPS62840
  Load Switch        TI TPS22916
  USB ESD            ST USBLC6-2SC6

## 4. Power

-   4 × AA alkaline batteries
-   USB-C emergency power only
-   3.3 V logic rail
-   Separate motor supply routing

## 5. Interfaces

-   UART: Fingerprint module
-   I²C: MTCH2120
-   PWM/GPIO: Motor driver
-   ADC: Battery monitoring
-   SWD/UART pads: Debug and programming

## 6. Mechanical Interfaces

-   MinebeaMitsumi actuator (preferred)
-   Dormount Euro profile cylinder (Phase 1)
-   Hidden capacitive keypad
-   Tempered glass front panel

## 7. Excluded Features

-   RFID
-   NFC
-   OLED
-   Battery charging

## 8. Design Rules

-   RF antenna keep-out for ESP32-C6
-   Decoupling capacitor at every IC power pin
-   Ground stitching vias
-   JLCPCB-compatible footprints where possible

## 9. Revision Control

Changes to frozen components or interfaces require an engineering change
review before implementation.
