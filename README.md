# 🤖 Arduino Obstacle Avoiding Robot

An Arduino-based autonomous robot that detects obstacles using an ultrasonic sensor and automatically changes direction to avoid collisions. The robot uses a motor driver shield to control four DC motors and a servo motor to scan the surroundings.


<img width="1280" height="580" alt="image" src="https://github.com/user-attachments/assets/ac80403b-5453-4273-91ac-8f526aa1b578" />


## 📌 Project Overview

The Obstacle Avoiding Robot is an autonomous robotics project designed to navigate its environment without continuous human control. It measures the distance between the robot and nearby objects using an ultrasonic sensor. When an obstacle is detected, the robot stops, moves backward, scans both sides, and turns toward the direction with more available space.

## ✨ Features

- 🚗 Autonomous movement and navigation
- 📡 Ultrasonic obstacle detection
- 🔄 Servo-based left and right scanning
- ↩️ Automatic backward movement when obstacles are detected
- ↪️ Intelligent turning based on measured distances
- ⚙️ Four-motor control using an Arduino motor shield
- 💻 Programmable using the Arduino IDE

## 🧰 Hardware Requirements

| Component | Quantity |
|---|---:|
| Arduino Uno | 1 |
| L293D-compatible motor driver shield | 1 |
| HC-SR04 ultrasonic sensor | 1 |
| SG90 or compatible servo motor | 1 |
| DC geared motors | 4 |
| Robot chassis with wheels | 1 |
| Battery pack suitable for the motors | 1 |
| Jumper wires | As required |

## 🔌 Pin Configuration

The following pin configuration is based on the supplied Arduino code.

| Component | Arduino Pin |
|---|---|
| Ultrasonic TRIG | A0 |
| Ultrasonic ECHO | A1 |
| Servo signal | D10 |
| Motor 1 | M1 |
| Motor 2 | M2 |
| Motor 3 | M3 |
| Motor 4 | M4 |

**Note:** The current code uses A0 and A1 for the ultrasonic sensor. If you modify the code to use A4 and A5, update the wiring accordingly. Verify that the chosen pins are not occupied by your particular shield.

## 📚 Required Libraries

Install these libraries in the Arduino IDE before compiling the program:

1. **AFMotor** — for controlling motors through compatible Adafruit-style motor shields.
2. **NewPing** — for ultrasonic distance measurement.
3. **Servo** — for controlling the servo motor.

### Installation

1. Open the Arduino IDE.
2. Navigate to **Sketch → Include Library → Manage Libraries**.
3. Search for and install the available NewPing and Servo libraries.
4. Install the compatible AFMotor library for your motor shield, following its documentation.
5. Restart the Arduino IDE if necessary.

Reference links:

- AFMotor: https://learn.adafruit.com/adafruit-motor-shield/library-install
- NewPing: https://github.com/livetronic/Arduino-NewPing
- Servo: https://github.com/arduino-libraries/Servo

## ⚙️ How It Works

1. **Initialization:** The Arduino initializes the motors, ultrasonic sensor, and servo position.
2. **Distance measurement:** The ultrasonic sensor measures the distance to objects ahead.
3. **Obstacle detection:** When the measured distance is 15 cm or less, the robot initiates its avoidance routine.
4. **Reverse movement:** The robot stops and moves backward briefly.
5. **Environment scanning:** The servo points the ultrasonic sensor toward the right and left to measure available space.
6. **Direction selection:** The robot compares the measured distances and chooses the side with more space.
7. **Turning:** The motors rotate in the required directions to turn the robot.
8. **Continuous navigation:** The robot resumes forward movement and repeats the process.

## 🚀 Getting Started

### Step 1: Clone the Repository

Replace `YOUR_USERNAME` and `YOUR_REPOSITORY` with your GitHub username and repository name.

```bash
git clone https://github.com/YOUR_USERNAME/YOUR_REPOSITORY.git
cd YOUR_REPOSITORY
```

### Step 2: Open the Project

Open the `.ino` file in the Arduino IDE.

### Step 3: Connect the Hardware

Connect the ultrasonic sensor, servo motor, motor shield, and DC motors according to the pin configuration and the wiring of your actual hardware.

### Step 4: Select the Board

In the Arduino IDE, select the appropriate Arduino board and COM port.

### Step 5: Upload the Code

Click **Verify** to compile the sketch, then click **Upload** to flash the program to the Arduino.

### Step 6: Test the Robot

Place the robot on a flat, open surface. Power it using a suitable battery supply and place an obstacle in front of it to test the detection and turning behavior.

## 🧠 Technologies Used

- Arduino C/C++
- Arduino Uno
- Ultrasonic sensing
- DC motor control
- Servo motor control
- Embedded systems
- Autonomous robotics

## 🔧 Troubleshooting

| Problem | Possible Solution |
|---|---|
| Robot moves in circles | Check the motor wiring, motor orientation, and forward/reverse commands. |
| Robot moves backward instead of forward | Correct the direction commands for the affected motors. |
| Ultrasonic sensor does not detect obstacles | Check the TRIG and ECHO wiring, sensor power, and pin definitions. |
| Servo does not rotate | Check the servo signal pin, power supply, and ground connection. |
| Motors do not run properly | Verify the motor shield compatibility, battery supply, and motor connections. |
| Compilation error: `AFMotor.h` not found | Install a compatible AFMotor library and confirm that the shield is supported. |

## 🔮 Future Improvements

- Add Bluetooth or Wi-Fi remote control.
- Integrate an ESP32 for wireless monitoring.
- Add an LCD or OLED display for distance measurements.
- Implement more advanced obstacle-avoidance algorithms.
- Add battery-level monitoring.
- Integrate mapping and navigation capabilities.

## 🎯 Applications

- Educational robotics projects
- Embedded systems learning
- Autonomous mobile robots
- Robotics and automation demonstrations
- Engineering mini-projects

## 👨‍💻 Author

**Harsha Vardhan Raju Yerra**

Cybersecurity Enthusiast | Ethical Hacking | IoT & Hardware Security

## 📄 License

This project is intended for educational and personal learning purposes. You may add an open-source license, such as the MIT License, if you want to permit others to reuse and modify the code under its terms.

## ⭐ Support

If you find this project useful, consider giving the repository a ⭐ on GitHub!

---

*Built with Arduino, sensors, motors, and a passion for robotics.* 🤖
