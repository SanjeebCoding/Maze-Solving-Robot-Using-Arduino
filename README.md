# 🤖 Maze Solving Robot using Arduino (Left-Hand Rule)

An autonomous **Maze Solving Robot** built using **Arduino UNO**, **IR sensors (LM393)**, and **L293D motor driver**, capable of navigating a line-based maze using the **Left-Hand Rule algorithm** without any human intervention.

---

## 📌 Project Overview

This project demonstrates a cost-effective and intelligent robotic system that can automatically detect paths, make decisions at intersections, and successfully navigate through a maze.
The robot continuously senses its environment using infrared sensors and controls its movement using DC motors driven by an L293D motor driver.

The decision-making logic is based on the **Left-Hand Rule**, a deterministic maze-solving algorithm.

---

## 🎯 Key Features

* 🔁 Fully autonomous maze navigation
* 📡 Real-time path detection using IR sensors
* 🧠 Decision-making using Left-Hand Rule algorithm
* 🔄 Automatic U-turn at dead ends
* ⚙️ Simple, low-cost, and beginner-friendly design
* 🧪 Ideal for hackathons, academic projects, and robotics learning

---

## 🧠 Algorithm Used – Left-Hand Rule

The Left-Hand Rule follows a simple logic:

1. **Turn Left** if a left path is available
2. **Go Straight** if left is not available
3. **Turn Right** if left and straight are blocked
4. **U-Turn** if all paths are blocked (dead end)

This guarantees maze traversal for connected mazes.

---

## 🧩 Components Used

| Component                   | Quantity    |
| --------------------------- | ----------- |
| Arduino UNO / UNO + WiFi R3 | 1           |
| IR Sensors (LM393)          | 3           |
| L293D Motor Driver Module   | 1           |
| DC Geared Motors            | 2           |
| Robot Chassis with Wheels   | 1           |
| Battery Pack (7–12V)        | 1           |
| Jumper Wires                | As required |
| Power Switch                | 1           |
| Caster Wheel                | 1           |

---

## ⚡ Circuit Connections

### IR Sensors

| Sensor    | Arduino Pin |
| --------- | ----------- |
| Left IR   | A0          |
| Center IR | A1          |
| Right IR  | A2          |

### Motor Driver (L293D)

| Function          | Arduino Pin |
| ----------------- | ----------- |
| Motor A IN1       | D8          |
| Motor A IN2       | D9          |
| Motor B IN3       | D10         |
| Motor B IN4       | D11         |
| Motor Speed (PWM) | D5, D6      |

> ⚠️ Ensure **common ground** between Arduino, motor driver, and battery.

---

## 🏗️ Robot Structure

* Differential drive system (2 DC motors)
* IR sensors mounted at the front bottom
* Arduino + Motor Driver mounted on chassis
* Battery placed at center for balance

```
[ IR Sensors ]
     |
[ Arduino UNO ]
     |
[ L293D Driver ]
   |       |
[Motor] [Motor]
```

---

## 🧪 Working Principle

* IR sensors detect black lines by infrared reflection
* Sensor data is sent to Arduino
* Arduino applies Left-Hand Rule logic
* Motor driver controls direction & speed
* Robot continuously adapts until maze exit is reached

---

## 📂 Repository Structure

```
Maze-Solving-Robot/
│
├── MAZE_Solving_Robot.ino     # Arduino source code
├── README.md                 # Project documentation
├── Robot Moving Video.mp4    # Working demo video
├── Circuit_Diagram.png       # Circuit diagram (optional)
├── Images/                   # Robot images (optional)
└── Docs/                     # Project report / PDF
```

---

## ▶️ Demo Video

🎥 **Robot Working Demonstration**

https://github.com/user-attachments/assets/1bb24303-48e0-471c-867e-bff414b3e58e

---

## 🚀 How to Run the Project

1. Assemble the robot hardware
2. Connect all components as per circuit
3. Upload `MAZE_Solving_Robot.ino` using Arduino IDE
4. Place robot on a line maze
5. Power ON and watch it solve the maze 🤖✨

---

## 🧠 Learning Outcomes

* Embedded systems programming
* Sensor integration
* Motor control using H-Bridge
* Autonomous navigation logic
* Debugging real-world robotic systems

---

## 📈 Future Improvements

* PID-based line following
* Shortest path optimization
* WiFi/Bluetooth monitoring
* Camera-based vision navigation
* OLED display for status

---

## 📚 References

* Arduino Official Docs – [https://www.arduino.cc](https://www.arduino.cc)
* Hackster.io Maze Robot Projects
* Arduino Project Hub
* YouTube Robotics Tutorials
