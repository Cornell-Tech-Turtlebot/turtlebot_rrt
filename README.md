[![Build Status](https://travis-ci.org/jeshoward/turtlebot_rrt.svg?branch=master)](https://travis-ci.org/jeshoward/turtlebot_rrt) Travis Build Status 

[![License](https://img.shields.io/badge/License-BSD%203--Clause-blue.svg)](https://opensource.org/licenses/BSD-3-Clause) Software License 

 
# Randomly Exploring Random Tree Path Planner ROS Plugin
This plugin implements a simulated Randomly Exploring Random Tree (RRT) path planner for the Kinetic Kame release of the Robot Operating System (ROS) framework. It uses the nav_core::BaseGlobalPlanner interface and can be used on any platforms that implement the move_base package, but has been specifically tested using the simulated Turtlebot platform.

A presentation on the project can be found on YouTube [here](https://youtu.be/YW-AWwA-fv8). The video provides an overview of the project, UML diagrams, as well as a demo.

## Table of Contents
- [Personnel](#personnel)
- [Installation](#installation)
- [Usage](#usage)
- [License](#license)

## Personnel
This plugin was created by [Jessica Howard](jmhoward@umd.edu) as a final project for the University of Maryland course ENPM808X - Software Development for Robotics during the Fall 2017 semester. The plugin was developed for use with the turtlebot, but this fork of the repo is altered for use with turtlebot3.

## Installation
Clone the package into your catkin workspace:
```
cd [workspace]/src
git clone https://github.com/jeshoward/turtlebot_rrt.git
cd ..
catkin_make
source devel/setup.bash
```

## Usage
In order to use this as part of the turtlebot3_navigation package, add the following lines to the move_base node in the move_base.launch file under turtlebot3/turtlebot3_navigation/launch:

```
    <param name="base_global_planner" value="turtlebot_rrt/RRTPlanner"/>

    <rosparam file="$(find turtlebot_rrt)/config/rrt_global_planner_params.yaml" command="load"/>
```


## License
BSD 3-Clause License

Copyright (c) 2017, Jessica Howard
All rights reserved.

Redistribution and use in source and binary forms, with or without
modification, are permitted provided that the following conditions are met:
    * Redistributions of source code must retain the above copyright
      notice, this list of conditions and the following disclaimer.
    * Redistributions in binary form must reproduce the above copyright
      notice, this list of conditions and the following disclaimer in the
      documentation and/or other materials provided with the distribution.
    * Neither the name of the <organization> nor the
      names of its contributors may be used to endorse or promote products
      derived from this software without specific prior written permission.

THIS SOFTWARE IS PROVIDED BY THE COPYRIGHT HOLDERS AND CONTRIBUTORS "AS IS" AND
ANY EXPRESS OR IMPLIED WARRANTIES, INCLUDING, BUT NOT LIMITED TO, THE IMPLIED
WARRANTIES OF MERCHANTABILITY AND FITNESS FOR A PARTICULAR PURPOSE ARE
DISCLAIMED. IN NO EVENT SHALL <COPYRIGHT HOLDER> BE LIABLE FOR ANY
DIRECT, INDIRECT, INCIDENTAL, SPECIAL, EXEMPLARY, OR CONSEQUENTIAL DAMAGES
(INCLUDING, BUT NOT LIMITED TO, PROCUREMENT OF SUBSTITUTE GOODS OR SERVICES;
LOSS OF USE, DATA, OR PROFITS; OR BUSINESS INTERRUPTION) HOWEVER CAUSED AND
ON ANY THEORY OF LIABILITY, WHETHER IN CONTRACT, STRICT LIABILITY, OR TORT
(INCLUDING NEGLIGENCE OR OTHERWISE) ARISING IN ANY WAY OUT OF THE USE OF THIS
SOFTWARE, EVEN IF ADVISED OF THE POSSIBILITY OF SUCH DAMAGE.

