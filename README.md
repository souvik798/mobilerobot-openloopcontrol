# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure

Step1:

Use from robomaster import robot

<br/>

Step 2:

Choose the x,y,z - axis movement distance(meters).

<br/>

Step 3:

Give ep_chasis.move to move straight

<br/>

Step 4:

Give ep_chasis.drive to get circular motion.


<br/>

Step 5:

Give ep_chasis.move to move straight

<br/>

step 6:

Give ep_chasis.drive to get circular motion.

<br/>


## Program
```
from robomaster import robot
import time

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis

    '''
     = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5]
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second) [0.5,2]
    '''
    ep_chassis.move(x=1.7, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_chassis.drive_speed(x=0.425,y=-0.1,z=-20)
    time.sleep(12)
    ep_chassis.drive_speed(x=0,y=-0.1,z=-2.5)
    time.sleep(1)
    ep_chassis.move(x=3, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_chassis.drive_speed(x=2,y=-2,z=-75)
    time.sleep(1.5)
    ep_chassis.drive_speed(x=0,y=-0.1,z=-2.5)
    time.sleep(1)
    ep_chassis.move(x=5, y=0, z=0, xy_speed=0.75).wait_for_completed()
    ep_robot.close()


```

## MobileRobot Movement Image:

![robo](./img/robomaster.png)




<br/>
<br/>
<br/>
<br/>

## MobileRobot Movement Video:

Upload your video in Youtube and paste your video-id here

[![IMAGE ALT TEXT HERE](https://youtube.com/shorts/huDYj3T7nf8?feature=share)

<br/>
<br/>
<br/>
<br/>

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
