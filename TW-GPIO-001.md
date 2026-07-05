# TW-GPIO-001 -- ESP32-C6 GPIO Allocation

**Project:** TW-SAP1 Hardware Platform\
**Product:** XS3400 Residential Smart Lock\
**Revision:** A (Draft)

> **Status:** Preliminary allocation. Final pin numbers will be frozen
> during schematic capture after verifying ESP32-C6 boot-strap and
> reserved pins.

## GPIO Allocation

  Function          Interface   Preferred GPIO   Notes
  ----------------- ----------- ---------------- ------------------------
  Fingerprint TX    UART        TBD              UART to HLK-ZW101
  Fingerprint RX    UART        TBD              UART from HLK-ZW101
  Touch SDA         I²C         TBD              MTCH2120
  Touch SCL         I²C         TBD              MTCH2120
  Motor IN1         GPIO/PWM    TBD              DRV8833
  Motor IN2         GPIO/PWM    TBD              DRV8833
  Buzzer            GPIO/PWM    TBD              Audible feedback
  Battery Voltage   ADC         TBD              Divider network
  USB Detect        GPIO        TBD              Emergency power detect
  Wake Input        GPIO        TBD              Low-power wake
  Status Output     GPIO        TBD              Future use
  Debug TX/RX       UART        TBD              Programming & logs

## Reserved Functions

-   Boot strap pins
-   RF antenna keep-out
-   Future Matter/Thread expansion
-   Manufacturing test pads

## Rules

1.  Avoid using ESP32-C6 boot configuration pins for external circuits.
2.  Keep UART dedicated to the fingerprint module.
3.  Use one shared I²C bus for low-speed peripherals.
4.  Reserve at least two spare GPIOs for future features.
5.  Document every GPIO change through revision control.

## Next Step

Freeze the exact GPIO numbers during schematic capture and update this
document before PCB routing.
