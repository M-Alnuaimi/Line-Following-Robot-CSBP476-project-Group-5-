# Line-Following-Robot-CSBP476-project-Group-5-

![IMG_1938](https://github.com/user-attachments/assets/1c8a36b2-47f9-45e7-be16-c3c5d5419dbe)


## Project Overview

This project demonstrates an autonomous robot built with the Keyestudio 4WD BT V2.0 kit. The robot is designed to follow a black line on a white surface using three IR sensors. It adjusts its movement in real-time, turning left, right, or moving forward depending on sensor readings. A matrix LED display shows a smile animation at startup for visual feedback.

The project also includes a phased control system using the `check` variable to manage different stages of behavior, such as switching between black line and white line tracking or stopping the robot completely.

---

## Contents of this Repository

1. `Phase2_Track.ino`: Arduino source code for the robot logic and control.
2. `flowchart.png`: A visual representation of the program logic.
3. `YouTube Link`: Watch it in action here: https://youtube.com/shorts/qs54Gwclo1M?si=-gnwLul96XwYGdsv

---

## Flowchart
![Flowchart](https://github.com/user-attachments/assets/d9c31942-6058-48e1-b516-e01159a8631f)

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
<img width="326" alt="image" src="https://github.com/user-attachments/assets/66501bb2-365c-4b5c-956d-a198e33cb18a" />

- Kit Link: https://www.amazon.ae/KEYESTUDIO-Programmable-Robotics-Electronics-Educational/dp/B0BCQ9TGY5/ref=asc_df_B0BCQ9TGY5?mcid=4f07f29b9dde399299cab133cef5a4bd&tag=googleshopp09-21&linkCode=df0&hvadid=719122129168&hvpos=&hvnetw=g&hvrand=12429762043085446816&hvpone=&hvptwo=&hvqmt=&hvdev=c&hvdvcmdl=&hvlocint=&hvlocphy=9215881&hvtargid=pla-1965034975616&psc=1&gad_source=1
---

## Team Members

- Mohammed Alnuaimi
- Ahmed Alsenaani
- Ahmed Almasiyuli

---

## How to Run

1. Connect the robot to your computer via USB.
2. Upload `Phase2_Track.ino` to the Arduino Uno using the Arduino IDE.
3. Place the robot on a black-line track.
4. Turn on the power and observe the robot follow the track autonomously.


