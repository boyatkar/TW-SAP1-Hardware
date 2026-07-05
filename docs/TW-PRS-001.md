# TW-PRS-001 -- Product Requirements Specification

**Project:** TW-SAP1 Hardware Platform\
**Product:** XS3400 Residential Smart Lock\
**Status:** Draft Rev A

## 1. Objective

Develop a premium residential smart lock platform optimized for
reliability, manufacturability, and future scalability.

## 2. Frozen Architecture

### Electronics

-   MCU: ESP32-C6-MINI-1
-   Fingerprint: Hi-Link HLK-ZW101
-   Capacitive Touch: Microchip MTCH2120
-   Motor Driver: TI DRV8833
-   Buck Regulator: TI TPS62840
-   Load Switch: TI TPS22916
-   USB ESD: ST USBLC6-2SC6

### Authentication

-   Fingerprint
-   PIN (Hidden Capacitive Keypad)
-   Mobile App (XSOS)
-   Mechanical Key

### Excluded from Rev A

-   RFID
-   NFC
-   OLED
-   Battery charging

## 3. Mechanical

-   PCB Size: 65 mm × 45 mm
-   PCB Layers: 4
-   Components: Top side
-   Bottom: Capacitive touch electrodes
-   USB-C: Emergency power only

## 4. Preferred Mechanical Components

-   Actuator: MinebeaMitsumi (Japan)
-   Euro Cylinder: Dormount (Phase 1)

## 5. Product Goals

-   Premium residential experience
-   Low standby power
-   Future Matter-ready architecture
-   JLCPCB prototype friendly
-   Designed for BIS/WPC certification

## 6. Repository

This document is the baseline engineering specification for TW-SAP1 Rev
A.
