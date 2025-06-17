# <h1 align="center"> ZHANYM </h1> 

This repository showcases the journey and development of our robot created for the **2025 World Robot Olympiad – Future Engineers** category.

We are **Team Zhanym WRO2025**, a duo of passionate and driven girls who designed, engineered, and built this robot from the ground up.

Here, you'll find all the documentation, design insights, and technical details behind our project.

<p align="center">
  <img src="other/LOGO.jpg" alt="Team Logo" width="300"/>
</p>


## Team Members 
### Khanbay Aigerim
Hello! 👋

My name is **Aigerim**, and I am **17 years old**.

This is my **second adventure** in the **WRO (World Robot Olympiad)** — a journey that fuels my passion for innovation and technology.

My first experience was back in **Grade 9**, when I took on the challenge of the **RoboMission category (Senior Division)**.  
That experience sparked my love for robotics and teamwork.

Now, I'm excited to take things to the next level as I dive into the **Future Engineers** category — where creativity, design, and real-world engineering come together! 🚀
.

<img src="t-photos/Aigerim.jpg" alt="Aigerim" width="300"/>


### Zharas Zhanuya
Hi! 👋

I’m **Zhanuya**, a **16-year-old student** passionate about **engineering**, **coding**, and **hands-on problem solving**.

I love working on tech projects that combine **hardware and creativity**.

Last year, I competed in the **WRO Future Engineers** category,  
and I’m excited to keep learning and building in this category! 🚀

<img src="t-photos/Zhanuya.jpg" alt="Zhanuya" width="300"/>


### 👨‍🏫 Mentor: Mister Askar
Hello! My name is **Askar**, and I am the **mentor** of this amazing team.

I’m truly happy to work with such talented and motivated students who are passionate about engineering, creativity, and robotics.

Guiding them through challenges and helping them grow is a privilege and a joy.

I also work at **Nazarbayev Intellectual School (NIS)** in **Atyrau**, where I support young minds in exploring STEM fields and developing real-world problem-solving skills.

<img src="t-photos/askar-mentor.jpg" alt="Askar - Mentor" width="300"/>

---

## Autonomous Robotic Vehicle

This autonomous robotic vehicle is capable of self-driving on a dynamically changing racetrack, completing multiple laps without human input and adapting to new configurations in each round.
<div style="width: 100%; display: flex; justify-content: center; margin-top: 40px;">
  <table style="background-color: #f0f0f0; text-align: center; border-collapse: collapse; font-family: Arial, sans-serif; transform: scale(1.2);">
    <tr>
      <td style="padding: 20px;">
        <img src="v-photos/front.jpg" width="250"><br><strong>Front</strong>
      </td>
      <td style="padding: 20px;">
        <img src="v-photos/back.jpg" width="250"><br><strong>Back</strong>
      </td>
    </tr>
    <tr>
      <td style="padding: 20px;">
        <img src="v-photos/right.jpg" width="250"><br><strong>Right</strong>
      </td>
      <td style="padding: 20px;">
        <img src="v-photos/left.jpg" width="250"><br><strong>Left</strong>
      </td>
    </tr>
    <tr>
      <td style="padding: 20px;">
        <img src="v-photos/top.jpg" width="250"><br><strong>Top</strong>
      </td>
      <td style="padding: 20px;">
        <img src="v-photos/bottom.jpg" width="250"><br><strong>Bottom</strong>
      </td>
    </tr>
  </table>
</div>





## Engineering Documentation Overview

This documentation outlines the key components of the engineering process involved in the development and operation of the autonomous vehicle. It provides an overview of the following subsystems:

### Mobility Control
Design and implementation of systems responsible for the vehicle's movement, including speed regulation, turning mechanisms, and path-following algorithms.

### Power and Sensory Management
Integration and management of the vehicle’s power supply, along with configuration and usage of various sensors. These sensors deliver essential environmental data used by the robot’s decision-making systems.

### Obstacle Navigation and Avoidance
Development of strategies and systems that allow the vehicle to detect, assess, and navigate around obstacles. This includes both hardware and software components required for safe and effective performance in the Obstacle Challenge.

# Mobility Control
## ⚙️ Mobility Control

### Evolution of Design

Over the course of development, we built and tested **three different chassis and drive configurations** to find the most reliable and competition-ready setup.

#### 🔧 First Version: EV3-Based Rear-Wheel Drive  
- **Motors**: Large EV3 motor for rear-wheel drive, Medium EV3 motor for steering  
- **Platform**: Open-source Linux-based EV3 firmware  
- **Pros**: Familiar platform, easy sensor integration  
- **Cons**: Long upload times, significant turning inaccuracies due to software delays and large motor inertia
<p align="center">
  <img src="other/images/1_mobility_control.jpg" alt="Mobility Control" width="400"/>
</p>





#### 🔧 Second Version: Front-Wheel Drive with DC Gearbox Motors  
- **Motors**: Two front-mounted DC gearbox motors + front servo for steering  
- **Platform**: POP-BOT XT board with direct wiring  
- **Pros**: Improved maneuverability  
- **Cons**: Required a lot of internal space for motor connections; turning errors due to all movement being concentrated in the front wheels
  <p align="center">
  <img src="other/images/2_mobility_control.jpg" alt="Mobility Control" width="400"/>
</p>

🔧 **Third Version: Rear-Wheel Drive with EV3 Medium Motor for Steering**  
**Motors**: NXT motor for rear-wheel drive, Medium EV3 motor for steering  
**Drive Configuration**: Rear-wheel drive  
**Platform**: POP-BOT XT board  


**Pros**: Compact rear-wheel drive setup, stable at higher speeds  
**Cons**: Steering lacked precision since it was controlled by power level instead of angle, which led to inaccurate turns and difficulty in fine adjustments  
 <p align="center">
  <img src="other/images/3_mobility_control.jpg" alt="Mobility Control" width="400"/>
</p>

#### ✅ Final Version: Rear-Wheel Drive with NXT Motor and Parallax Servo  
- **Motors**: NXT motor for drive, Parallax continuous rotation servo for steering  
- **Drive Configuration**: Rear-wheel drive  
- **Improvements**:  
- **Rear-wheel drive** offers better traction and improved directional stability, especially at higher speeds  
- The **Parallax servo** enables precise angular steering, making turns smoother and more accurate
   
<p align="center">
  <img src="v-photos/right.jpg" alt="Mobility Control" width="400"/>
</p>

  
---

### 🔩 Drivetrain & Motors

- **Drive Motor**: LEGO NXT motor  
- **Mounting**: Connected to the rear axle using a custom holder  
- **Motor Driver**: Integrated with POP-BOT XT board  
- **Steering Mechanism**: Parallax continuous rotation servo motor connected to the front wheels  
 
### Potential Improvements
- Upgrade NXT motor to a lighter high-efficiency DC motor to reduce weight and increase speed control  
- Implement position feedback from the servo for dynamic steering correction  
- Add soft damping or suspension to reduce shaking on uneven surfaces  

### Motor Components in Final Version

<p align="center">
  <img src="other/images/nxt_motor.webp" alt="LEGO NXT Motor" width="300"/>
</p>

#### ⚙️ LEGO NXT Motor  
- **Description**: 9 V DC motor with 48:1 internal gearbox and optical encoder (~1° resolution) 
- **Key Specs**:  
  - Built-in optical encoder provides position feedback 
  - Gear reduction gives high torque at low RPM 
- **Advantages**: precise movement control, reliable performance in robotic applications  
- **Disadvantages**: heavier than micro DC options; limited top speed  
- **Usage**: used for rear-wheel drive

---

<p align="center">
  <img src="other/images/parallax.jpg" alt="Parallax Continuous Rotation Servo" width="300"/>
</p>

#### 🌀 Parallax Continuous Rotation Servo (900‑00008)  
- **Description**: continuous-rotation servo made by Parallax (Futaba gear set), designed for PWM control of speed and direction
- **Key Specs** (900‑00008):  
  - Operating voltage: 4–6 V DC 
  - Torque: ~2.7 kg·cm (4.8 V) up to ~3.0 kg·cm (6 V) 
  - Speed: ~50–60 RPM (no load) 
  - Weight: ~42–45 g 
- **Advantages**: precise angular steering via PWM (1300–1700 µs pulse widths) 
- **Considerations**: requires calibration (center potentiometer adjustment) 
- **Usage**: used for steering mechanism in final version


---

### 🏗️ Control Board: POP‑BOT XT

<p align="center">
  <img src="other/images/pop_bot.jpg" alt="POP‑BOT XT Board" width="300"/>
</p>

#### 🧭 POP‑BOT XT (Arduino Leonardo–compatible)

- **Microcontroller**: ATmega32U4, 16 MHz, preloaded with Arduino Leonardo bootloader  
- **Memory**: 32 KB Flash, 2.5 KB SRAM, 1 KB EEPROM  
- **I/O**: 12 analog inputs, digital I/O pins, I²C, UART, and SPI communication  
- **Motor Drivers**: Two built-in DC motor drivers, three JST headers for servos (4.8–7.2 V supported)  
- **Power Supply**: Powered by 4 × AA batteries (4.8–6 V), with onboard step-up/step-down voltage regulator (+5 V)  
- **Other Features**: Integrated 1.8" color graphic LCD (128×160, 262K colors), USB programmable without external hardware  
- **Advantages**: All-in-one robotics platform — microcontroller, motor drivers, power management, and display in a single board  
- **Usage in Our Robot**: Acts as the central control unit; both the NXT motor (drive) and the Parallax continuous rotation servo (steering) are connected to this board  


## 🔌 Power and Sensory Management

Integration and management of the vehicle’s power supply, along with configuration and usage of various sensors. These sensors deliver essential environmental data used by the robot’s decision-making systems.

---

### 📷 HuskyLens AI Camera

<p align="center">
  <img src="other/images/huskylens.jpg" alt="HuskyLens AI Camera" width="300"/>
</p>

- **Description**: Smart vision sensor with built-in machine learning algorithms  
- **Key Features**:
  - Recognizes lines, objects, colors, faces, QR codes, and tags
  - Built-in UART/I2C communication interface  
- **Operating Voltage**: 3.3 V – 5 V  
- **Usage**:
  - **Stage 1 (Line Following)**: The robot uses HuskyLens to detect and follow lines on the track  
  - **Stage 2 (Obstacle Challenge)**: Recognizes the color of blocks (e.g., red/green) to make navigation decisions accordingly  



---

### 📐 MPU6050 Gyroscope + Accelerometer

<p align="center">
  <img src="other/images/mpu.jpg" alt="MPU6050 Sensor" width="300"/>
</p>

- **Description**: 6-axis motion tracking device (3-axis gyroscope + 3-axis accelerometer)  
- **Key Features**:
  - I2C communication  
  - Integrated Digital Motion Processor (DMP)  
- **Operating Voltage**: 3 V – 5 V  
- **Usage**:
  - The robot uses the **gyroscope** to measure angular rotation, enabling more precise turns and directional stability  
  - Helps to smooth out turning behavior, especially during sharp cornering
 ```cpp
#include <Wire.h>
#include <MPU6050_light.h>
#include <popxt.h>

MPU6050 mpu(Wire);

#define DRIVE_MOTOR 1
#define SERVO_PIN 1
#define BASE_SERVO 88
#define DEAD_ZONE 0.01

float Kp = 4.5;
float Kd = 1.8;

float yaw = 0.0;
float targetYaw = 0.0;
float prevError = 0.0;
unsigned long lastTime = 0;

int currentSteer = BASE_SERVO;
bool started = false;

void setup() {
  Wire.begin();
  mpu.begin();
  mpu.calcGyroOffsets();

  sw_ok_press();         // Ждём кнопку
  mpu.calcGyroOffsets(); // Повторная калибровка

  servo(SERVO_PIN, BASE_SERVO);
  lastTime = millis();
}

void loop() {
  if (!started) {
    motor(DRIVE_MOTOR, 70);
    started = true;
  }

  mpu.update();

  float dt = (millis() - lastTime) / 1000.0;
  lastTime = millis();

  float gz = mpu.getGyroZ();
  if (abs(gz) < DEAD_ZONE) gz = 0;
  yaw += gz * dt;

  float error = targetYaw - yaw;
  float derivative = (error - prevError) / dt;
  prevError = error;

  float output = constrain(Kp * error + Kd * derivative, -25, 25);
  int targetSteer = constrain(BASE_SERVO + output, 40, 130);

  if (targetSteer > currentSteer + 3)      currentSteer += 3;
  else if (targetSteer < currentSteer - 3) currentSteer -= 3;
  else                                     currentSteer = targetSteer;

  servo(SERVO_PIN, currentSteer);
  delay(50);
}
```






