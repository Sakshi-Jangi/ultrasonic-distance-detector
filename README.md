# 📏 Ultrasonic Distance Detector – Arduino + HC-SR04

An Arduino-based obstacle detection system using an HC-SR04 ultrasonic sensor. The device measures distance in real time and provides LED + buzzer alerts based on proximity — ideal for robotics and indoor navigation.

---

## 🔧 Components

- Arduino UNO  
- HC-SR04 Ultrasonic Sensor  
- Red, Yellow, Green LEDs  
- Buzzer  
- Breadboard, Resistors, Jumper Wires  
- Power Source (USB or 9V)

---

## ⚙️ Working Principle

The HC-SR04 emits ultrasonic pulses and measures the time they take to return. The Arduino calculates the distance and triggers alerts:

| Distance        | Indicator           |
|----------------|---------------------|
| < 10 cm         | Red LED + fast beep |
| 10–20 cm        | Yellow LED + slow beep |
| > 20 cm         | Green LED only      |

```cpp
duration = pulseIn(echoPin, HIGH);
distance = duration * 0.034 / 2;
✅ Features
Real-time distance sensing (5–30 cm range)

Buzzer + LED alert system based on object proximity

Compact design for robotics and smart devices

Tested with ±2 cm accuracy in indoor conditions

Built as a practical IoT and embedded systems project using Arduino.
