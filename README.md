# TARS Robot

This is an experimental project to simulate and teach a robot control dynamics. The robot of choice is a simple model of the [TARS](docs/TARS.md) robot seen in Interstellar.


## Goal

The goal of this project is to teach the TARS robot to move forward in the simulated environment without moving any cones.

![Starting Position](docs/images/TARS_start.png)

An example python control program can be found in the tars_sample_controller package. It demonstrates the ability to control the TARS robot while it is in a physical simulation:

![Example Simulation](docs/images/TARS_example.png)

The TARS robot is currently very simplified. It has 3 joints and 4 legs all acuated around the center.

![TARS Robot](docs/images/TARS_rviz.png)


## Current Stage

Currently the project makes use of [ROS](http://www.ros.org/) and [Gazebo](http://gazebosim.org/) for controlling and simulating the robot respectively. 

## Setup

**This is currently only tested and running on Ubuntu 14.04**

### Installation
Dependencies:
+ [Install ROS](http://wiki.ros.org/indigo/Installation/Ubuntu)
+ [Install ROS Controller](http://wiki.ros.org/ros_control) - See bottom of wiki page
+ Check this directory out into your catkin workspace `src/` folder
+ Make your catkin workspace - `catkin_make; catkin_make install`

This project will compile packages as normal under ROS catkin make.

### To Run

To open Gazebo and begin a simulation run:

	roslaunch tars_sample_controller tars_runner.launch

You may also open Gazebo independently and then run the control script to repeatedly run trials. Run each of these in a separate terminal window:
	
	roslaunch tars_gazebo tars_world.launch
	rosrun tars_sample_controller tars_sample_controller.py


## Reference Material

Some articles and material that has been helpful:

+ [Tutorial: Using a URDF in Gazebo](http://gazebosim.org/tutorials?tut=ros_urdf)
+ [Tutorial: ROS Control](http://gazebosim.org/tutorials?tut=ros_control)
+ [Package: gazebo](http://wiki.ros.org/gazebo)

## Thanks!

Thanks for looking and please feel free to contact if you would like to help in any way. From 3D modelling to programming to AI to robot building - all is welcomed.