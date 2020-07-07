# 2020-sensing-intelligent-system-competition-NUC  

This repo is for locobot NUC.  
Control arm to pick and place object. 

## How to run on locobot:
- Open main.launch.
```
roslaunch locobot_control main.launch use_base:=true use_camera:=true use_arm:=true
```  
- Grasp:
```
source ~/pyenv_pyrobot/bin/activate
rosrun grasp grasping.py
```
Open another terminal, call grasp service.
```
rosservice call /grasp "pose:
  position:
    x: 0.30
    y: 0.0
    z: 0.10
  orientation:
    x: 0.0
    y: 0.707
    z: 0.0
    w: 0.707
id: 0"
```   
  
  
- Place:
```
source ~/pyenv_pyrobot/bin/activate
rosrun place placing.py
```
Open another terminal, call place service.
```
rosservice call /place "pose:
  position:
    x: 0.30
    y: 0.0
    z: 0.10
  orientation:
    x: 0.0
    y: 0.707
    z: 0.0
    w: 0.707
id: 0" 
```
