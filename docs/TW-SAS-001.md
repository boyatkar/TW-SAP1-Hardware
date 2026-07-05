# TW-SAS-001 -- System Architecture Specification

**Project:** TW-SAP1 Hardware Platform\
**Product:** XS3400 Residential Smart Lock\
**Revision:** A (Draft)

## 1. Purpose

This document defines the overall hardware architecture and subsystem
interactions for the TW-SAP1 platform.

## 2. System Overview

The ESP32-C6-MINI-1 is the central controller and communicates with: -
HLK-ZW101 fingerprint module (UART) - MTCH2120 capacitive touch
controller (I²C) - DRV8833 motor driver (GPIO/PWM) - Battery monitor
(ADC) - USB-C emergency power interface - XSOS mobile application over
BLE/Wi-Fi

## 3. Authentication Methods

-   Fingerprint
-   PIN (capacitive keypad)
-   XSOS mobile application
-   Mechanical key override

## 4. Power Architecture

Input: - 4 × AA alkaline batteries - USB-C emergency power (no charging)

Power rails: - 3.3 V logic - Motor supply - Switched peripheral rail

## 5. PCB Architecture

-   Board size: 65 × 45 mm
-   4-layer PCB
-   Components on top side
-   Capacitive electrodes on bottom side
-   RF keep-out for ESP32-C6 antenna

## 6. Mechanical Interfaces

-   MinebeaMitsumi actuator
-   Dormount Euro profile cylinder
-   Hidden capacitive keypad
-   HLK-ZW101 front-mounted fingerprint sensor

## 7. Future Expansion

Reserved for: - Matter - Thread - Additional sensors - RFID/NFC variants
on future products

## 8. Revision Policy

All architectural changes require documentation updates before schematic
changes are implemented.
