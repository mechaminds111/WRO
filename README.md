# WRO 2026 Future Engineers

## Team
MechaMinds, Srednja škola Tina Ujevića, Kutina, Croatia
<br><br><br>
At first we were classmates who didnt't talk much, but when we decided to come together as a team for a robotics competiton, everything changed. 
Now we are friends who love spending time together and most importantly, we are a **team** that is ready to overcome every challenge.
<br>
<br>
<img src="team1.jpeg" width="350" hight='300'> <img src="team2.jpeg" width="250" > <br>
<img src="team3.JPG" width="350" height='300'> <img src="team4.JPG" width="350" height='300'> 

## Members
While every member of MechaMinds was fully involved in every stage of development—from brainstorming and building to coding and testing, 
we each took the lead in specific areas to ensure maximum efficiency:

* **Ivano Koren** — *Lead Mechanical Engineer*. Ivano spearheaded the physical construction of the vehicle, optimizing the chassis layout, steering geometry, and weight distribution, while the team assisted in testing mechanical durability.
* **Barbara Lukić** — *Lead Software Engineer*. Barbara took the driver's seat for the core programming, developing program in Pybricks, with input from the whole team during track-side debugging.
* **Nadia Kravčuk** — *Systems Engineer & Documentation Lead*. Nadia directed our technical reporting, ensuring our engineering journal, while coordinating with the team to capture media and data.

## Competition
We are competing in the **World Robot Olympiad (WRO) 2026 – Future Engineers** category. The competition challenges us to design a scale-model autonomous vehicle capable of executing real-time decision-making under changing track conditions.

The 2026 tournament is focused on the vehicle completing two distinct challenges within a strict **3-minute time limit** per round:

### 1. Open Challenge
* **Objective:** The vehicle must successfully complete three (3) full consecutive laps on the track.
  <br>
  **OUR SOLUTION:**

### 2. Obstacle Challenge
* **Objective:** The vehicle must complete three (3) laps while navigating throught a specific layout of randomly placed green and red obstacles and in the end it needs to do a parallel parking.
* **Traffic obstacle logic:**
  * **Red Pillar:** When the vehicle comes across a red obstacle it needs to keep to the **right** side of the lane.
  * **Green Pillar:** When the vehicle comes across a green obstacle it needs to keep to the **left** side of the lane.
* **The Parking Mission:** Upon completing the third lap, the vehicle must autonomously locate the designated parking zone (marked by magenta barriers) and do a precise, parallel parking maneuver without making contact with the walls or obstacles.
<br>
OUR SOLUTION:...

## Vehicle

Our vehicle is a fully autonomous self-driving car designed for the WRO 2026 Future Engineers competition. The robot is capable of following the track, avoiding obstacles and recognizing traffic signs without human intervention.

## Images
<img src="back1.jpeg" width="250"> <img src="front1.jpeg" width="250"> <img src="left side1.jpeg" width="250"> <img src="right side1.jpeg" width="250">
<img src="under1.jpeg" width="250"> <img src="up1.jpeg" width="250">
<br>
<img src="izrada1.jpeg" width="250"> <img src="izrada2.jpeg" width="250"> <img src="izrada3.jpeg" width="250"> 
<img src="izrada4.jpeg" width="250"> <img src="izrada5.jpeg" width="250"> <img src="izrada6.jpeg" width="250"> 
<br>
<img src="back2.jpeg" width="250"> <img src="front2.jpeg" width="250"> <img src="down2.jpeg" width="250"> 
<img src="up2.jpeg" width="250"> <img src="left side2.jpeg" width="250"> <img src="right side2.jpeg" width="250"> 
<br>
<img src="ford1.jpeg" width="250"> <img src="ford2.jpeg" width="250"> <img src="ford front.jpeg" width="250"> 
<img src="ford down.jpeg" width="250"> <img src="ford right.jpeg" width="250"> <img src="ford left.jpeg" width="250"> <img src="ford back.jpeg" width="250"> 
<br>
<img src="back last.jpeg" width="250"> <img src="front last.jpeg" width="250"> <img src="down last.jpeg" width="250"> 
<img src="up last.jpeg" width="250"> <img src="left last.jpeg" width="250"> <img src="right last.jpeg" width="250">




## Vehicle & Mechanical Design

Our vehicle is an autonomous model car according to the WRO 2026 Future Engineers rules. The mechanical design uses a rear-wheel-drive system where a single large LEGO motor provides power to the rear axle, while a single smaller LEGO motor acts as the steering motor to control the front wheels. This balances the vehicle's driving dynamics and prevents the tires from slipping sideways during tight cornering. Both drive wheels are physically locked to the same axle, completely eliminating any form of prohibited electronic or independent dual-motor differential setups.

### Technical Specifications
* **Dimensions:** 220mm (Length) x 170 mm (Width) x 150 mm (Height) — *Within the maximum allowed 300 x 200 x 300 mm boundary.*
* **Total Weight:** 0.532 kg — *Under the maximum limit of 1.5 kilograms.*

### Kinematics & Drivetrain Architecture
* **Steering Actuation:** We used a single LEGO steering motor configured with a physical geometry (Ackermann steering concept) to manage turning angles. This provides smooth traction and prevents the tires from slipping sideways during sharp turns.
* **Propulsion System:** Driven by a single large LEGO motor connected to the rear axle with a 1:1 gear ratio. Both rear wheels are locked on the same axle, which perfectly follows the rules by eliminating any dual-motor or differential setups.
* **Wheel Restrictions:** The vehicle rides exclusively on high-grip rubber tires.


## Hardware
- Controller: LEGO SPIKE Prime Hub
- Distance Sensor: LEGO Distance Sensor
- Color Sensor: LEGO Color Sensor
- Driving Motor: LEGO Motor
- Steering Motor: LEGO Motor

## Software - Power & Sensor Architecture

### 1. Wiring Diagram & Port Assignment
To ensure a stable and reproducible control loop, all electronic components are directly routed to the LEGO SPIKE Prime Hub. The specific physical port arrangement is mapped as follows:

| Component | Device Type | Port Assignment | Function |
| :--- | :--- | :--- | :--- |
| **Driving Motor** | LEGO Large Angular Motor | **Port A** | Rear-axle propulsion and velocity control |
| **Steering Motor** | LEGO Medium Angular Motor | **Port C** | Front-wheel Ackermann steering actuation |
| **Distance Sensor** | LEGO Distance Sensor | **Port E, Port D, Port F** | Front obstacle detection and distance tracking |

### 2. Sensor Selection & Placement Justification
The positioning of our sensors was mathematically and physically optimized based on the official field geometry:
* **Distance Sensor:** Mounted on the absolute leading edge of the front bumper at a height of 50 mm from the surface. This elevation ensures it perfectly captures the 100-150 mm high obstacle pillars while completely ignoring the low field boundary walls, eliminating false-positive braking triggers.

### 3. Obstacle & Parking Logic
* **Red and Green Obstacles:** When an obstacle is detected within 10 cm, the color sensor evaluates its RGB signature. If the red value is dominant, the steering motor sets an immediate steering angle adjustment keeping to the right side of the lane. If green is dominant, it applies an adjustment, keeping to the left side until the distance sensor clears the object.
* **The Parking Mission:** The software maintains an internal lap counter and upon entering the 3rd lap, the color sensor begins scanning for the magenta parking zone barrier. Once detected, the robot halts, switches the driving motor to reverse and executes a pre-programmed turn sequence to achieve a precise parallel park.

### 4. System State Machine
Our Pybricks Python program is structured around making a real-time decision. The software continuously cycles through five distinct operational states:

* **STATE 1: INIT** -> Runs the sensor calibration and resets the steering motor to the center position.
* **STATE 2: LANE_FOLLOWING** -> Executes the main line-following algorithm using the color sensor.
* **STATE 3: OBSTACLE_AVOIDANCE** -> Triggered when the distance sensor detects an object closer than 10 cm. It checks the pillar's color and calculates the bypass steering angle.
* **STATE 4: PARKING_SEQUENCE** -> Triggered after completing the 3rd lap when the magenta lines are detected.
* **STATE 5: STOP** -> Fully cuts power to all motors and completes the run.


## Repository Structure

/docs - documentation

/code - source code

/images - robot images

/videos - challenge videos




## Development
**This repository is used to track the development of our autonomous vehicle for WRO 2026.**

We started working on our vehicle for WRO 2026 in late September. From then until June we have changed four different robots. 
The **first robot** we used was 3D printed and built by hand, using several distance sensors. The following pictures show the robot from all sides:
<br><br>
<img src="back1.jpeg" width="250"> <img src="front1.jpeg" width="250"> <img src="left side1.jpeg" width="250"> <img src="right side1.jpeg" width="250">
<img src="under1.jpeg" width="250"> <img src="up1.jpeg" width="250">
<br> 
<br>
The **second robot** was an upgraded version on the first one. It had a camera and several distance sensors all around it. Before we started programming we had to make new wheels and change a few parts. Next few pictures show us making new parts:
<br><br>
<img src="izrada1.jpeg" width="250"> <img src="izrada2.jpeg" width="250"> <img src="izrada3.jpeg" width="250"> 
<img src="izrada4.jpeg" width="250"> <img src="izrada5.jpeg" width="250"> <img src="izrada6.jpeg" width="250"> 
<br>
<br>
The following pictures are pictures of robot when it was finished.
<br><br>
<img src="back2.jpeg" width="250"> <img src="front2.jpeg" width="250"> <img src="down2.jpeg" width="250"> 
<img src="up2.jpeg" width="250"> <img src="left side2.jpeg" width="250"> <img src="right side2.jpeg" width="250"> 
<br> 
<br> 
The **third robot** was LEGO robot. It was made because we had big problems with connecting second robot to our laptop. It was inspired by classic Ford Model T.
The following pictures show the robot from all sides:
<br><br>
<img src="ford1.jpeg" width="250"> <img src="ford2.jpeg" width="250"> <img src="ford front.jpeg" width="250"> 
<img src="ford down.jpeg" width="250"> <img src="ford right.jpeg" width="250"> <img src="ford left.jpeg" width="250"> <img src="ford back.jpeg" width="250"> 
<br>
After some time working with LEGO robot we realized that, because of how the weight of the robot was distributed, we couldn't keep working with it and so we made a new, **fourth**, LEGO robot which is our current one and the one we will be competing with. The following pictures are pictures of our current robot:
<br>
<img src="back last.jpeg" width="250"> <img src="front last.jpeg" width="250"> <img src="down last.jpeg" width="250"> 
<img src="up last.jpeg" width="250"> <img src="left last.jpeg" width="250"> <img src="right last.jpeg" width="250">
