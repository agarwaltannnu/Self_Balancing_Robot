# Self-Balancing Robot 🤖

A two-wheeled self-balancing robot built using Arduino UNO, MPU6050, and DC motors. The robot continuously measures its tilt angle and uses a PID controller to adjust motor speed, allowing it to maintain balance in real time.

This project was developed to understand embedded systems, sensor integration, and feedback control using PID.

![Arduino](https://img.shields.io/badge/Platform-Arduino%20UNO-blue?style=flat-square)
![Embedded C](https://img.shields.io/badge/Language-Embedded%20C-green?style=flat-square)
![Control System](https://img.shields.io/badge/Control-PID-orange?style=flat-square)

---

## Overview

The robot uses an MPU6050 sensor to measure its tilt angle and continuously compares it with the desired upright position. Based on the error, the PID controller calculates the required motor correction and adjusts the motor speed, helping the robot maintain its balance.

---

## Features

- Real-time balancing using PID control
- Tilt measurement using MPU6050
- PWM-based motor speed control
- Arduino UNO based implementation
- Compact two-wheel robot design

---

##  Tech Stack

- **Microcontroller:** Arduino UNO
- **Programming Language:** Embedded C (Arduino IDE)
- **Sensor:** MPU6050 IMU
- **Motor Driver:** L293D
- **Control Algorithm:** PID Controller

  ---

## How It Works

```
Tilt Sensor (MPU6050)
        ↓
Calculate Error (Target Angle - Current Angle)
        ↓
PID Algorithm computes correction
        ↓
Motor Driver adjusts wheel speed
        ↓
Robot maintains balance ✓
```

### Control Loop
1. **Read** tilt angle from MPU6050
2. **Calculate** error from desired angle
3. **Apply PID** to compute motor correction
4. **Adjust** motor speeds via PWM
5. **Repeat** at high frequency (~100 Hz)

---

## Hardware Requirements

| Component | Quantity | Purpose |
|-----------|----------|---------|
| Arduino UNO | 1 | Microcontroller |
| MPU6050 | 1 | Accelerometer + Gyroscope |
| L293D Motor Driver | 1 | DC Motor control |
| DC Motors | 2 | Robot wheels |
| Li-ion Battery | 1 | Power supply |
| Chassis | 1 | Mechanical frame |

---

## Wiring Connections

**MPU6050 to Arduino:**
- VCC → 5V
- GND → GND
- SCL → A5
- SDA → A4

**L293D to Arduino:**
- IN1, IN2 → D3, D4
- IN3, IN4 → D5, D6
- Motor connections to OUT1-OUT4

---

## Installation & Setup

### 1. Clone Repository
```bash
git clone https://github.com/agarwaltannnu/Self_Balancing_Robot.git
cd Self_Balancing_Robot
```

### 2. Install Arduino IDE
Download from [arduino.cc](https://www.arduino.cc/en/software)

### 3. Install Required Libraries
- MPU6050 library (by ITead)
- Search in Arduino IDE: Sketch → Include Library → Manage Libraries

### 4. Upload Code
1. Connect Arduino to computer via USB
2. Select Board: Tools → Board → Arduino UNO
3. Select Port: Tools → Port
4. Click Upload button

---

## Calibration Tips

- **Offset Calibration**: Place robot on flat surface before startup
- **PID Tuning**: Adjust Kp, Ki, Kd values based on response
  - High Kp → Faster response (may oscillate)
  - High Ki → Reduces steady-state error
  - High Kd → Reduces oscillation
- **Sensor Range**: Ensure MPU6050 is leveled ±90°

---

## Challenges Faced

- Reduced sensor noise by filtering IMU readings.
- Tuned PID parameters to improve balancing performance.
- Calibrated the motors for smoother movement.
- Optimized power supply for stable operation.

---

## Future Enhancements

-  **Wireless Control** - Bluetooth/WiFi remote operation
-  **Obstacle Detection** - Add ultrasonic sensors
-  **Mobile App** - Real-time control interface
-  **Path Following** - Navigate autonomously
-  **Data Logging** - Record tilt angles and motor speeds

---



## What I Learned

Working on this project helped me gain hands-on experience in:
- **Control Systems**: Understanding PID controllers
- **Embedded Programming**: Arduino development
- **Sensor Integration**: Working with IMU sensors
- **Real-time Systems**: Time-critical feedback loops
- **Hardware-Software Integration**: Bridging electronics & code

---


## Project

A collaborative group project in robotics and embedded systems.

GitHub: [@agarwaltannnu](https://github.com/agarwaltannnu)

---
