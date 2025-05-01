# Line-Following-Robot-CSBP476-project-Group-5-

![Robot Image](https://www.keyestudio.com/image/cache/catalog/KS0559/KS0559%20(1)-750x750.jpg)

## Project Overview

This project demonstrates an autonomous robot built with the Keyestudio 4WD BT V2.0 kit. The robot is designed to follow a black line on a white surface using three IR sensors. It adjusts its movement in real-time, turning left, right, or moving forward depending on sensor readings. A matrix LED display shows a smile animation at startup for visual feedback.

The project also includes a phased control system using the `check` variable to manage different stages of behavior, such as switching between black line and white line tracking or stopping the robot completely.

---

## Contents of this Repository

1. `main.ino`: Arduino source code for the robot logic and control.
2. `flowchart.png`: A visual representation of the program logic.
3. `demo_video.mp4`: Demo of the robot in action.
4. `YouTube Link`: Watch it in action here: [YouTube Demo](https://youtu.be/YOUR_VIDEO_LINK)

---

## Flowchart

![Flowchart](flowchart.png)

### Flowchart Description:

1. **Start**: Initialize sensors, motors, and display a smiley face on the LED matrix.
2. **Read Sensors**: IR sensors detect the line status.
3. **Check Phase**: The `check` variable determines the logic path:
   - `check = 0`: Start normal black line tracking.
   - `check = 1`: Switch to white line tracking mode.
   - `check = 2`: Return to black line mode and stop at the finish.
   - `check = 3`: Stop the robot.
4. **Tracking Logic**:
   - If only the middle sensor sees black → move forward.
   - If left detects black → turn left.
   - If right detects black → turn right.
   - If no sensor detects black → turn right (default recovery).
5. **Stop**: Robot stops after completing all tracking phases.

---

## Features

- **Multi-phase logic** to control movement across different stages.
- **IR line detection** using left, middle, and right sensors.
- **PWM motor control** for precise directional movement.
- **Matrix display animation** for start-up feedback.
- **Supports black and white line tracking**.

---

## Hardware Components

- Keyestudio 4WD BT V2.0 Robot Kit
- Arduino Uno R3
- 3 x Infrared Tracking Sensors
- L298N Motor Driver Module
- Dot Matrix LED Display
- Motor Driver Shield
- Power Supply (batteries)
- Jumper Wires

---

## Team Members

- Mohammed Alnuaimi
- [Add team members here if applicable]

---

## How to Run

1. Connect the robot to your computer via USB.
2. Upload `main.ino` to the Arduino Uno using the Arduino IDE.
3. Place the robot on a black-line track.
4. Turn on the power and observe the robot follow the track autonomously.

---

## License

This project is for educational use. You are free to modify and distribute it under the MIT License.


