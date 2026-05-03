# Automated Solar Grass Cutter

Arduino project for a solar-powered grass cutting robot with RemoteXY control.

## Features
- Manual, automatic, and area modes
- Mobile control via RemoteXY
- Ultrasonic obstacle detection

## Requirements
- Arduino board compatible with the current pin mapping
- ESP8266 (hard serial point) for RemoteXY
- RemoteXY library 3.1.8 or later

## Setup
1. Install the RemoteXY library from http://remotexy.com/en/library/
2. Open the sketch in the Arduino IDE.
3. Update WiFi settings in the RemoteXY config section.
4. Connect the motor drivers, ultrasonic sensors, and cutting motor per the pin map in the sketch.
5. Upload and test.

## Pin Map (from sketch)
- Drive motors: `up_r_p`, `up_r_n`, `up_l_p`, `up_l_n`, `down_r_p`, `down_r_n`, `down_l_p`, `down_l_n`
- Ultrasonic: `trig_f`, `echo_f`, `trig_r`, `echo_r`, `trig_l`, `echo_l`
- Cutting motor: `cutting`

## Diagram
- [Grass RC.pdf](Grass%20RC.pdf)

## Notes
- Manual mode uses the joystick to drive.
- Automatic mode drives forward and avoids obstacles.
- Area mode cuts a rectangular area based on X/Y input.
