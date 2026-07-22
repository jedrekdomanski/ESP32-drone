# ESP32 Quadrotor Drone

A custom-built, Wi-Fi-controlled quadcopter powered by the ESP32 microcontroller. This project is inspired by and builds upon the DIY drone architecture featured on [Circuit Digest](https://circuitdigest.com/microcontroller-projects/DIY-wifi-controlled-drone).

---

## 📌 Project Overview

The goal of this project is to build an affordable, open-source, and fully functional quadrotor drone from scratch. Utilizing the dual-core processing capabilities and built-in Wi-Fi of the ESP32, the drone processes sensor data in real-time for flight stabilization while receiving wireless flight controls directly from a web interface or mobile app.

---

## ✨ Key Features

* **ESP32 Core Brain:** High-performance, low-cost microcontroller handling sensor fusion, control loops (PID), and wireless communication.
* **Wi-Fi Control:** Real-time remote control over Wi-Fi (hosted via ESP32 Access Point mode or local network).
* **IMU Stabilization:** 6-axis Motion Tracking (MPU6050 accelerometer + gyroscope) for attitude estimation and stable hovering.
* **PID Flight Control:** Custom implementation of Roll, Pitch, and Yaw stabilization loops.
* **Lightweight Architecture:** Minimalist DIY frame design tailored for high power-to-weight ratio.

---

## 🛠️ Hardware Requirements

* **Microcontroller:** ESP32 Development Board
* **IMU Sensor:** MPU6050 (6-DOF Gyroscope + Accelerometer)
* **Motors:** 4x Coreless Brushed Motors (or Brushless Motors with ESCs)
* **Propellers:** 2x CW and 2x CCW Propellers
* **Motor Drivers / ESCs:** MOSFET switching circuit or dedicated ESCs depending on motor type
* **Power Source:** 1S / 2S LiPo Battery with suitable voltage regulators
* **Frame:** Custom 3D-printed or lightweight carbon fiber/plastic frame

---

## 📐 System Architecture & Flight Dynamics

1. **Sensor Data Acquisition:** Reads raw gyroscope and accelerometer data via I2C from the MPU6050.
2. **Attitude Calculation:** Uses a Complementary or Kalman filter to compute precise Roll, Pitch, and Yaw angles.
3. **Control Loop:** Processes error signals between user commands and current attitude using a PID controller.
4. **Motor Output:** Generates dynamic PWM signals sent to the motors/ESCs to maintain balance and respond to control inputs.

