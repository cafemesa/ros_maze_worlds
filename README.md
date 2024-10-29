# ROS Maze Worlds

This repository provides maze models for the Gazebo Simulation Tool, designed to work with ROS. You can use the included launch file to load and customize different maze environments, setting the maze ID and the starting position of the robot.

## Installation (After install ROS and create your workspace)
1. **Clone this repository into you catkin workspace in the src folder and compile**
   ```bash
   cd ~/catkin_ws/src
   git clone https://github.com/cafemesa/ros_maze_worlds.git
   cd ~/catkin_ws
   catkin_make
   ```

2. **Copy Maze Models:**  
   Move the maze files from the `worlds` folder in this repository into your Gazebo models directory:

   ```bash
   cp -r models/* ~/.gazebo/models/
   ```


## Launching the Maze Simulation
Use the maze.launch file to start the simulation. You can choose between several predefined maze layouts and customize the robot’s starting position.

   ```bash
   roslaunch maze_pkg maze.launch maze_id:=<ID> x_pos:=<X_POSITION> y_pos:=<Y_POSITION>
   ```

### Arguments
1. maze_id: Choose a maze layout by setting the ID (1 to 7).
2. x_pos: Set the robot's initial x-coordinate.
3. y_pos: Set the robot's initial y-coordinate.
4. yaw_pos: Set the robot's initial yaw orientation.


### Example Usage

To launch the simulation with maze ID 3 and set the robot's starting position to (-3.0, 1.0):


   ```bash
   roslaunch maze_pkg maze.launch maze_id:=3 x_pos:=-3.0 y_pos:=1.0 yaw_pos:=3.1516
   ```