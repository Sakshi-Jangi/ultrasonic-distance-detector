# 📏 Ultrasonic Distance Detector – Proximity Warning System

This project implements a real-time distance measuring and obstacle alert system using the **HC-SR04 ultrasonic sensor** and **Arduino UNO**. Visual (LEDs) and auditory (buzzer) indicators provide feedback based on how close an object is.

---

## 🛠 Components Used

- Arduino UNO board  
- HC-SR04 Ultrasonic Sensor  
- Red, Yellow, Green LEDs  
- Buzzer  
- Breadboard and jumper wires  
- 9V Battery or USB power

---

## 💡 Working Principle

The **HC-SR04 sensor** sends out an ultrasonic pulse and measures the time it takes to bounce back from a nearby object. The Arduino calculates the distance using:

Distance = (Time × Speed of Sound) / 2

yaml
Copy
Edit

Based on the measured distance:
- 🟥 **Red LED** + Fast buzzer beep for close objects
- 🟨 **Yellow LED** + Slow beep for medium range
- 🟩 **Green LED** + No buzzer for safe distance

---

## ✅ Features

- Accurate measurement of distance using ultrasonic reflection  
- Buzzer and LED indicators for real-time feedback  
- Useful in robotics, parking sensors, obstacle avoidance  
- Simple design and easy implementation on Arduino

---

## 📐 Observations from Testing

- Distance range tested: **5 cm to 30 cm**
- Results were consistent with an error margin of ±2 cm
- Sensor performed well in indoor environments

---

## 🔧 Sample Arduino Code Snippet

```cpp
digitalWrite(trigPin, LOW);
delayMicroseconds(2);
digitalWrite(trigPin, HIGH);
delayMicroseconds(10);
digitalWrite(trigPin, LOW);

duration = pulseIn(echoPin, HIGH);
distance = duration * 0.034 / 2;
A practical project to demonstrate ultrasonic sensing, Arduino programming, and simple embedded control logic. Ideal for students and beginners in IoT/robotics.
