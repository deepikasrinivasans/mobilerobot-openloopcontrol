# MobileRobot-Openloopcontrol
## Aim:

To develop a python control code to move the mobilerobot along the predefined path.

## Equipments Required:
1. RoboMaster EP core
2. Python 3.7

## Procedure
### Step1:
Import the required packages
### Step2:
Assign the value for X axis and Y axis 
### Step3:
write the program to move the Robot
### Step4:
Write the program to record video
### Step5:
Run the program to move the robot



## Program
```
#Developed by: Deepika S
#Register number: 212222230028

from robomaster import robot
import time
from robomaster import camera

if _name_ == '_main_':
    ep_robot = robot.Robot()
    ep_robot.initialize(conn_type="ap")

    ep_chassis = ep_robot.chassis
    ep_led = ep_robot.led
    ep_camera = ep_robot.camera
          
    print("Video streaming started.....")
    ep_camera.start_video_stream(display=True, resolution = camera.STREAM_360P)
    ''' 
    x = x-axis movement distance,( meters) [-5,5]
    y = y-axis movement distance,( meters) [-5,5] 
    z = rotation about z axis ( degree)[-180,180]
    xy_speed = xy axis movement speed,( unit meter/second)  [0.5,2]

    '''
    ep_chassis.move(x=5.3, y=0, z=0, xy_speed=1).wait_for_completed()
 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed()
    # ep_led.set_led(comp="all",r=255,g=100,b=0,effect="on")  
    ep_chassis.move(x=4, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=5, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=3, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=0, y=0, z=-90, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=2, y=0, z=0, xy_speed=1).wait_for_completed() 
    ep_chassis.move(x=3, y=0, z=-360, xy_speed=1).wait_for_completed() 
    








    '''
    x = speed in x direction( meter/second) [-3.5,3.5]
    y = speed in y direction( meter/second) [-3.5,3.5]
    z = rotation about z axis ( degree/second)[-300,300]
    '''
'''   ep_led.set_led(comp="all",r=0,g=0,b=255,effect="on")  
    ep_chassis.drive_speed(x=0.4,y=0,z=-20)
    time.sleep(12)
    ep_led.set_led(comp="all",r=0,g=255,b=0,effect="on") 
    ep_chassis.move(x=2.95, y=0, z=0, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=100,g=255,b=0,effect="on") 
    
    
    ep_chassis.move(x=0.1, y=0, z=60, xy_speed=1).wait_for_completed()
    ep_led.set_led(comp="all",r=0,g=0,b=255,effect="on") 
    ep_chassis.move(x=0.8, y=0, z=0, xy_speed=1).wait_for_completed()

    ep_chassis.drive_speed(x=0.2,y=0,z=-20.5)
    time.sleep(4)
    
    ep_chassis.move(x=2.8, y=0, z=0, xy_speed=1).wait_for_completed()

    
    
'''   
ep_camera.stop_video_stream()
print("Stopped video streaming.....")
ep_robot.close()
```

    


## MobileRobot Movement IMAGE:
## INITIAL POSITION:
![STARTING POINT](https://github.com/abinayasangeetha/mobilerobot-openloopcontrol/assets/119393675/22963d5c-1e81-456e-9469-a274d19c6e7d)


## FINAL POSITION:

![ENDING POINT](https://github.com/abinayasangeetha/mobilerobot-openloopcontrol/assets/119393675/37031dc1-e19b-4921-a1fa-be5389d364bb)

## MobileRobot Movement Video:
https://youtu.be/xkAumdRbGyU 

## Result:
Thus the python program code is developed to move the mobilerobot in the predefined path.


<br/>
<br/>

```
Mobile Robotics Laboratory
Department of Artificial Intelligence and Data Science/ Machine Learning
Saveetha Engineering College
```
