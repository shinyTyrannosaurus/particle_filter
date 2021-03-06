A reliable position estimation is of fundamental importance to building truly autonomous robots, 
especially the ones that perform navigation and local manipulation tasks, within indoor environments.
This is a demonstration of global localization for estimating the unknown pose of a moving robot, 
inside an environment whose map is known, by using the particle filter method.

The simulated robot uses a Stage-simulated 2D world with a known floorplan of the environment and 
unknown location. The robot must estiate its pose (position & direction angle) using the sensor 
measurements from laser range sensors on the robot that give information about the distances of the 
obstacles from the robot in certain angles, and then using the known map to match the locations that 
are more likely to mimic the robot’s pose. The robot uses the particle filter to determine its position 
in the stage simulator. A particle filter is represented by a set of random samples (particles) or 
guesses drawn from a prior distribution of guesses based on their importance weights. In the beginning, 
the beliefs of the robot’s pose on the map is completely uncertain. So initially it is expected that the 
particles or guesses are placed all over the map, all starting with an equal importance. The importance 
weights for a particle are updated by observing the laser measurements from laser sensor on robot and 
calculating the likelihood of that particle to see the obstacles as seen by the robot using the map data.

To run the simulation, you must have ROS installed. This sim was developed using ROS indigo:
http://wiki.ros.org/indigo/Installation

Once you have installed ros, clone this repo into your catkin workspace, launch ROScore, then navigate
to the launch directory and type:

'roslaunch solution_python.launch'

and the simulation should start.
