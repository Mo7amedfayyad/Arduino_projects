# Smart Traffic

Arduino traffic light controller with gas/air quality alarm and LDR-based lighting control.

## Features
- Two-direction traffic light control
- Optional manual override based on serial input values
- Gas sensor alarm using a buzzer
- LDR-based relay control for lighting

## Requirements
- Arduino board compatible with the current pin mapping
- Gas sensor (digital output)
- LDR connected to analog input
- Relay module for lighting control
- Optional: CVZone SerialData support

## Setup
1. Connect LEDs and sensors according to the pin map below.
2. If using CVZone SerialData, install the library and enable the serial data code.
3. Upload the sketch and monitor the serial output for LDR values.

## Modes (valsRec[0])
- 0: Normal traffic cycle
- 1: Car in front (front direction green)
- 2: Car beside (beside direction green)
- 3: Ambulance in front (front direction green)
- 4: Ambulance beside (beside direction green)

## Pin Map (from sketch)
- Traffic light 1: `red1Pin`=2, `yellow1Pin`=3, `green1Pin`=4
- Traffic light 2: `red2Pin`=5, `yellow2Pin`=6, `green2Pin`=7
- Gas sensor: `gas`=8
- Buzzer: `buzz`=13
- LDR: `ldr`=A0
- Relay: `relay`=11

## Diagram
- [smart_traffic.PDF](smart_traffic.PDF)

## Notes
- Gas alarm activates the buzzer when the gas input is LOW.
- LDR controls the relay when the analog value drops below the threshold.
