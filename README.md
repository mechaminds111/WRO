# MechaMinds-WRO 2026 Future Engineers
# WRO Future Engineers - Engineering Documentation
<p align="center">
<img src="TEAM-PICTURES/school logo.png" width="200" > 
<br>
<em> Our school logo.</em>
</p>

## Team Members
- **Barbara Lukić**
- **Nadia Kravčuk**
- **Ivano Koren**

<p align="center">
  <img src="TEAM-PICTURES/team photo/team photo.jpeg" width="500" >
</p>
<br>
<p align="center">
  <em>Team picture.</em>
</p>
<p align="center">
  <img src="TEAM-PICTURES/funny photo/funny photo2.jpeg" width="500" > 
</p>
<br>
<p align="center">
  <em>Funny team picture.</em>
</p>

[Watch the introduction video](TEAM-PICTURES/video/video_mechaminds.mp4)

## Table of Contents

- [1. Project Overview](#1-project-overview)
- [2. Team](#2-team)
- [3. Vehicle Overview](#3-vehicle-overview)

- [4. Development History](#4-development-history)
  - [4.1 Version 1](#41-version-1)
  - [4.2 Version 2](#42-version-2)
  - [4.3 Version 3](#43-version-3)
  - [4.4 Version 4](#44-version-4)

- [5. Current Robot](#5-current-robot)
 
- [6. Mobility & Mechanical Design](#6-mobility--mechanical-design)
  - [6.1 Chassis](#61-chassis)
  - [6.2 Steering & Driving System](#62-steering--driving-system)
  - [6.3 Dimensions and Weight](#63-dimensions-and-weight)
  
- [7. Power & Sensor Architecture](#7-power--sensor-architecture)
  - [7.1 Motors](#71-motors)
  - [7.2 Sensors](#72-sensors)
  - [7.3 Camera](#73-camera)
  - [7.4 Wiring Diagram](#74-wiring-diagram)
  - [7.5 Power](#75-power)
  - [7.6 ON/OFF Button](#76-onoff-button)
  
- [8. Software Architecture](#8-software-architecture)
  - [8.1 Overview](#81-overview)
  - [8.2 Code](#82-code)
  - [8.3 Open Challenge Strategy](#83-open-challenge-strategy)
  - [8.4 Obstacle Challenge Strategy](#84-obstacle-challenge-strategy)
    
- [9. Engineering Decisions](#9-engineering-decisions)
  - [9.1 Major Problems and Solutions](#91-major-problems-and-solutions)

- [10. Testing & Results](#10-testing--results)

- [11. Components / Bill of Materials](#11-components--bill-of-materials)

- [12. Build & Reproduction Guide](#12-build--reproduction-guide)
  - [12.1 Parts](#121-parts)
  - [12.2 Assembly](#122-assembly)

- [13. Repository Structure](#13-repository-structure)
- [14. Engineering Journal](#14-engineering-journal)


## 1. Project Overview
Our project is an autonomous vehicle that can navigate the competition field, detect and avoid obstacles, follow the track and make real time decisions without human intervention.

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

## 2. Team
We are the Croatian robotics team **MechaMinds** and our names are **Barbara Lukić**, **Ivano Koren** and **Nadia Kravčuk**. We come from Tin Ujević High School in Kutina. Our mentor's name is Damir Petravić. Together we worked on the design of the robot, programming and testing our robot.



<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

## 3. Vehicle Overview
| Specification | Value |
|---|---|
| Length | 18 cm |
| Width | 17.5 cm |
| Height | 15.5 cm |
| Weight | 0.876 kg |
| Drive type | Rear-wheel drive |
| Steering type | Ackermann steering |     ---Servo-controlled front steering???
| Main controller | Raspberry Pi 5 Model (B Rev1.1) |
| Programming language | C++ |
| Main sensors | MRMS LIDAR 2 m (VL53L0CX), CAN Bus |
| Camera | Raspberry Pi Camera Module 3 |
| Power source | Turnigy 5S LiPo, 18.5 V, 5000 mAh |

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

## 4. Development history 
Our robot went through several major design changes during the development process. 
### 4.1. Version 1 
**About the robot** 
  - Our first robot was a custom-built vehicle made using 3D-printed and hand-built parts. It had several distance sensors that helped us test the robot.

**Main problem** 
  - The robot was not reliable enough to complete three laps so we decided to change the robot for better performance.

| Front | Rear |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_1/front.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_1/rear.jpeg" width="200"> |

| Left | Right |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_1/left.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_1/right.jpeg" width="200"> |

| Top | Bottom |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_1/top.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_1/bottom.jpeg" width="200"> |

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 4.2. Version 2
**About the robot**
- This robot was an upgraded version of the first one, it had a camera and several distance sensors.
  
**Main problem**
- All year we have been working on this robot, about one month before the competition we started having problems connecting the robot to Wi-Fi, it started crashing and we tried to find a solution before the competition but we did not succeed.

| Front | Rear |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_2/final/front.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_2/final/rear.jpeg" width="200"> |

| Left | Right |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_2/final/left.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_2/final/right.jpeg" width="200"> |

| Top | Bottom |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_2/final/top.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_2/final/bottom.jpeg" width="200"> |

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 4.3. Version 3
**About the robot**
- This robot was built out of LEGO, it represents a model of a Ford car.

**Main problem**
- The robot had a problem turning its wheels because of the design, so it could not complete even one lap, because of this we had to completely redesign it.

| Front | Rear |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_3/front.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_3/rear.jpeg" width="200"> |

| Left | Right |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_3/left.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_3/right.jpeg" width="200"> |

| Top | Bottom |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_3/ford1.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_3/bottom.jpeg" width="200"> |

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 4.4. Version 4
**About the robot**
- This was our final robot that we went to the competition with, it was also built out of lego bricks, it worked with the help of distance sensors.
  
**Main problem**
- Although we went to the competition with this robot it still had a few flaws. The LEGO sensors that we used to measure distance were not able to detect walls from sufficient distance so the robot couldn't complete even one lap.

| Front | Rear |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_4/front.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_4/rear.jpeg" width="200"> |

| Left | Right |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_4/left.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_4/right.jpeg" width="200"> |

| Top | Bottom |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_4/top.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_4/bottom.jpeg" width="200"> |

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

## 5. Current Robot
The robot we will use for the competition in Zagreb is [4.2 Version 2](#42-version-2). Although this version originally had problems with an unstable Wi-Fi connection, the connection issue was later solved [9.1 Major Problems and Solutions](#91-major-problems-and-solutions) This robot can now avoid obstacles and track walls using two distance sensors that are placed on each side of the robot. 

The robot uses a four-wheel chassis with rear-wheel drive and servo-controlled front steering.

For navigation, the robot uses LiDAR distance sensors positioned near the front of the chassis. They measure the distance from nearby walls and allow the robot to follow the track, maintain a safe distance from the walls and avoid collisions.

A Raspberry Pi Camera Module 3 is mounted at the front of the robot. The camera is used to detect colored obstacles and other important features of the competition field. By combining camera-based vision with LiDAR distance measurements, the robot can make navigation decisions in real time.


| Front | Rear |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_2/final/front.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_2/final/rear.jpeg" width="200"> |

| Left | Right |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_2/final/left.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_2/final/right.jpeg" width="200"> |

| Top | Bottom |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_2/final/top.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_2/final/bottom.jpeg" width="200"> |

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

| Front | Rear |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_2/final/front.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_2/final/rear.jpeg" width="200"> |

| Left | Right |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_2/final/left.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_2/final/right.jpeg" width="200"> |

| Top | Bottom |
|---|---|
| <img src="DEVELOPMENT-HISTORY/version_2/final/top.jpeg" width="200"> | <img src="DEVELOPMENT-HISTORY/version_2/final/bottom.jpeg" width="200"> |

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

## 6. Mobility & Mechanical Design
### 6.1 Chassis

#### Chassis Overview
Our current vehicle uses a four-wheel chassis, the chassis provides the mechanical base for the drive system, steering mechanism, sensors and processing hardware. The design was developed with stability, compact dimensions and reliable steering in mind.

#### Component Placement
The electronic components are arranged on several levels above the main chassis plate. The battery is positioned low inside the chassis to keep the center of gravity as low as possible, while the processing and control electronics are placed above it. The camera is placed at the front of the robot on a dedicated 3D-printed support so it could have good visibility of the field. The distance sensors are positioned near the front of the vehicle so that they can detect the surrounding walls during navigation.

- Main controller: on top of the robot
- Battery: inside the chassis
- Drive motor: in the back, underneath the chassis
- Steering servo: in the front, underneath the chasis
- Sensors: in the front, inside the chassis
- Camera: the front of the robot

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 6.2 Steering & Driving System

The vehicle uses a servo-controlled front steering mechanism. A steering servo placed at the front of the chassis moves a mechanical linkage that connects the two front wheels. Instead of controlling the left and right wheels with separate motors, both front wheels are mechanically linked and change direction together. This provides car-like steering while the rear wheels make the robot move forward. The steering components are mounted directly to the 3D-printed chassis, which allowed us to adjust the geometry and mounting positions during development. The two rear wheels are connected by a metal rod and do not turn left or right, so they keep the robot moving straight. The motor is connected to the battery and provides the power needed to move the robot. This simple system allows the robot to move forward in a straight line.

<p align="center">
  <img src="DEVELOPMENT-HISTORY/version_2/final/bottom.jpeg" width="500">
</p>

<p align="center">
  <em>Front steering mechanism and mechanical linkage.</em>
</p>

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 6.3 Dimensions and Weight

| Measurement | Value |
|---|---|
| Length | 180 mm |
| Width | 175 mm |
| Height | 155 mm |
| Weight | 0.876 kg |
| Wheelbase | 100 mm |
| Front track width | 175 mm |
| Rear track width | 170 mm |
| Front wheel diameter | 60 mm |
| Rear wheel diameter | 65 mm |

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>


## 7. Power & Sensor Architecture
### 7.1 Motors

The robot is powered by a single ML-R BDC N20 micro brushed DC motor. It operates at 12V DC with a low-power profile, ensuring high efficiency for battery-powered operation. The integrated 1:100 gear ratio provides high output torque within a compact 12 mm form factor. This motor serves as the primary drive source for the robot's propulsion mechanism.

<p align="left">
  <img src="POWER-AND-SENSORS/motor/motor.png" alt="ML-R BDC N20 Motor" width="200" />
</p>

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 7.2 Sensors

The robot uses MRMS VL53L0CX LiDAR sensors to measure the distance to nearby obstacles. The sensors have a specified range of up to 2 m and communicate with the rest of the system via CAN Bus. Each robot is equipped with three LiDAR sensors, allowing distance measurements in multiple directions. The collected data can be used for obstacle detection, navigation, and collision avoidance. Both LiDARSs are placed at the front of the robot, each on one side, between two chassis and at the angle of 45° so they wouldn't be too high nor too low to not be able to detect walls from the side and from the front.

<img src="POWER-AND-SENSORS/sensors/sensor.jpg" width="200"> 

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

###  7.3 Camera

The robot uses a Raspberry Pi Camera Module 3 for visual perception of its surroundings. The camera is connected to the Raspberry Pi 5 and can be used to capture images and video for further processing. It can support tasks such as line detection, object recognition, marker detection, and navigation. The camera complements the LiDAR sensors by providing visual information that distance sensors alone cannot provide.

<img src="POWER-AND-SENSORS/camera/camera.png" width="200"> 

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 7.4 Wiring Diagram

<p>
  This diagram illustrates the robot's physical structure and highlights the core components, 
  demonstrating how the essential systems and connections are wired together.
</p>

<img src="BUILD-GUIDE/wiring/zicerobotaa.png" width="500" >


<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 7.5 Power
#### Battery

Our robot is powered by a Turnigy 5.0 High Discharge LiPo battery. 
The battery was selected to provide sufficient voltage, capacity and 
current for the robot's motors and electronic components.

#### Specifications

| Parameter | Value |
|---|---|
| Battery type | LiPo (Lithium Polymer) |
| Configuration | 5S |
| Nominal voltage | 18.5 V |
| Capacity | 5000 mAh (5.0 Ah) |
| Discharge rating | 20–30C |
| Discharge current | 150 A |
| Manufacturer | Turnigy |
| Model | Turnigy 5.0 |
| Main connector | High-current connector |
| Balance connector | 5S balance connector |

We chose this battery because our robot requires a power source capable of 
supplying high current to the motors while maintaining a stable voltage.

<img src="BATTERY-AND-CHARGER/battery/battery1.jpeg" width="200"> <img src="BATTERY-AND-CHARGER/battery/battery3.jpeg" width="200"> <img src="BATTERY-AND-CHARGER/battery/battery4.jpeg" width="200">
#### Charger

The robot uses a B6 LiPro 80W Balance Charger to charge the LiPo battery. It supports 1–6 cell LiPo batteries and includes a balance function to keep the voltage of the individual cells equal during charging.

<img src="BATTERY-AND-CHARGER/charger/charger1.jpeg" width="200">

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 7.6 ON/OFF Button
The buttons used to turn the robot on, start it, and stop it was placed on top to make it easily accessible.

<p>This section explains the code structure and button controls for operating the robot.</p>

<h4 align="center">Code for Buttons</h4>

<p align="center">
  <img src="POWER-AND-SENSORS/buttons/button1.jpeg" alt="Code for Buttons" width="80%" />
</p>

<p align="center">
  <img src="POWER-AND-SENSORS/buttons/button2.jpeg" alt="Physical Buttons on Robot" width="50%" />
</p>

<h4>Button Functions</h4>

<p><strong>1. Button 1 (Pin 1) &ndash; Start / Stop:</strong> Launches <code>system_start()</code> or halts the robot with <code>full_stop()</code>.</p>

<p><strong>2. Button 2 (Pin 2) &ndash; Open Challenge:</strong> Selects and starts <code>open_challenge()</code>.</p>

<p><strong>3. Button 3 (Pin 3) &ndash; Obstacle Challenge:</strong> Selects and starts <code>prepreke_challenge()</code>.</p>

<p><strong>4. Button 4 (Pin 4) &ndash; Servo +2°:</strong> Manually increases the servo angle by 2 degrees.</p>

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

## 8. Software Architecture
### 8.1 Overview
The robot software is written in C++. The code is developed and maintained within Visual Studio Code, utilizing dedicated extensions for embedded C++ compilation and debugging. The software architecture handles direct motor control, power management, and timing routines required for accurate motor drive operations.

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 8.2 Code
#### Code used for distance sensors
<img src="CODE/sensors code/sensors code.png" width="300">

#### Code used for camera
<img src="CODE/camera code/camera code.png" width="300">

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

[Code](4_vožnja_u_krug_bez_prepreka.txt)

### 8.3 Open Challenge Strategy

The Open Challenge requires the robot to complete three laps of the track autonomously without colliding with obstacles. During the run, the robot uses its LiDAR sensors and camera to detect the track boundaries and nearby objects. Based on the sensor data, the control system continuously adjusts the robot’s direction and movement. The main goal is to achieve reliable navigation, smooth cornering, and consistent obstacle avoidance throughout all three laps.

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 8.4 Obstacle Challenge Strategy

<p>The robot uses a <b>Raspberry Pi Camera Module 3</b> connected to a <b>Raspberry Pi 5</b>, enabling image and video capture for line detection, object recognition, and color marker detection. While LiDAR sensors handle wall-following and distance measurement, the camera provides visual perception that distance sensors alone cannot supply. By combining wall-following via LiDAR with visual processing from the camera, the robot actively detects red and green obstacles. The system processes camera data in real time to steer correctly around color-coded markers while maintaining high-speed autonomous navigation. This dual-sensing setup ensures precise positioning and seamless obstacle avoidance required to complete all three laps fully autonomously.</p>

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>


## 9. Engineering Decisions
### 9.1 Major Problems and Solutions
#### Connection Failure 

- During development, we experienced repeated problems with the Wi-Fi connection between the robot and the development computer. The connection was unstable and we could not work with the robot properly. To improve reliability, we tested a wired Ethernet connection using an RJ45 network cable. During our tests, this connection proved to be significantly more stable and reliable than Wi-Fi, so we decided to use the wired connection during development.

<img src="connection-solution/connection1.jpeg" width="200"> <img src="connection-solution/connection2.jpeg" width="200">
<img src="connection-solution/connection3.jpeg" width="200"> <img src="connection-solution/connection4.jpeg" width="200">

#### Sensor Placement

- During testing, the distance sensors were positioned on the upper part of the robot. In this position, the sensors were too high and could not reliably detect the wall directly in front of the vehicle. After identifying this issue, we redesigned the sensor position and moved the distance sensors lower on the chassis. This improved their field of view and allowed them to detect the wall more reliably. This change showed us how sensor placement can affect the performance of the navigation system.

<img src="DEVELOPMENT-HISTORY/version_2/build/build-03.jpeg" width="250">  <img src="DEVELOPMENT-HISTORY/version_2/build/build-04.jpeg" width="250">

**Test result:**
| Sensor position | Successful wall detections |
|---|---:|
| Original higher position | 3/10 |
| Lowered position | 8/10 |


<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

## 10. Testing & Results

<p>You can see all the tests and results on our YouTube channel:</p>

<a href="https://www.youtube.com/@mechaminds111" target="_blank">
  MechaMinds Youtube Channel
</a>

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>
  
## 11. Components / Bill of Materials

[View the Bill of Materials PDF](docs/bill-of-materials/bill-of-materials.pdf)

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

## 12. Build & Reproduction Guide
Our robot is completely made out of 3D-printed parts.

### 12.1 Parts

All custom mechanical components and structural parts of the robot were designed using Autodesk Fusion and manufactured via 3D printing.
* **3D Modeling & CAD:** Autodesk Fusion
* **Manufacturing:** 3D Printed
* **3D Models & STL Files:**
  * Wheel STL file: [BUILD-GUIDE/wheels/wheel11.stl](BUILD-GUIDE/wheels/wheel1.stl)
  * Chassis STL file: [BUILD-GUIDE/chassis/mrm3d-chmod110-chassis.stl](BUILD-GUIDE/chassis/mrm3d-chmod110-chassis.stl)
  * Raspberry pi3 STL file: [BUILD-GUIDE/Raspberry-pi3/RaspberryPI3.stl](BUILD-GUIDE/Raspberry-pi3/RaspberryPi3.stl)
  * RotaryJointRoundTop STL file: [BUILD-GUIDE/rotaryjoint/RotaryJointRoundTop.stl](BUILD-GUIDE/rotaryjoint/RotaryJointRoundTop.stl)


-**wheels**:

<img src="BUILD-GUIDE/wheels-making/wheels2.jpeg" width="200">  <img src="BUILD-GUIDE/wheels-making/wheels3.jpeg" width="200"> <img src="BUILD-GUIDE/wheels-making/wheels-fusion.png" width="400" height='400'>

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

### 12.2 Assembly

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>


## 13. Repository Structure
This repository is organized into separate folders for documentation, hardware, software, media and testing. It makes it easier to locate files needed to understand and reproduce the robot.

```text
WRO/
├── BATTERY-AND-CHARGER/
│   ├── battery/
│   │   ├── battery1.jpeg
│   │   ├── battery2.jpeg
│   │   ├── battery3.jpeg
│   │   └── battery4.jpeg
│   └── charger/
│       └── charger1.jpeg
│
├── BUILD-GUIDE/
│   ├── Raspberry pi3/
│   │   └── RaspberryPi3.stl
│   ├── chassis/
│   │   ├── chassis.stl
│   │   └── mrm3d-chmod110 - chassis.stl
│   ├── panel/
│   │   └── mrm-pl90x35.stl
│   ├── rotaryjoint/
│   │   └── RotaryJointRoundTop.stl
│   ├── wheels-making/
│   │   ├── wheels-fusion.png
│   │   ├── wheels1.jpeg
│   │   ├── wheels2.jpeg
│   │   └── wheels3.jpeg
│   ├── wheels/
│   │   ├── wheel1.stl
│   │   └── wheel5-70.step
│   ├── wiring/
│   │   └── donjaploca.PNG.jpg
│   └── engineering-decisions.md.txt
│
├── CODE/
│   ├── camera code/
│   │   └── camera code.png
│   └── sensors code/
│       └── sensors code.png
│
├── DEVELOPMENT-HISTORY/
│   ├── version_1/
│   │   ├── bottom.jpeg
│   │   ├── front.jpeg
│   │   ├── left.jpeg
│   │   ├── rear.jpeg
│   │   ├── right.jpeg
│   │   └── top.jpeg
│   │
│   ├── version_2/
│   │   ├── build/
│   │   │   ├── build-01.jpeg
│   │   │   ├── build-02.jpeg
│   │   │   ├── build-03.jpeg
│   │   │   ├── build-04.jpeg
│   │   │   ├── build-05.jpeg
│   │   │   └── build-06.jpeg
│   │   └── final/
│   │       ├── bottom.jpeg
│   │       ├── front.jpeg
│   │       ├── left.jpeg
│   │       ├── rear.jpeg
│   │       ├── right.jpeg
│   │       └── top.jpeg
│   │
│   ├── version_3/
│   │   ├── bottom.jpeg
│   │   ├── ford1.jpeg
│   │   ├── ford2.jpeg
│   │   ├── front.jpeg
│   │   ├── left.jpeg
│   │   ├── rear.jpeg
│   │   └── right.jpeg
│   │
│   └── version_4/
│       ├── bottom.jpeg
│       ├── front.jpeg
│       ├── left.jpeg
│       ├── rear.jpeg
│       ├── right.jpeg
│       └── top.jpeg
│
├── POWER-AND-SENSORS/
│   ├── buttons/
│   │   ├── button1.jpeg
│   │   └── button2.jpeg
│   ├── camera/
│   │   └── camera.png
│   ├── motor/
│   │   └── motor.png
│   └── sensors/
│       └── sensor.jpg
│
├── TEAM-PICTURES/
│   ├── funny photo/
│   │   ├── funny photo1.jpeg
│   │   ├── funny photo2.jpeg
│   │   ├── funny photo3.jpeg
│   │   └── funny photo4.jpeg
│   ├── other photos/
│   │   ├── lego - mechaminds.jpg
│   │   ├── team2.jpeg
│   │   ├── team3.JPG
│   │   └── team4.JPG
│   ├── team photo/
│   │   └── team photo.jpeg
│   ├── video/
│   │   ├── video_mechaminds.mp4
│   │   └── video_mechaminds.zip
│   └── school logo.png
│
├── archive/
│   └── first-readme.md.txt
│
├── bill-of-materials/
│   └── bill-of-materials.pdf
│
├── connection-solution/
│   ├── connection1.jpeg
│   ├── connection2.jpeg
│   ├── connection3.jpeg
│   └── connection4.jpeg
│
└── README.md
```

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>

## 14. Engineering Journal
With the start of last school year (8.9.2025) we started working with robot [4.1 Version 1](#41-version-1), but the robot was not reliable enough to complete three laps so we decided to change the robot for better performance. 
On 31.3.2026. we started working with [4.2 Version 2](#42-version-2). The robot was working very well but then about one month before the competition we started having problems connecting the robot to Wi-Fi, it started crashing and we tried to find a solution before the competition but we did not succeed. 
So, on 22.5.2026. we built [4.3 Version 3](#43-version-3). The robot had a problem turning its wheels because of the design, so it could not complete even one lap, because of this we had to completely redesign it.
On 6.6.2026. we built [4.4 Version 4](#44-version-4). Although we went to the competition with this robot it still had a few flaws. The LEGO sensors that we used to measure distance were not able to detect walls from sufficient distance so the robot couldn't complete even one lap.
Over the summer we decided that we should fix robot [4.2 Version 2](#42-version-2) so the whole summer we spent working on that robot and fixing it. On 27.8.2026. we connected robot to Wi-Fi and then we got into programming. 

<p align="right">
  <a href="#table-of-contents">⬆ Back to Table of Contents</a>
</p>
