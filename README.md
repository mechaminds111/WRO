# WRO 2026 Future Engineers

## Team
MechaMinds, Srednja škola Tina Ujevića, Kutina, Croatia
<br><br><br>
At first we were classmates who didnt't talk much, but when we decided to come together as a team for a robotics competiton, everything changed. 
Now we are friends who love spending time together and most importantly, we are a **team** that is ready to overcome every challenge.
<br>
<br>
<img src="team1.jpeg" width="350" hight='300'> <img src="team2.jpeg" width="250" > <br>
<img src="team3.JPG" width="350" height='300'> <img src="team4.JPG" width="350" height='300'> <img src="lego - mechaminds.jpg" width="300" height='500'> 
<br>


## Members
While every member of MechaMinds was fully involved in every stage of development—from brainstorming and building to coding and testing, 
we each took the lead in specific areas to ensure maximum efficiency:

* **Ivano Koren** — *Lead Mechanical Engineer*. Ivano spearheaded the physical construction of the vehicle, optimizing the chassis layout, steering geometry, and weight distribution, while the team assisted in testing mechanical durability.
* **Barbara Lukić** — *Lead Software Engineer*. Barbara took the driver's seat for the core programming, developing program in Pybricks, with input from the whole team during track-side debugging.
* **Nadia Kravčuk** — *Systems Engineer & Documentation Lead*. Nadia directed our technical reporting, ensuring our engineering journal, while coordinating with the team to capture media and data.

## Repository Structure

* **images** - robot images

* **docs** - documentation

* **videos** - all videos are visible on our YouTube channel [MechaMinds](https://www.youtube.com/@MechaMinds111)

* **code** - source code


## Competition and our solutions
We are competing in the **World Robot Olympiad (WRO) 2026 – Future Engineers** category. The competition challenges us to design a scale-model autonomous vehicle capable of executing real-time decision-making under changing track conditions.

The 2026 tournament is focused on the vehicle completing two distinct challenges within a strict **3-minute time limit** per round:

### 1. Open Challenge
* **Objective:** The vehicle must successfully complete three (3) full consecutive laps on the track.
  <br>
**OUR SOLUTION:** In order for the robot to complete three laps around the field as efficiently and quickly as possible we added three (3) different distance sensors, one sensor on each side and one in the front. The robot is then set to move forward and if any of the three sensors detect something the robot is set to turn left or right depending on how it is defined in the code.

### 2. Obstacle Challenge
* **Objective:** The vehicle must complete three (3) laps while navigating throught a specific layout of randomly placed green and red obstacles and in the end it needs to do a parallel parking.
* **Traffic obstacle logic:**
  * **Red Pillar:** When the vehicle comes across a red obstacle it needs to keep to the **right** side of the lane.
  * **Green Pillar:** When the vehicle comes across a green obstacle it needs to keep to the **left** side of the lane.
* **The Parking Mission:** Upon completing the third lap, the vehicle must autonomously locate the designated parking zone (marked by magenta barriers) and do a precise, parallel parking maneuver without making contact with the walls or obstacles.
  <br>
**OUR SOLUTION:** To enable the robot to recognize the red and green obstacles, we would have needed color sensors. However, since we started working with LEGO robots relatively late, we did not have enough time to develop and test this feature. As a result, our robot does not use color sensors. Instead, our current solution relies on a pre-programmed path that tells the robot where it is supposed to go.

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


## Vehicle & mechanical design

Our vehicle is an autonomous model car according to the WRO 2026 Future Engineers rules. The mechanical design uses a rear-wheel-drive system where a single large LEGO motor provides power to the rear axle, while a single smaller LEGO motor acts as the steering motor to control the front wheels. This balances the vehicle's driving dynamics and prevents the tires from slipping sideways during tight cornering. Both drive wheels are physically locked to the same axle, completely eliminating any form of prohibited electronic or independent dual-motor differential setups.

### Technical specifications
* **Dimensions:** 225mm (Length) x 185 mm (Width) x 90 mm (Height) — *Within the maximum allowed 300 x 200 x 300 mm boundary.*
* **Total weight:** 0.532 kg — *Under the maximum limit of 1.5 kilograms.*

### Kinematics & drivetrain architecture
* **Steering actuation:** We used a single LEGO steering motor configured with a physical geometry (Ackermann steering concept) to manage turning angles. This provides smooth traction and prevents the tires from slipping sideways during sharp turns.
* **Propulsion system:** Driven by a single large LEGO motor connected to the rear axle with a 1:1 gear ratio. Both rear wheels are locked on the same axle, which perfectly follows the rules by eliminating any dual-motor or differential setups.
* **Wheel restrictions:** The vehicle rides exclusively on high-grip rubber tires.


## Hardware
- Controller: LEGO SPIKE Prime Hub
- Distance Sensor: LEGO Distance Sensor
- Color Sensor: LEGO Color Sensor
- Driving Motor: LEGO Motor
- Steering Motor: LEGO Motor

## Software - Power & sensor architecture

### 1. Wiring diagram & port assignment
To ensure a stable and reproducible control loop, all electronic components are directly routed to the LEGO SPIKE Prime Hub. The specific physical port arrangement is mapped as follows:

| Component | Device type | Port assignment | Function |
| :--- | :--- | :--- | :--- |
| **Driving motor** | LEGO Large Angular Motor | **Port A** | Rear-axle propulsion and velocity control |
| **Steering motor** | LEGO Medium Angular Motor | **Port C** | Front-wheel Ackermann steering actuation |
| **Distance sensors** | LEGO Distance Sensor | **Port E, Port D, Port F** | Front obstacle detection and distance tracking |

### 2. Sensor selection & placement justification
The positioning of our sensors was mathematically and physically optimized based on the official field geometry:
* **Distance Sensor:** Mounted on the leading edge of the front bumper at a height of 50 mm from the surface. This height ensures it perfectly captures the walls and distance from them.

### 3. Obstacle & parking logic
* **Red and green obstacles:** When an obstacle is located in front of the robot, the robot follows the program and turns left or right, depending on the color of the pillar.
* **The parking mission:** Since we did not have enough time to learn how to use the color sensor, the robot is programmed to at least attempt to park between the magenta obstacles.


## Development
**This repository is used to track the development of our autonomous vehicle for WRO 2026.**

We started working on our vehicle for WRO 2026 in late September. From then until June we have changed four different robots. 
The **First robot** we used was 3D printed and built by hand, using several distance sensors. The following pictures show the robot from all sides:
<br><br>
<img src="back1.jpeg" width="250"> <img src="front1.jpeg" width="250"> <img src="left side1.jpeg" width="250"> <img src="right side1.jpeg" width="250">
<img src="under1.jpeg" width="250"> <img src="up1.jpeg" width="250"> 
<br>
You can find this robot compleating three circles around the track on our YouTube channel or on this link: [First three laps around the track - walltracking](https://www.youtube.com/watch?v=BhE81YOuBHM)
<br> 
<br>
The **Second robot** was an upgraded version on the first one. It had a camera and several distance sensors all around it. Before we started programming we had to make new wheels and change a few parts. Next few pictures show us making new parts:
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
The **Third robot** was LEGO robot. It was made because we had big problems with connecting second robot to our laptop. It was inspired by classic Ford Model T.
The following pictures show the robot from all sides:
<br><br>
<img src="ford1.jpeg" width="250"> <img src="ford2.jpeg" width="250"> <img src="ford front.jpeg" width="250"> 
<img src="ford down.jpeg" width="250"> <img src="ford right.jpeg" width="250"> <img src="ford left.jpeg" width="250"> <img src="ford back.jpeg" width="250"> 
<br>
The video of this robot driving is also uploaded on our YouTube channel: [First three laps around the track - Ford](https://www.youtube.com/watch?v=bmhLn2NZVjs)
<br>
After some time working with LEGO robot we realized that, because of how the weight of the robot was distributed, we couldn't keep working with it and so we made a new, **Fourth**, LEGO robot which is our current one and the one we will be competing with. The following pictures are pictures of our current robot:
<br>
<img src="back last.jpeg" width="250"> <img src="front last.jpeg" width="250"> <img src="down last.jpeg" width="250"> 
<img src="up last.jpeg" width="250"> <img src="left last.jpeg" width="250"> <img src="right last.jpeg" width="250">

## Code
from pybricks.hubs import PrimeHub
from pybricks.pupdevices import Motor, ColorDistanceSensor, ColorSensor, UltrasonicSensor, ForceSensor
from pybricks.parameters import Button, Color, Direction, Port, Side, Stop
from pybricks.tools import hub_menu
from pybricks.tools import wait, StopWatch
from pybricks.robotics import DriveBase

robot = PrimeHub()
#senzor = ColorDistanceSensor(Port.B)  
senzor_udaljenostiD= UltrasonicSensor(Port.D) 
senzor_udaljenostiN= UltrasonicSensor(Port.F) 
senzor_udaljenostiL= UltrasonicSensor(Port.E)

motor_pogon=Motor(Port.A,Direction.COUNTERCLOCKWISE)#E
motor_skretanje=Motor(Port.C,Direction.CLOCKWISE)#F
#robot=DriveBase(motor_pogon,121,62.4)
#robot.use_gyro(True)

#varijable
rWheel=32.5
pi=3.141592653589793
tolerance=360
resetAngle=-77 #69
stallSpeed=500

cWheel=2*rWheel*pi

def ResetTurningAngle():
    motor_skretanje.run_until_stalled(stallSpeed)
    motor_skretanje.reset_angle()
    motor_skretanje.run_angle(300,resetAngle)
    motor_skretanje.reset_angle()

def fd(v,s): #brzina, distance
    angle=(s/cWheel)*360
    motor_pogon.reset_angle()
    motor_pogon.run_angle(v,angle)

def turn(v,t,d): #brzina, time, direction, 
    if d.upper()=='L' or d.upper()=='LEFT' or d.upper()== 'LIJEVO':
        motor_skretanje.run_until_stalled(-stallSpeed)
    if d.upper()=='D' or d.upper()=='R' or d.upper()=='DESNO' or d.upper()=='RIGHT':
        motor_skretanje.run_until_stalled(stallSpeed)
    motor_pogon.run(v) 
    wait(t)
    motor_pogon.stop()
    ResetTurningAngle()
    #motor_skretanje.run_target(300,resetAngle)

ResetTurningAngle()
#3L
'''for i in range(6):
    fd(1000,1000)
    turn(1000,2000,'l')#2000 time
    fd(1000,1200)#probaj jos 1100
    turn(1000,2000,'l')'''

#4L RADI!
'''fd(-1000,500)
for i in range(6):
    fd(1000,1000)
    turn(1000,2000,'l')#2000 time
    fd(1000,1100)
    turn(1000,2000,'l')'''

#1L+ reset angle na -69 RADI!
'''for i in range(6):
    fd(1000,1000)
    turn(1000,1600,'l')#2000 time
    fd(1000,1200)#ak ne radi stavi 1200 ko gore
    turn(1000,1600,'l')'''
#2L+RADI!
'''fd(1000,400)
for i in range(6):
    turn(1000,1600,'l')#2000 time
    fd(1000,1200)#ak ne radi stavi 1200 ko gore
    turn(1000,1500,'l')
    fd(1000,1400)'''
#5L
'''for i in range(6):
    fd(1000,1100)
    turn(1000,1700,'l')#2000 time
    fd(1000,1400)#ak ne radi stavi 1200 ko gore
    turn(1000,1700,'l')'''
#6L
'''fd(1000,400)
for i in range(8):
    turn(1000,1700,'l')#2000 time
    fd(1000,1400)#ak ne radi stavi 1200 ko gore
    turn(1000,1600,'l')
    fd(1000,1300)'''

#1D ko 2L
'''
#2D ko 1L
for i in range(6):
    fd(1000,1200)
    turn(1000,1700,'d')#2000 time
    fd(1000,1200)#ak ne radi stavi 1200 ko gore
    turn(1000,1700,'d')'''

'''#3D ko 4L
#4D ko 3L
for i in range(6):
    fd(1000,1000)
    turn(1000,2000,'d')#2000 time
    fd(1000,1200)#probaj jos 1100
    turn(1000,2000,'d')
#5D ko 6L
fd(1000,400)
for i in range(8):
    turn(1000,1700,'l')#2000 time
    fd(1000,1400)#ak ne radi stavi 1200 ko gore
    turn(1000,1600,'l')
    fd(1000,1300)
#6D ko 5L
'''

'''if selected =="1":
    drive1()
elif selected =="2":
    drive2()'''
'''def drive1():'''


'''for i in range(12):
    ResetTurningAngle()
    motor_pogon.run(1000)
    wait(100)    #ide ravno'''
    
    
    
'''motor_pogon.run(0)
    wait(900) #stane
    motor_skretanje.run_angle(1000, 60)
    wait(1000)    #zakrene se
    motor_pogon.run(1000)
    wait(500)  #pomakne se malo ravno
    motor_skretanje.run_angle(1000, -55)
    wait(1000)   #zakrenen se nazad tocno (malo manje)
    motor_pogon.run(1000)
    wait(1500)  #pici dalje ravno
    '''
    




'''def drive2():'''
'''for i in range(12):
    motor_pogon.run(1500)
    for t in range(40): 
        if senzor.color() == Color.RED:
            motor_skretanje.run_angle(1000,-60)
            wait(1000)
            motor_pogon.run(1000)
            wait(600)
            motor_skretanje.run_angle(1000,40)
            wait(1000)
            motor_pogon.run(1000)
            wait(1000)
            
        elif senzor.color() == Color.GREEN:
            motor_skretanje.run_angle(1000,60)
            wait(1000)
            motor_pogon.run(1000)
            wait(600)
            motor_skretanje.run_angle(1000,-40)
            wait(1000)
            motor_pogon.run(1000)
            wait(1000)
            
        wait(50) 


    wait(800)
    motor_skretanje.run_angle(1000, 60)
    wait(1200)
    motor_skretanje.run_angle(1000, -60)
    wait(1000)
'''

'''while True:
    color = sensor.color()
    if color == Color.RED :
        motor_pogon.run(0)
        wait(600)
    else:
        motor_pogon.run(1000)
        wait(600)
        

    wait(100)    '''



#senzor distance desni - port c
 
#print(senzor_udaljenosti.distance())

'''if senzor_udaljenosti.distance() > 100:
    motor_pogon.run(1000)
    wait(1900)
    
else:
    motor_skretanje.run_angle(1000, 30)
    wait(1000)
    motor_skretanje.run_angle(1000, -30)
    wait(1000)'''

'''motor_pogon.run(1000)  # stalno vozi naprijed

if senzor_udaljenosti.distance() <= 100:
    motor_skretanje.run_angle(1000, 30)
    wait(1000)
    motor_skretanje.run_angle(1000, -30)'''



'''ResetTurningAngle()'''
'''
senzor_udaljenosti = UltrasonicSensor(Port.D)
senzor_prednji = UltrasonicSensor(Port.F)

ResetTurningAngle()

while True:

    # spora vožnja naprijed
    motor_pogon.run(500)

    # ako prednji senzor vidi prepreku na 20 cm
    if senzor_prednji.distance() <= 200:

        motor_pogon.stop()

        motor_skretanje.run_target(300, 60)  # desno
        wait(1000)

        motor_pogon.run(300)
        wait(1000)

        motor_skretanje.run_target(300, 0)   # ravno

    # ako bočni senzor vidi prepreku na 10 cm
    elif senzor_udaljenosti.distance() <= 100:

        motor_skretanje.run_target(300, -40)  # lijevo

    else:

        motor_skretanje.run_target(300, 0)    # ravno

    wait(50)'''

ResetTurningAngle()

motor_pogon.reset_angle()
motor_pogon.run(800)

while robot.imu.heading() <= 360 * 3:
    
    if  senzor_udaljenostiN.distance()<=600 :
        #motor_pogon.run(500)
        #turn(400, 20,'l' )
        if senzor_udaljenostiL.distance() > senzor_udaljenostiD.distance():
            turn(400, 20, 'l')   # više mjesta lijevo
        else:
            turn(400, 20, 'd')   # više mjesta desno
   
    elif  senzor_udaljenostiD.distance()<200 and senzor_udaljenostiL.distance() >200:
        motor_pogon.run(500)
        turn(400, 20,'l' )
        
    elif senzor_udaljenostiD.distance() > 200 and senzor_udaljenostiL.distance()<200:
        motor_pogon.run(500)
        turn(400, 20,'d')

    else:
        motor_pogon.run(500)

    wait(10)

motor_pogon.stop()

