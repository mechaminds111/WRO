# WRO 2026 Future Engineers

## Team
MechaMinds

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

### 2. Obstacle Challenge
* **Objective:** The vehicle must complete three (3) laps while navigating throught a specific layout of randomly placed green and red obstacles and in the end it needs to do a parallel parking.
* **Traffic obstacle logic:**
  * **Red Pillar:** When the vehicle comes across a red obstacle it needs to keep to the **right** side of the lane.
  * **Green Pillar:** When the vehicle comes across a green obstacle it needs to keep to the **left** side of the lane.
* **The Parking Mission:** Upon completing the third lap, the vehicle must autonomously locate the designated parking zone (marked by magenta barriers) and do a precise, parallel parking maneuver without making contact with the walls or obstacles.

## Vehicle

Our vehicle is a fully autonomous self-driving car designed for the WRO 2026 Future Engineers competition. 
The robot is capable of following the track, avoiding obstacles, recognizing traffic signs and 
completing the parking challenge without human intervention.

## Vehicle & Mechanical Design

Our vehicle is a custom-engineered autonomous scale-model car designed strictly around the WRO 2026 Future Engineers regulations. The mechanical design balances a low center of gravity with structural stiffness to handle high-speed cornering and precise steering alignments.

### Technical Specifications & Constraints
* **Dimensions:** 250mm (Length) x 180 mm (Width) x 150 mm (Height) — *Strictly within the maximum allowed 300 x 200 x 300 mm boundary.*
* **Total Weight:** 1.25 kg — *Well under the maximum limit of 1.5 kilograms, optimizing acceleration and battery longevity.*

### Kinematics & Drivetrain Architecture
* **Steering Actuation:** We used a single LEGO steering motor configured with a physical geometry (Ackermann steering concept) to manage turning angles. This provides smooth traction and prevents the tires from slipping sideways during tight cornering.
* **Propulsion System:** Driven by a single angular high-torque LEGO motor connected to a fixed rear axle drivetrain via a 1:1 gearbox layout.Both drive wheels are physically locked to the same axle, completely eliminating any form of prohibited electronic or independent dual-motor differential setups.
* **Wheel Restrictions:** The vehicle rides exclusively on high-grip rubber tires.


## Hardware
- Controller: LEGO SPIKE Prime Hub
- Distance Sensor: LEGO Distance Sensor
- Color Sensor: LEGO Color Sensor
- Driving Motor: LEGO Motor
- Steering Motor: LEGO Motor

## Software
- Programming language: Python
- Operating system: Pybricks

## Repository Structure

/code - source code

/images - robot images

/videos - challenge videos

/docs - documentation

## Development

This repository is used to track the development of our autonomous vehicle for WRO 2026.
