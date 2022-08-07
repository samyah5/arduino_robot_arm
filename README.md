# arduino_robot_arm
Installing the package arduino robot arm

## Creating Workspace 
```
mkdir -p ~/catkin_ws/src

cd ~/catkin_ws/

catkin_make

```

## Add the "arduino_robot_arm" package to "src" folder

```
cd ~/catkin_ws/src

sudo apt install git

git clone https://github.com/smart-methods/arduino_robot_arm.git 

```
## insatall all the dependecies
```
rosdep install --from-paths src --ignore-src -r -y

sudo apt-get install ros-noetic-moveit

sudo apt-get install ros-noetic-joint-state-publisher ros-noetic-joint-state-publisher-gui

sudo apt-get install ros-noetic-gazebo-ros-control joint-state-publisher

sudo apt-get install ros-noetic-ros-controllers ros-noetic-ros-control
```
## Compiler the package
```
catkin_make
```
## Controlling the motors
```
roslaunch robot_arm_pkg check_motors.launch
```
<img width="960" alt="Rviz" src="https://user-images.githubusercontent.com/108360083/183287976-ef818ac6-177e-4234-81fd-06e4428640db.png">



