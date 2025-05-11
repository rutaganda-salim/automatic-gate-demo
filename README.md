# 🚪 Ultrasonic Sensor-Based Gate Controller  

This project uses an Arduino to control a servo-operated gate with an **HC-SR04 ultrasonic sensor**. When an object (like a person) is detected within a range of **50cm**, the gate opens (servo rotates), a **blue LED illuminates**, and a **buzzer emits a soft beep**. If no object is detected for **5 seconds**, the gate closes, and a **red LED lights up**.  

---

## 📦 **Hardware Requirements**  
### **Components List**  
- Arduino (Uno or Nano)  
- HC-SR04 Ultrasonic Sensor  
- SG90 Servo Motor  
- Red and Blue LEDs (with ~220Ω resistors)  
- Passive Buzzer  
- Jumper Wires  

### **Connection Details**  
| Component       | Arduino Pin |
|----------------|------------|
| HC-SR04 Trigger | D2         |
| HC-SR04 Echo    | D3         |
| Red LED (Anode) | D4         |
| Red LED (Cathode) | D8        |
| Blue LED (Cathode) | D7       |
| Blue LED (Anode) | D5         |
| Servo Signal    | D6         |
| Buzzer (+)      | D12        |

> **Tip:** Ensure all components share a common ground (`GND`).  

---

## ⚙️ **Software Setup Instructions**  
### **1. Install the Servo Library**  
The project uses the **Servo library**, which is included by default in the Arduino IDE. If it’s missing:  
- Open Arduino IDE → **Sketch → Include Library → Manage Libraries** → Search for **"Servo"** → Install.  

### **2. Upload the Code**  
1. Copy the provided code into a new Arduino sketch.  
2. Select your board model (**Tools → Board → Arduino Uno/Nano**).  
3. Choose the correct port (**Tools → Port**).  
4. Click the **Upload** button (▶️).  

---

## 🎛️ **How It Operates**  
- **Object Detection**: The ultrasonic sensor measures distance, and if an object is within **50cm**, it triggers the gate.  
- **Gate Mechanism**:  
  - **Opening**: The servo rotates to **90°**, the blue LED turns on, and the buzzer emits soft beeps.  
  - **Closing**: After **5 seconds** without detection, the servo returns to **0°**, and the red LED lights up.  
- **Buzzer Behavior**: Emits short beeps (**50ms ON, 500ms cycle**) while the gate is open.  

---

## 🔧 **Common Issues and Fixes**  
- **Servo movement is erratic**: Check the power supply; use an external power source if necessary.  
- **Ultrasonic sensor not responding**: Verify the wiring (`Trigger` → `D2`, `Echo` → `D3`).  
- **LEDs not functioning**: Double-check polarity and resistor values.  

---

## 📜 **License**  
This project is licensed under the MIT License. Feel free to use, modify, and share it.  

**Happy Building!** 💻⚡  

---
